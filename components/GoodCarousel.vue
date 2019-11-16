<template>
  <v-carousel cycle hide-delimiter-background show-arrows-on-hover>
    <v-carousel-item v-for="(slide, i) in slides" :key="i" :src=slide>
    </v-carousel-item>
  </v-carousel> 
</template>

<script>
export default {
    name: 'GoodCarousel',
    data () {
      return {
        colors: [ 
          'primary',
          'secondary',
          'yellow darken-2',
          'red',
          'orange',
        ],
        slides: [
          'https://fakeimg.pl/800x600/880000/?text=edge 122',
          'https://fakeimg.pl/800x600/800988/?text=edge 300',
          'https://fakeimg.pl/800x600/000999/?text=ranger 100',
          'https://fakeimg.pl/800x600/004400/?text=ranger 120',
          'https://fakeimg.pl/800x600/005599/?text=ranger 130',
        ],
      }
    },
  }
</script>