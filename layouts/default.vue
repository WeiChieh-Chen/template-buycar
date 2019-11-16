<template>
  <v-app dark>
    <v-navigation-drawer
      v-model="drawer"
      app
      clipped
    >
      <div class="ma-3">
        <v-app-bar-nav-icon @click.stop="drawer = !drawer" />超炫購物
      </div>
      <v-list dense>
        <v-list-item
          :key="i"
          :to="item.to"
          exact
          router
        v-for="(item, i) in items">
          <v-list-item-action>
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title>{{ item.title }}</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>

      <v-list dense v-if="login">
        <v-list-item link @click.stop="clickListItem('Buycar')">
          <v-list-item-action>
            <v-icon>mdi-cart</v-icon>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title>購物車</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>
      <v-list dense v-if="!login">
        <v-list-item link @click.stop="clickListItem('Login')">
          <v-list-item-action>
            <v-icon>mdi-account</v-icon>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title>登入</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>

    <v-card>
      <v-app-bar>
        <v-app-bar-nav-icon @click.stop="drawer = !drawer" />
        <v-toolbar-title>超炫購物</v-toolbar-title>
        <v-spacer></v-spacer>
        <span v-if="login" class="font-weight-black">歡迎 ocpanda</span>
        <v-tooltip bottom>
          <template v-slot:activator="{ on }">
            <v-btn icon v-on='on' @click.stop="login = !login">
              <v-icon>mdi-account</v-icon>
            </v-btn>
          </template>
          <span>{{ login? '登出' : '登入' }}</span>
        </v-tooltip>
        <v-tooltip bottom v-if="login">
          <template v-slot:activator="{ on }">
            <v-btn icon v-on='on'>
              <v-icon>mdi-cart</v-icon>
            </v-btn>
          </template>
          <span>購物車</span>
        </v-tooltip>
      </v-app-bar>

      <v-bottom-navigation
        grow
        color="teal"
      >
        <v-btn :to="item.to" v-for="item in items">
          <span>{{ item.title }}</span>
          <v-icon>{{ item.icon }}</v-icon>
        </v-btn>
      </v-bottom-navigation>
    </v-card>
    <nuxt />
  </v-app>
</template>
<script>
    export default {
        data() {
            return {
                drawer: false,
                login: false,
                items: [
                    {
                        icon: 'mdi-home',
                        title: '首頁',
                        to: '/home'
                    },
                    {
                        icon: 'mdi-shopping',
                        title: '商品',
                        to: '/products/goods'
                    },
                    {
                        icon: 'mdi-contact-mail',
                        title: '聯絡我們',
                        to: '/contact'
                    },
                ],
            }
        }
    }
</script>

<style scoped>

</style>
