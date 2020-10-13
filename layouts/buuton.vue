<template>
  <v-app dark>
    <div>
      <div class="ma-0 pa-0">
        <template>
          <v-toolbar
            dark
            src="https://cdn.vuetifyjs.com/images/parallax/material.jpg"
          >
            <v-app-bar-nav-icon @click.stop="drawer = !drawer" />
          </v-toolbar>
          <v-card>
            <v-navigation-drawer permanent expand-on-hover>
              <v-navigation-broder permanent expand-on-hover>
                <v-list>
                  <v-list-item class="px-2">
                    <v-list-item-avatar>
                      <v-img
                        src="https://randomuser.me/api/portraits/women/85.jpg"
                      />
                    </v-list-item-avatar>
                  </v-list-item>

                  <v-list-item link>
                    <v-list-item-content>
                      <v-list-item-title class="title">
                        Sandra Adams
                      </v-list-item-title>
                      <v-list-item-subtitle>
                        sandra_a88@gmail.com
                      </v-list-item-subtitle>
                    </v-list-item-content>
                  </v-list-item>
                </v-list>

                <v-divider />

                <v-list nav dense>
                  <v-list-item link>
                    <v-list-item-icon>
                      <v-icon>mdi-folder</v-icon>
                    </v-list-item-icon>
                    <v-list-item-title>My Files</v-list-item-title>
                  </v-list-item>
                  <v-list-item link>
                    <v-list-item-icon>
                      <v-icon>mdi-account-multiple</v-icon>
                    </v-list-item-icon>
                    <v-list-item-title>Shared with me</v-list-item-title>
                  </v-list-item>
                  <v-list-item link>
                    <v-list-item-icon>
                      <v-icon>mdi-star</v-icon>
                    </v-list-item-icon>
                    <v-list-item-title>Starred</v-list-item-title>
                  </v-list-item>
                </v-list>
              </v-navigation-broder>
            </v-navigation-drawer>
          </v-card>
        </template>
      </div>
    </div>
  </v-app>
</template>

<script>
export default {
  data () {
    return {
      clipped: false,
      drawer: false,
      fixed: false,
      items: [],
      model: 0,
      colors: ['primary', 'secondary', 'yellow darken-2', 'red', 'orange']
    }
  }
}
</script>

<style>
</style>
