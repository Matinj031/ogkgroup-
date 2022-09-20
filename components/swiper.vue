<template>
  <div ref="swiper" v-bind="$attrs" v-on="$listeners">
    <div class="swiper-wrapper">
      <div
        v-for="(slide, i) in items"
        :key="'swiperSlide' + i"
        class="swiper-slide"
      >
        <slot :slide="slide" :keys="compKeys">
          <img :src="slide[compKeys.src]" :alt="slide[compKeys.alt]" />
        </slot>
      </div>
    </div>
    <div
      v-if="compOptions.scrollbar"
      class="swiper-scrollbar"
      :class="compOptions.scrollbar.class"
    ></div>
    <div
      v-if="compOptions.pagination"
      class="swiper-pagination"
      :class="compOptions.pagination.class"
    ></div>
  </div>
</template>

<script>
import { Swiper, Autoplay, Scrollbar, Pagination } from 'swiper'
import 'swiper/swiper-bundle.min.css'

export default {
  name: 'Swiper',

  props: {
    value: {
      type: Object,
      default: undefined,
    },
    items: {
      type: [Array, Object],
      default: () => [],
    },
    options: {
      type: Object,
      default: () => {},
    },
    keys: {
      type: Object,
      default: () => {},
    },
  },

  data() {
    return {
      swiper: undefined,
      initOptions: {
        modules: [Autoplay, Scrollbar, Pagination],
        on: {
          activeIndexChange: (ummmm) => {
            console.log(ummmm)
          },
        },
      },
      defaultKeys: {
        src: 'src',
        alt: 'alt',
      },
    }
  },

  computed: {
    compOptions() {
      return { ...this.initOptions, ...this.options }
    },
    compKeys() {
      return { ...this.defaultKeys, ...this.keys }
    },
  },

  watch: {
    swiper(instance) {
      instance !== undefined &&
        this.swiper === undefined &&
        this.swiperMounted()
    },
  },

  mounted() {
    Swiper.use([Autoplay, Scrollbar, Pagination])
    this.swiper = new Swiper(this.$refs.swiper, this.compOptions)
    this.swiperMounted()
  },

  methods: {
    swiperMounted() {
      this.$emit('input', this.swiper)
      this.$emit('mounted')
    },
  },
}
</script>