<template>
  <v-app>
    <v-navigation-drawer
      v-model="drawer"
      :mini-variant="miniVariant"
      :clipped="clipped"
      fixed
      app
      src="https://i.imgur.com/fbOiPGH.jpg"
    >
      <v-navigation-broder permanent expand-on-hover>
        <v-list>
          <v-list-item class="px-2" justify="center">
            <v-list-item-avatar>
              <v-img
                src="https://randomuser.me/api/portraits/women/85.jpg"
              />
            </v-list-item-avatar>
          </v-list-item>

          <v-list-item link>
            <v-list-item-content>
              <v-list-item-title class="title">
                Robert Armserdam
              </v-list-item-title>
              <v-list-item-subtitle>
                Robert_Armserdam202@gmail.com
              </v-list-item-subtitle>
            </v-list-item-content>
          </v-list-item>
        </v-list>

        <v-divider />

        <v-list nav dense>
          <v-list-item link>
            <v-list-item-icon>
              <v-icon>mdi-badge-account-horizontal</v-icon>
            </v-list-item-icon>
            <v-list-item-title>My Profile</v-list-item-title>
          </v-list-item>
          <v-list-item link>
            <v-list-item-icon>
              <v-icon>mdi-comment-processing-outline</v-icon>
            </v-list-item-icon>
            <v-list-item-title>Messenger</i></v-list-item-title>
          </v-list-item>
          <v-list-item link>
            <v-list-item-icon>
              <v-icon>mdi-logout</v-icon>
            </v-list-item-icon>
            <v-list-item-title>Log Out</v-list-item-title>
          </v-list-item>
        </v-list>
      </v-navigation-broder>
      </v-card>
    </v-navigation-drawer>
    <v-app-bar
      absolute
      color="#fcb69f"
      src="https://i.imgur.com/sD33gxz.jpg"
      app
    >
      <v-app-bar-nav-icon @click.stop="drawer = !drawer" />
      <h1>Market Place</h1>
      <v-spacer />
    </v-app-bar>
    <v-main>
      <v-container>
        <nuxt />
        <br>
      </v-container>
    </v-main>
    <v-navigation-drawer v-model="rightDrawer" :right="right" temporary fixed />
    <v-footer :absolute="!fixed" app />
  </v-app>
</template>
<script>
export default {
  data () {
    return {
      clipped: false,
      drawer: false,
      fixed: false,
      items: [
        {
          icon: 'mdi-database-search',
          title: 'Search',
          to: '/'
        },
        {
          icon: 'mdi-account',
          title: 'About Me',
          to: '/about'
        }
      ],
      miniVariant: false,
      right: true,
      rightDrawer: false
    }
  }
}
</script>
