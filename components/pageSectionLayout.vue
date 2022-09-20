<template>
  <div>
    <div
      class="page-header-container w-screen h-screen absolute z-50 pr-48 overflow-hidden"
    >
      <v-row algin="center" justify="center" no-gutters>
        <v-col cols="1">
          <v-row class="pa-0 ma-0">
            <v-col
              cols="6"
              offset="6"
              class="border border-neutral-50 border-b-0 border-r-0"
              justify="center"
              align="center"
            >
              <p
                class="py-tag cursor-pointer animate__animated animate__bounce"
              >
                py
              </p>
            </v-col>
            <v-col
              cols="6"
              offset="6"
              class="border border-neutral-50 border-r-0"
              justify="center"
              align="center"
            >
              <p
                class="EN-tag cursor-pointer animate__animated animate__bounce"
              >
                EN
              </p>
            </v-col>
          </v-row>
        </v-col>
        <v-col cols="2" class="border border-neutral-50 border-b-0 border-r-0">
          <div class="logo animate__animated animate__bounce">
            <nuxt-link to="/">
              <img
                class="opacity-1"
                src="../static/ogk-logo-en-white-nodesc.svg"
                alt=""
              />
              <img
                class="opacity-1"
                src="../static/ogk-logo-en-white-desc.svg"
                alt=""
              />
            </nuxt-link>
          </div>
        </v-col>
        <v-col cols="2" class="border border-neutral-50 border-b-0 border-r-0">
        </v-col>
        <v-col cols="2" class="border border-neutral-50 border-b-0 border-r-0">
        </v-col>
        <v-col cols="2" class="border border-neutral-50 cursor-pointer">
          <div
            class="button toggle-menu flex items-center justify-center mt-10 mr-32 cursor-pointer animate__animated animate__fadeInUp"
            @click="$emit('showMenu')"
          >
            <ul class="hamburger">
              <li></li>
              <li></li>
              <li></li>
            </ul>

            <span class="menu-hover ml-4 mb-4"></span>
          </div>
        </v-col>
      </v-row>

      <v-row algin="center" justify="center" no-gutters class="h-44">
        <v-col
          cols="2"
          offset="1"
          class="border border-neutral-50 border-t-0 border-r-0"
        >
        </v-col>
        <v-col cols="2" class="border border-neutral-50 border-t-0 border-r-0">
        </v-col>
        <v-col cols="2" class="border border-neutral-50 border-t-0 border-r-0">
        </v-col>
        <v-col
          cols="2"
          align="center"
          justify="center"
          class="border border-neutral-50 border-t-0"
        >
        </v-col>
      </v-row>

      <v-row algin="center" justify="center" no-gutters class="h-96">
        <v-col
          offset="1"
          cols="6"
          class="border border-neutral-50 border-t-0 border-r-0 border-b-0 pl-10 pt-10"
        >
        
          {{ swiperInstance && swiperInstance.realIndex }}
          <h1 class="titleText text-white animate__animated animate__fadeInUp">
            {{
              swiperInstance && sliderItems[swiperInstance.realIndex].title
            }}
            <!-- {{ swiperInfo[infoIndex].title }} -->
          </h1>
          <p class="subText text-white animate__animated animate__fadeInUp">
            {{
              swiperInstance && sliderItems[swiperInstance.realIndex].subText
            }}
          </p>
        </v-col>

        <v-col
          cols="2"
          align="center"
          justify="center"
          class="border border-neutral-50 border-t-0 border-b-0 overflow-hidden"
        >
          <index-video-compo class="animate__animated animate__fadeInUp" />
        </v-col>
      </v-row>

      <v-row algin="center" justify="center" no-gutters class="h-24">
        <v-col
          cols="2"
          offset="1"
          class="border border-neutral-50 border-b-0 border-r-0"
        >
        </v-col>
        <v-col cols="2" class="border border-neutral-50 border-b-0 border-r-0">
        </v-col>
        <v-col cols="2" class="border border-neutral-50 border-b-0 border-r-0">
        </v-col>
        <v-col cols="2" class="border border-neutral-50 overflow-hidden">
          <div
            class="control-section w-full h-full bg-white flex item-center justify-start"
          >
            <div class="btn-play basis-24">
              <div class="btn-icon z-50">
                <v-icon large color="white" class="cursor-pointer"
                  >mdi-play</v-icon
                >
              </div>
            </div>
            <div
              class="btn-describtion basis-full flex items-start justify-center h-10 flex-column pl-8"
            >
              <span class="normal">
                <div class="video-title">About the&nbsp;Group</div>
                <div class="video-duration">2:17 min</div>
              </span>

              <span class="hover">
                <div class="video-title">About the&nbsp;Group</div>
                <div class="video-duration">2:17 min</div>
              </span>
            </div>
          </div>
        </v-col>
      </v-row>

      <v-row algin="center" justify="center" no-gutters class="h-24">
        <v-col
          cols="2"
          offset="1"
          class="border border-neutral-50 border-t-0 border-b-0 border-r-0"
        >
        </v-col>
        <v-col
          cols="2"
          class="border border-neutral-50 border-t-0 border-b-0 border-r-0"
        >
        </v-col>
        <v-col
          cols="2"
          class="border border-neutral-50 border-t-0 border-b-0 border-r-0"
        >
        </v-col>
        <v-col
          cols="2"
          align="center"
          justify="center"
          class="border border-neutral-50 border-t-0 border-b-0"
        >
        </v-col>
      </v-row>

      <v-row algin="center" justify="center" no-gutters class="h-28">
        <v-col
          cols="3"
          class="navigateDown border border-neutral-50 -left-36 flex item-center justify-center cursor-pointer"
          style="background-color: #009a67"
        >
          <v-icon color="white" class="z-50" x-large> mdi-chevron-down </v-icon>
        </v-col>

        <v-col
          cols="2"
          class="border border-neutral-50 bg-white -left-36 flex items-center justify-center gap-4 animate__animated animate__fadeInUp"
        >
          <v-progress-circular
            v-for="(item, index) in sliderItems"
            :key="index"
            :rotate="-90"
            :size="30"
            :width="2"
            :value="value"
            color="teal"
            class="cursor-pointer"
            @click="$emit('jumpTo', index)"
          >
            <v-icon>mdi-circle-small</v-icon>
          </v-progress-circular>
        </v-col>
        <v-col
          cols="2"
          class="border border-neutral-50 border-t-0 border-b-0 border-r-0 -left-36"
        >
          <v-col
            cols="6"
            class="border border-neutral-50 bg-white h-full animate__animated animate__fadeInUp"
          >
            <div class="flex items-center justify-center gap-5 mt-8">
              <v-icon
                class="text-black cursor-pointer mdiPrev"
                @click="prevSilde()"
                x-large
                >mdi-chevron-left</v-icon
              >
              <v-icon
                class="text-black cursor-pointer mdiNext"
                @click="nextSlide()"
                x-large
                >mdi-chevron-right</v-icon
              >
            </div>
          </v-col>
        </v-col>
        <v-col
          cols="2"
          class="border border-neutral-50 border-t-0 border-b-0 border-r-0 -left-36"
        >
        </v-col>
        <v-col
          cols="2"
          align="center"
          justify="center"
          class="border border-neutral-50 border-t-0 border-b-0 -left-36"
        >
        </v-col>
      </v-row>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      notOpen: true,
      i: 0,

      interval: {},
      value: 0,
      infoIndex: 0,
    }
  },
  props: {
    swiperInstance: Object,
    sliderItems: Array,
  },
  methods: {
    nextSlide() {
      // this.$nuxt.$emit('incremnet', (this.i = this.i + 1))
      this.$emit('next')
    },
    prevSilde() {
      // this.$nuxt.$emit('decrement', (this.i = this.i - 1))
      this.$emit('prev')
    },

    logHello: function () {
      setInterval(() => {
        if (this.infoIndex == 3) {
          this.infoIndex = 0
        } else {
          this.infoIndex++
        }
      }, 5000)
    },
  },
  mounted() {
    this.$nuxt.$on('resetI', ($event) => (this.i = $event))
    this.$nuxt.$on('resetImax', ($event) => (this.i = $event))

    this.logHello()
    this.interval = setInterval(() => {
      if (this.value === 100) {
        return (this.value = 0)
      }
      this.value += 20
    }, 800)
  },
  beforeDestroy() {
    clearInterval(this.interval)
  },
}
</script>
<style>
.page-header-container {
  width: 100vw;
  height: 100vh;
  z-index: 50;
  padding-left: 2rem;
  padding-right: 11.5rem;
  position: absolute;
  top: 0rem;
  overflow: hidden !important;
}
div.logo img {
  position: absolute;
  top: 24px;
  left: 17%;
  width: 180px;
  -webkit-transition: opacity 0.5s ease, -webkit-transform 0.5s ease;
  transition: opacity 0.5s ease, -webkit-transform 0.5s ease;
  transition: opacity 0.5s ease, transform 0.5s ease;
  transition: opacity 0.5s ease, transform 0.5s ease,
    -webkit-transform 0.5s ease;
}
.toggle-menu {
  position: relative;
  white-space: nowrap;
  -webkit-transition: all 0.5s ease;
  transition: all 0.5s ease;
  display: flex;
  align-content: center;
  justify-self: center;
  gap: 15px;
}

.toggle-menu:hover .menu-hover::before {
  transition: 0.3s cubic-bezier(0.175, 0.885, 0.32, 1.275);
  top: -2rem;
  opacity: 0;
  color: #009a67;
}

.toggle-menu:hover .menu-hover::after {
  transition: 0.5s cubic-bezier(0, 0.885, 0.32, 1.275);
  top: 0rem;
  opacity: 1;
  color: #009a67;
}

.btn,
.button {
  outline: 0;
  border: 0;
  -webkit-box-sizing: border-box;
  box-sizing: border-box;
  white-space: nowrap;
  cursor: pointer;
  text-align: center;
  text-decoration: none;
  border: 1px transparent solid;
  background-color: transparent;
  -webkit-transition: 0.5s ease;
  transition: 0.5s ease;
  z-index: 1000;
  color: #ffffff;
}
ul.hamburger li {
  width: 25px;
  height: 3px;
  background-color: #009a67;
  border-radius: 0.1px;
  margin-bottom: 4px;
  border-radius: 10px;
  -webkit-transition: opacity 0.5s ease, -webkit-transform 0.5s ease;
  transition: opacity 0.5s ease, -webkit-transform 0.5s ease;
  transition: opacity 0.5s ease, transform 0.5s ease;
  transition: opacity 0.5s ease, transform 0.5s ease,
    -webkit-transform 0.5s ease;
}
.menu-hover {
  position: relative;
  font-family: 'MetronicPro';
  line-height: 14px;
  font-size: 14px;
  transition: all 0.4s cubic-bezier(0.215, 0.61, 0.355, 1);
}
.titleText {
  font-size: 72px;
  width: 50%;
  line-height: 5rem;
  margin-bottom: 1rem;
  letter-spacing: 2px;
  line-height: 1em;
  font-family: Metronic, sans-serif;
  font-weight: normal;
}
.subText {
  width: 65%;
  font-family: Metronic, sans-serif;
  margin-top: 24px;
  font-size: 16px;
  line-height: 1.5;
}

.menu-hover::before {
  content: 'MENU';
  text-align: center;
  font-family: Metronic, sans-serif;
  font-weight: 600;
  letter-spacing: 0.4px;
  text-transform: uppercase;
  z-index: 5;
  font-size: 14px;
  line-height: 1em;
  z-index: 20;
  -webkit-transition: 0.3s ease;
  transition: 0.3s ease;
  transition: 0.5s cubic-bezier(0.175, 0.885, 0.32, 1.275);
  position: absolute;
  top: 0;
  left: 0;
}
.menu-hover::after {
  content: 'MENU';
  text-align: center;
  font-family: Metronic, sans-serif;
  font-weight: 600;
  letter-spacing: 0.4px;
  text-transform: uppercase;
  z-index: 5;
  font-size: 14px;
  line-height: 1em;
  z-index: 20;
  -webkit-transition: 0.3s ease;
  transition: 0.3s ease;
  transition: 0.5s cubic-bezier(0.175, 0.885, 0.32, 1.275);
  position: absolute;
  top: 2rem;
  opacity: 0;
  left: 0;
}

.col,
.row {
  padding: 0 !important;
}

.col {
  position: relative;
}
.border-neutral-50 {
  --tw-border-opacity: 0.1 !important;
  border-color: rgb(250 250 250 / var(--tw-border-opacity)) !important;
}
.control-section {
  cursor: pointer;
  overflow: hidden;
}

.btn-play {
  border: none;
  outline: none;
  background-color: #009a67;
  display: flex;
  align-items: center;
  justify-content: center;
  opacity: 1;
}

.control-section {
  -webkit-transition: -webkit-transform 0.5s ease;
  transition: -webkit-transform 0.5s ease;
  transition: transform 0.5s ease;
  transition: transform 0.5s ease, -webkit-transform 0.5s ease;
}

.control-section .btn-play::after {
  content: '';
  position: absolute;
  width: 6rem;
  height: 100%;
  background-color: #02795a;
  top: 0%;
  left: 0;
  transition: all 0.4s cubic-bezier(0.215, 0.61, 0.355, 1);
}

.btn-describtion span.normal {
  margin-top: 7rem;
  visibility: visible;
  opacity: 1;
  transition: all 0.3s cubic-bezier(0.215, 0.61, 0.355, 1);
}
.btn-describtion span.hover {
  visibility: hidden;
  opacity: 0;
  transition: all 0.3s cubic-bezier(0.215, 0.61, 0.355, 1);
}

.btn-describtion span.normal .video-title,
.btn-describtion span.hover .video-title {
  font-size: 14px;
  line-height: 1.57;
  color: #333333;
  font-weight: 500;
}

.btn-describtion span.normal .video-duration,
.btn-describtion span.hover .video-duration {
  font-family: 'OpenSans-Medium';
  font-size: 14px;
  font-weight: 400;
  color: #979797;
  margin-top: 0.5rem;
}

.control-section:hover .btn-play::after {
  top: 0%;
  transition: all 0.4s cubic-bezier(0.215, 0.61, 0.355, 1);
}
.control-section:hover .btn-describtion span.normal {
  margin-top: 2rem;
  visibility: visible;
  opacity: 0;
  transition: all 0.3s cubic-bezier(0.215, 0.61, 0.355, 1);
}

.control-section:hover .btn-describtion span.hover {
  margin-top: -2rem;
  visibility: visible;
  opacity: 1;
  transition: all 0.3s cubic-bezier(0.215, 0.61, 0.355, 1);
}

.py-tag,
.EN-tag {
  color: #ffffff;
  margin-top: 0.8rem;
  width: 100%;
  text-align: center;
  font-family: Metronic, sans-serif;
  font-weight: 600;
  letter-spacing: 0.4px;
  z-index: 5;
  font-size: 14px;
  line-height: 1em;
  z-index: 20;
  -webkit-transition: 0.3s ease;
  transition: 0.3s ease;
  transition: all 0.2s cubic-bezier(0.215, 0.61, 0.355, 1);
}
.EN-tag {
  color: rgba(255, 255, 255, 0.3);
}
.py-tag:hover {
  color: #fff !important;
  text-shadow: 0 0 5px #03e9f4, 0 0 25px #03e9f4, 0 0 50px #03e9f4,
    0 0 100px #03e9f4;
  letter-spacing: 0.1rem;
  transition: all 0.2s cubic-bezier(0.215, 0.61, 0.355, 1);
}
.EN-tag:hover {
  color: #fff !important;
  text-shadow: 0 0 5px #03e9f4, 0 0 25px #03e9f4, 0 0 10px #03e9f4,
    0 0 1000px #03e9f4;
  letter-spacing: 0.1rem;
  transition: all 0.2s cubic-bezier(0.215, 0.61, 0.355, 1);
}
.mdiNext:hover {
  margin-left: 0.5rem;
  color: #008f69;
  transition: all 0.5s cubic-bezier(0.215, 0.61, 0.355, 1);
}
.mdiPrev:hover {
  margin-right: 0.5rem;
  color: #008f69;
  transition: all 0.5s cubic-bezier(0.215, 0.61, 0.355, 1);
}
.navigateDown::after {
  content: '';
  position: absolute;
  top: 100%;
  left: 0;
  opacity: 1;
  width: 100%;
  height: 100%;
  background-color: #ffffffec;
  transition: all 0.5s cubic-bezier(0.215, 0.61, 0.355, 1);
}

.navigateDown:hover::after {
  top: -1% !important;
}
.navigateDown:hover .v-icon {
  color: #008f69 !important;
}
</style>