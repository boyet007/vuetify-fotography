<template>
      <v-carousel>
    <v-carousel-item
      v-for="(item,i) in items"
      :key="i"
      :src="item.src"
      reverse-transition="fade-transition"
      transition="fade-transition"
    ></v-carousel-item>
  </v-carousel>
</template>

<script>
  export default {
    data: () => ({
        items: [
          {
            src: require('../assets/images/photo01.jpg'),
          },
          {
            src: require('../assets/images/photo02.jpg'),
          },
          {
            src: require('../assets/images/photo03.jpg'),
          },
          {
            src: require('../assets/images/photo04.jpg'),
          },
        ],
    }),
  }
</script>
