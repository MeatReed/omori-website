<template>
  <div>
    <v-img class="header" height="90" width="100%">
      <img
        class="header_title"
        src="/header_title.png"
        max-height="96"
        max-width=""
      />
    </v-img>
    <div class="header">
      <v-container>
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
      </v-container>
    </div>
  </div>
</template>

<script>
export default {}
</script>

<style></style>
