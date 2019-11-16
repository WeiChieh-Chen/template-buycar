<template>
  <v-col>
    <v-img src="https://picsum.photos/id/25/500/300" lazy-src="https://picsum.photos/id/25/10/6" spect-ratio="1" class="grey lighten-2">
      商品示意圖
    </v-img>
    <i class="fas fa-heart"></i>

    <span class="ml-4">234</span><br>
    <span>dddddd</span>
  </v-col>
</template>

<script>
  export default {
    name: 'PreviewProduct',
    data() {
      return {
        heartClick: false
      }
    }
  }
</script>
