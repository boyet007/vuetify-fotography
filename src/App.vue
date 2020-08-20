<template>
  <v-app>
    <v-app-bar color="primary"
      app flat
    >
        <Header /> 
    </v-app-bar>

    <v-main>
      <Hero />
    </v-main>
  </v-app>
</template>

<script>
import Header from './components/Header';
import Hero from './components/Hero';

export default {
  name: 'App',

  components: {
    Header, Hero
  },

  data: () => ({
    //
  }),
};
</script>
