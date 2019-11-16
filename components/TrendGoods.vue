<template>
  <div>
    <v-row class="ml-4">
      <v-col>
        <v-row class="mb-2">
          <span class="normal-title-light">秋冬最新品</span>
        </v-row>
        <v-row>
          <div class="my-2">
            <v-btn large outlined>
              <v-icon left>mdi-subdirectory-arrow-right</v-icon>去逛街
              </v-btn>
          </div>
        </v-row>
        <v-row>
          <v-img src="https://picsum.photos/id/20/500/300" lazy-src="https://picsum.photos/id/15/10/6" spect-ratio="1" class="grey lighten-2">
            商品類型示意圖
          </v-img>
        </v-row>
      </v-col>
      <v-col>
        <v-row>
          <preview-product></preview-product>
          <preview-product></preview-product>
        </v-row>
      </v-col>
    </v-row>
  </div>
</template>

<script>
  import PreviewProduct from './PreviewProduct'

  export default {
    name: 'TrendGoods',
    components: {
      PreviewProduct
    }
  }
</script>