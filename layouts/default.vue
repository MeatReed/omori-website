<template>
  <v-app>
    <v-img class="header" height="90" width="100%">
      <img
        class="header_title"
        src="/header_title.png"
        max-height="96"
        max-width=""
      />
    </v-img>
    <div class="header">
      <v-app-bar app dense flat color="black">
        <v-tabs centered hide-slider active-class="tab-active">
          <v-tab nuxt to="/" :ripple="false">
            <img class="eye_active" src="/nav_active.gif" alt="" />
            <img src="/nav_about.png" alt="" />
          </v-tab>
          <v-tab nuxt to="/story" :ripple="false">
            <img class="eye_active" src="/nav_active.gif" alt="" />
            <img src="/nav_story.png" alt="" />
          </v-tab>
          <v-tab nuxt to="/music" :ripple="false">
            <img class="eye_active" src="/nav_active.gif" alt="" />
            <img src="/nav_music.png" alt="" />
          </v-tab>
          <v-tab nuxt to="/gallery" :ripple="false">
            <img class="eye_active" src="/nav_active.gif" alt="" />
            <img src="/nav_gallery.png" alt="" />
          </v-tab>
          <v-tab nuxt to="/updates" :ripple="false">
            <img class="eye_active" src="/nav_active.gif" alt="" />
            <img src="/nav_updates.png" alt="" />
          </v-tab>
          <v-tab nuxt to="/team" :ripple="false">
            <img class="eye_active" src="/nav_active.gif" alt="" />
            <img src="/nav_team.png" alt="" />
          </v-tab>
        </v-tabs>
      </v-app-bar>
    </div>
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
