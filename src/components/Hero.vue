<template>
  <div class="hero-block">
    <v-carousel hide-delimiters cycle>
      <v-carousel-item
        v-for="(item,i) in items"
        :key="i"
        :src="item.src"
        reverse-transition="fade-transition"
        transition="fade-transition"
      >
        <v-row
            class="fill-height title"
            align="center"
            justify="center"
          >
            <div class="display-3 hidden-xs-only">{{ item.title }}</div>
        </v-row>
      </v-carousel-item>
  </v-carousel>
  </div>
</template>

<script>
  export default {
    data: () => ({
        items: [
          {
            src: require('../assets/images/photo01.jpg'),
            title: 'We Are Professional',
          },
          {
            src: require('../assets/images/photo02.jpg'),
            title: 'The Beautiful Of Scenery',
          },
          {
            src: require('../assets/images/photo03.jpg'),
            title: 'High Technology',
          },
          {
            src: require('../assets/images/photo04.jpg'),
            title: 'Passion With Your Style',
          },
        ],
    }),
  }
</script>
