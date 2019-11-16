<template>
  <v-content>
    <v-container class="fill-height" fluid>
      <v-row align="start" justify="center">
        <v-col>
          <good-carousel></good-carousel>
        </v-col>
        <v-col>
          <v-row class="mb-2">
            <v-img src="https://picsum.photos/id/11/500/300" lazy-src="https://picsum.photos/id/11/10/6"
            aspect-ratio="1" class="grey lighten-2" max-height="246">
              <v-row align="end" class="lightbox white--text pa-2 fill-height" style="font-size: 20px;">
                <v-col>
                  <span>優惠專區</span>
                </v-col>
              </v-row>
            </v-img>
          </v-row>
          <v-row class="mt-2">
            <v-img src="https://picsum.photos/id/15/500/300" lazy-src="https://picsum.photos/id/15/10/6"
              aspect-ratio="1" class="grey lighten-2" max-height="246">
              <v-row align="end" class="lightbox white--text pa-2 fill-height" style="font-size: 20px;">
                <v-col>
                  <span>活動專區</span>
                </v-col>
              </v-row>
            </v-img>
          </v-row>
        </v-col>
      </v-row>
      <v-row class="mt-10">
        <p class="font-weight-black ml-4 big-title-light">熱門商品</p>
      </v-row>
      <trend-goods></trend-goods>
      <trend-goods></trend-goods>
      <trend-goods></trend-goods>
    </v-container>
  </v-content>
</template>

<script>
  import GoodCarousel from '~/components/GoodCarousel'
  import TrendGoods from '~/components/TrendGoods'

  export default {
    name: 'home',
    components: {
        GoodCarousel, TrendGoods
    },
  }
</script>
