<template>
  <v-app>
    <Header />
    <v-main>
      <nuxt />
    </v-main>
    <v-footer app color="black" height="96">
      <v-col class="text-center" cols="12">
        {{ new Date().getFullYear() }} — <strong>Footer</strong>
      </v-col>
    </v-footer>
  </v-app>
</template>

<script>
export default {
  data() {
    return {}
  },
}
</script>

<style>
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

.v-main__wrap {
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

.v-footer {
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
