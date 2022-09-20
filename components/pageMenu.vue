<template>
  <div
    class="page-header-container menu-container w-screen h-screen absolute z-50 pr-48 overflow-hidden animate__animated"
    :class="{
      ' animate__fadeOutUp': show == false,
      ' animate__slideInDown': show == true,
    }"
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
              style="
                color: ghostwhite;
                margin-top: 1.2rem;
                font-family: MetronicPro-Bold;
                font-weight: 800;
                letter-spacing: 0.4px;
                text-transform: uppercase;
                font-size: 14px;
                line-height: 1em;
              "
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
              style="
                color: #757778;
                margin-top: 1.2rem;
                font-family: MetronicPro-Bold;
                font-weight: 800;
                letter-spacing: 0.4px;
                text-transform: uppercase;
                font-size: 14px;
                line-height: 1em;
              "
            >
              EN
            </p>
          </v-col>
        </v-row>
      </v-col>
      <v-col
        cols="2"
        class="border border-neutral-50 border-b-0 border-r-0 border-t-0"
      >
        <div class="logo animate__animated animate__bounce">
          <nuxt-link to="/">
            <img
              class="opacity-1"
              src="../static/ogk-logo-en-white-nodesc.svg"
              alt=""
            />
          </nuxt-link>
        </div>
      </v-col>
      <v-col
        cols="2"
        class="border border-neutral-50 border-b-0 border-r-0 border-t-0"
      >
      </v-col>
      <v-col
        cols="2"
        class="border border-neutral-50 border-b-0 border-r-0 border-t-0"
      >
        <div class="diagonal-container to-left"></div>
      </v-col>
      <v-col
        cols="2"
        class="border border-neutral-50 cursor-pointer border-b-0 border-t-0"
      >
        <div
          class="button toggle-menu flex items-center justify-center mt-10 mr-32 cursor-pointer animate__animated animate__fadeInUp"
        >
          <v-icon
            color="#009A67"
            large
            class="ml-4"
            @click="$emit('closeMenu')"
          >
            mdi-close
          </v-icon>
          <span class="menu-hover ml-4 mb-4"></span>
        </div>
      </v-col>
    </v-row>

    <v-row algin="center" justify="center" no-gutters class="h-36">
      <v-col cols="8" offset="1" class="border border-neutral-50">
        <div
          class="link-container flex items-center justify-start w-full h-full"
        >
          <nuxt-link class="ml-12 link-active" to="/">MAIN</nuxt-link>
          <nuxt-link class="ml-12" to="/">PROJECTS GEOGRAPHY</nuxt-link>
          <nuxt-link class="ml-12" to="/">EQUIPMENT</nuxt-link>
          <nuxt-link class="ml-12" to="/">CONTACTS</nuxt-link>
        </div>
      </v-col>
    </v-row>

    <v-row algin="center" justify="center" no-gutters class="h-60">
      <v-col
        cols="8"
        offset="1"
        class="border border-neutral-50 border-t-0 border-b-0"
      >
        <div class="services-container">
          <h1>SERVICES</h1>
          <div class="services">
            <nuxt-link to="/">SURFACE DRILLING</nuxt-link>
            <nuxt-link to="/">UNDERGROUND CORE DRILLING</nuxt-link>
            <nuxt-link to="/">GRADE CONTROL RC DRILLING</nuxt-link>
            <nuxt-link to="/"> DRILLING AND BLASTING SERVICES</nuxt-link>
            <nuxt-link to="/">ROCK MASS EXCAVATION AND HAULAGE</nuxt-link>
            <nuxt-link to="/">
              PRIMARY AND SECONDARY DEVELOPMENT, AND STOPING IN UNDERGROUND MINE
              WORKINGS</nuxt-link
            >
            <nuxt-link to="/">HOLE CONSTRUCTION AND UP-HOLE DRILLING</nuxt-link>
          </div>
        </div>
      </v-col>
    </v-row>

    <v-row algin="center" justify="center" no-gutters class="h-44">
      <v-col
        cols="6"
        offset="1"
        class="border border-neutral-50 border-b-0 border-r-0"
      >
        <div class="about-group-container">
          <h1>ABOUT THE GROUP</h1>
          <div class="about-links">
            <nuxt-link to="/">ABOUT US</nuxt-link>
            <nuxt-link to="/">STRUCTURE</nuxt-link>
            <nuxt-link to="/">MANAGEMENT</nuxt-link>
            <nuxt-link to="/">OUR CLIENTS</nuxt-link>
            <nuxt-link to="/">DOCUMENTS</nuxt-link>
          </div>
        </div>
      </v-col>
      <v-col cols="2" class="border border-neutral-50 border-b-0">
        <div
          class="download-section flex items-center justify-center w-full h-full"
        >
          <img
            src="../static/small-doc-1.svg"
            width="105px"
            height="auto"
            alt=""
          />
          <div class="text">
            <div class="title">
              download<br />
              presentation
            </div>
            <div class="cap">PDF, 31&nbsp;MB</div>
          </div>
        </div>
      </v-col>
    </v-row>

    <v-row algin="center" justify="center" no-gutters class="h-72">
      <v-col
        cols="2"
        offset="1"
        class="border border-neutral-50 border-b-0 border-r-0"
      >
        <v-row class="h-52 w-full h-full pa-0 ma-0">
          <v-col
            cols="12"
            class="border border-neutral-50 border-t-0 border-l-0 border-r-0"
          >
          </v-col>
        </v-row>
        <div class="tender-btn h-full w-full">
          <nuxt-link to="/"> </nuxt-link>
        </div>
      </v-col>
      <v-col cols="2" class="border border-neutral-50 border-b-0 border-r-0">
        <div class="diagonal-container to-right"></div>
      </v-col>
      <v-col cols="2" class="border border-neutral-50 border-b-0 border-r-0">
        <div class="diagonal-container to-right"></div>
      </v-col>
      <v-col cols="2" class="border border-neutral-50 border-b-0">
        <v-row class="h-48 w-full h-full pa-0 ma-0">
          <v-col
            cols="12"
            class="border border-neutral-50 border-t-0 border-l-0 border-r-0 border-b-0"
          >
          </v-col>
        </v-row>
        <p class="copyright w-full text-center">© 2011 - 2022 OGK Group</p>
      </v-col>
    </v-row>
  </div>
</template>
<script>
export default {
  data() {
    return {
      menuContainer: null,
    }
  },
  props: {
    show: {
      default: false,
      required: true,
      type: Boolean,
    },
  },
}
</script>
<style scoped>
.menu-container {
  position: absolute;
  top: 0%;
  left: 0%;
  opacity: 1;
  z-index: 100000;
  visibility: visible;
  background-color: #333333;
}
div.diagonal-container {
  border: none;
  outline: none;
  width: 100%;
  height: 100%;
  margin: 0 auto;
}

.to-left {
  background: linear-gradient(
    19deg,
    transparent calc(50% - 1px),
    rgba(250, 250, 250, 0.105) 50%,
    transparent calc(50% + 1px)
  );
}

.to-right {
  background: linear-gradient(
    -225.5deg,
    transparent calc(50% - 1px),
    rgba(250, 250, 250, 0.105) 50%,
    transparent calc(50% + 1px)
  );
}

.link-container .nuxt-link-active {
  color: #ffffff !important;
  transition: 0.3s cubic-bezier(0.175, 0.885, 0.32, 1.275);
  font-family: Metronic, sans-serif;
  font-weight: 600;
  line-height: 0.71;
  letter-spacing: 0.4px;
  text-transform: uppercase;
  font-size: 13px;
}
.link-container .nuxt-link-active:hover {
  color: #009a67 !important;
  transition: 0.3s cubic-bezier(0.175, 0.885, 0.32, 1.275);
}
.menu-hover::before {
  content: 'CLOSE';
  position: absolute;
  font-family: 'MetronicPro';
  font-weight: bold;
  top: 0;
  left: 0;
  z-index: 30;
  opacity: 1;
  transition: 0.5s cubic-bezier(0.175, 0.885, 0.32, 1.275);
}
.menu-hover::after {
  content: 'CLOSE';
  position: absolute;
  left: 0;
  bottom: -5rem;
  z-index: 30;
  opacity: 0;
  transition: 0.5s cubic-bezier(0.175, 0.885, 0.32, 1.275);
}
.about-group-container .nuxt-link-active:hover {
  color: #009a67 !important;
  transition: 0.3s cubic-bezier(0.175, 0.885, 0.32, 1.275);
}
.link-container .link-active {
  color: #009a67 !important;
  cursor: auto;
}
.services-container,
.about-group-container {
  padding: 3rem !important;
}
.services-container h1,
.about-group-container h1 {
  color: #ffffff !important;
  font-size: 14px !important;
  font-family: MetronicPro-Bold !important;
  letter-spacing: 0.4px !important;
}
.services-container .services,
.about-group-container .about-links {
  margin-top: 1rem !important;
}
.services-container .services .nuxt-link-active:hover {
  color: #009a67 !important;
}
.services-container .services .nuxt-link-active,
.about-group-container .about-links .nuxt-link-active {
  color: rgba(255, 255, 255, 0.3) !important;
  transition: 0.3s ease !important;
  cursor: pointer;
  font-family: Metronic, sans-serif;
  font-weight: 600;
  line-height: 0.71;
  letter-spacing: 0.4px;
  text-transform: uppercase;
  font-size: 13px;
  line-height: 38px;
  margin-right: 32px;
  color: rgba(255, 255, 255, 0.3);
  white-space: nowrap;
}
.download-section {
  position: absolute;
  top: 50%;
  -webkit-transform: translate3d(0, -50%, 0);
  transform: translate3d(0, -50%, 0);
  font-size: 0;
  white-space: nowrap;
  transition: all 0.5s cubic-bezier(0.215, 0.61, 0.355, 1);
  cursor: pointer;
}
.download-section .text {
  display: inline-block;
  vertical-align: top;
  color: #fff;
  padding-top: 14px;
}
.download-section .text .title {
  font-family: Metronic, sans-serif;
  font-weight: 500;
  line-height: 0.71;
  letter-spacing: 0.4px;
  text-transform: uppercase;
  font-size: 14px !important;
  line-height: 1.43;
}
.download-section .text .cap {
  font-size: 14px !important;
  line-height: 1.57;
  margin-top: 2px;
  opacity: 0.5;
  transition: all 0.5s cubic-bezier(0.215, 0.61, 0.355, 1);
}
.download-section:hover {
  background-color: #009a67;
  transition: all 0.5s cubic-bezier(0.215, 0.61, 0.355, 1);
}
.copyright {
  position: absolute;
  font-size: 14px;
  line-height: 1.57;
  color: rgba(255, 255, 255, 0.5);
  width: 100%;
  text-align: center;
  bottom: 24px;
}
.tender-btn {
  position: relative;
  width: 100%;
  height: 100% !important;
  opacity: 1;
  display: flex;
  align-items: flex-start !important;
  justify-content: center !important;
  text-align: center;
}
.tender-btn .nuxt-link-active::before {
  content: 'TENDER PLATFORM';
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  padding-top: 2rem;
  height: 100% !important;
  text-align: center;
  font-family: Metronic, sans-serif;
  font-weight: 600;
  letter-spacing: 0.4px;
  text-transform: uppercase;
  z-index: 5;
  font-size: 13px;
  line-height: 1em;
  z-index: 20;
  -webkit-transition: 0.3s ease;
  transition: 0.3s ease;
  color: #ffffff;
  transition: all 0.5s cubic-bezier(0.215, 0.61, 0.355, 1);
}
.tender-btn .nuxt-link-active::after {
  content: 'TENDER PLATFORM';
  position: absolute;
  top: 50%;
  left: 0;
  width: 100%;
  padding-top: 2rem;
  height: 100% !important;
  text-align: center;
  font-family: Metronic, sans-serif;
  font-weight: 600;
  letter-spacing: 0.4px;
  text-transform: uppercase;
  z-index: 5;
  font-size: 13px;
  line-height: 1em;
  z-index: 20;
  -webkit-transition: 0.3s ease;
  transition: 0.3s ease;
  color: #ffffff;
  transition: all 0.5s cubic-bezier(0.215, 0.61, 0.355, 1);
  background-color: #3d3d3d;
}
.tender-btn:hover .nuxt-link-active::after {
  top: 0% !important;
  transition: all 0.5s cubic-bezier(0.215, 0.61, 0.355, 1);
}
.tender-btn:hover .nuxt-link-active::before {
  top: -6% !important;
  opacity: 0 !important;
  transition: all 0.5s cubic-bezier(0.215, 0.61, 0.355, 1);
}
</style>