<template>
  <v-app>
    <Header />
    <v-main :style="styleBackgroundImage">
      <nuxt />
    </v-main>
    <v-footer app color="black" height="96">
      <v-col class="text-center" cols="12">
        {{ new Date().getFullYear() }} —
        <strong
          ><a
            href="https://github.com/MeatReed/omori-website"
            target="_blank"
            rel="noopener noreferrer"
            >Github</a
          ></strong
        >
      </v-col>
    </v-footer>
  </v-app>
</template>

<script>
export default {
  data() {
    return {
      styleBackgroundImage: {
        'background-image': 'url(/omoriwebgif2-w1200.gif)',
      },
      images: [
        '/omoriwebgif1-w1200.gif',
        '/omoriwebgif2-w1200.gif',
        '/omoriwebgif3-w1200.gif',
        '/omoriwebgif4-w1200.gif',
        '/omoriwebgif5-w1200.gif',
        '/omoriwebgif6-w1200.gif',
        '/omoriwebgif7-w1200.gif',
        '/omoriwebgif8-w1200.gif',
        '/omoriwebgif9-w1200.gif',
        '/omoriwebgif10-w1200.gif',
        '/omoriwebgif11-w1200.gif',
      ],
    }
  },
  watch: {
    $route() {
      this.styleBackgroundImage = {
        'background-image': `url(${
          this.images[Math.floor(Math.random() * this.images.length)]
        })`,
      }
    },
  },
}
</script>

<style>
.v-main {
  width: 100%;
  height: 100%;
  background-repeat: no-repeat;
  background-position: center center;
  background-size: cover;
  position: fixed;
  top: 0;
  left: 0;
  z-index: 1;
}

@font-face {
  font-family: 'OMORI_GAME2';
  src: local('OMORI_GAME2'),
    url(~assets/fonts/OMORI_GAME2.ttf) format('truetype');
  font-family: 'OMORI_GAME';
  src: local('OMORI_GAME'), url(~assets/fonts/OMORI_GAME.ttf) format('truetype');
}

h1 {
  font-family: 'OMORI_GAME2';
  font-size: 50px;
}

p {
  font-family: 'OMORI_GAME2';
  font-size: 30px;
}

.v-sheet.v-footer {
  border-top: 1px solid rgb(255, 255, 255) !important;
}

.v-main__wrap {
  padding-top: 138px !important;
}

.header_title {
  width: auto;
  height: 89px;
  padding: 12px 0px;
  display: inline-block;
}

.v-app-bar {
  margin-top: 90px !important;
}

.v-tabs {
  border-top: 1px solid rgb(255, 255, 255);
  border-bottom: 1px solid rgb(255, 255, 255);
}

.header {
  position: fixed;
  top: 0;
  left: 0;
  z-index: 200;
  text-align: center;
  background: url(/header_static.gif) center center repeat !important;
}

.v-tab:hover .eye_active {
  display: block;
}

.v-tab:hover {
  padding-left: 0px;
}

.v-tab {
  padding-left: 62px;
}

.v-tab .eye_active {
  display: none;
}

.tab-active {
  padding-left: 0px;
}

.tab-active .eye_active {
  display: block;
}

.theme--dark.v-tabs .v-tab:hover::before {
  opacity: 0;
}

.theme--dark.v-tabs .v-tab--active:hover::before,
.theme--dark.v-tabs .v-tab--active::before {
  opacity: 0;
}
</style>
