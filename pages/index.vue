<template>
  <div id="screen" class="w-screen h-screen">
    <div id="content" class="w-full h-full relative">
      <PageSectionLayout
        @next="nextSilde"
        @prev="prevSilde"
        :swiperInstance="swiperInstance"
        :sliderItems="sliderItems"
        @jumpTo="ChangeSlide"
        @showMenu="showPageMenu = true"
      />
      <page-menu :show="showPageMenu" @closeMenu="showPageMenu = false" />
      <swiper
        v-model="swiperInstance"
        :items="sliderItems"
        :options="swiperOptions"
        class="product-related__swiper overflow-hidden w-full h-full"
      >
        <template #default="{ slide }" class="object-cover">
          <v-img
            :lazy-src="slide.src"
            :src="slide.src"
            width="100vw"
            height="100vh"
            :aspect-ratio="16 / 9"
            cover
            class="object-cover"
          ></v-img>
        </template>
      </swiper>
    </div>
  </div>
</template>
<script>
import pageHeaderComponent from '~/components/pageSectionLayout.vue'
import PageSectionLayout from '~/components/pageSectionLayout.vue'
export default {
  components: { pageHeaderComponent, PageSectionLayout },
  data() {
    return {
      swiperInstance: null,
      showPageMenu: false,
      swiperOptions: {
                        loop: true,
                autoplay: {
                    delay: 5000,
                },
        // loop: true,

        // effect: 'creative',
        // creativeEffect: {
        //   prev: {
        //     shadow: true,
        //     translate: ['-20%', 0, 0],
        //   },
        //   next: {
        //     translate: ['100%', 0, 0],
        //   },
        // },
      },
      sliderItems: [
        {
          title: 'We Are Trusted',
          subText:
            'Our clients, partners and company employees valueour reliability and financial discipline',
          src: 'b1.jpg',
        },
        {
          title: 'OGK Group',
          subText:
            'The only independent mining service company in Russia and CIS that provides a full range of services.',
          src: 'b2.jpg',
        },
        {
          title: 'We can do everything',
          subText:
            'We provide all types of services, including drilling for solid minerals, drilling and blasting, mining workings, rock mass excavation and haulage.',
          src: 'b3.jpg',
        },
        {
          title:  'The best equipment',
          subText:
            'We have state of the art equipment and continually invest the money into expanding our capacities.',
          src: 'b4.jpg',
        },
      ],
    }
  },

  methods: {
    ChangeSlide(i) {
      this.swiperInstance.slideTo(i)
    },
    nextSilde() {
      this.swiperInstance.slideNext()
    },
    prevSilde() {
      this.swiperInstance.slidePrev()
    },
    slideCurrentIndex() {
      console.log(this.swiperInstance.activeIndex)
      // return this.swiperInstance.activeIndex
    },
  },

  // watch: {
  //   i: function (e) {
  //     if (e == this.sliderItems.length - 1) {
  //       this.$nuxt.$emit('resetI', -1)
  //     }
  //     console.log(e)
  //   },
  // },
}
</script>
<style scoped>
#screen {
  position: relative;
  width: 100%;
  min-height: 100%;
  z-index: 5;
  -webkit-transform-origin: 0 0;
  transform-origin: 0 0;
  -webkit-transition: -webkit-transform 0.75s ease;
  transition: -webkit-transform 0.75s ease;
  transition: transform 0.75s ease;
  transition: transform 0.75s ease, -webkit-transform 0.75s ease;
  -webkit-backface-visibility: hidden;
  backface-visibility: hidden;
}
#screen #content {
  position: relative;
  background-color: #fff;
  width: 100%;
  -webkit-transition: 0.5s;
  transition: 0.5s;
  min-height: 100%;
}
</style>