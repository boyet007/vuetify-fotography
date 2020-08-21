<template>
    <v-main>
        <Hero />
        <Gallery />
        <LatestPost />
    </v-main>
</template>

<script>
import Hero from '../components/Hero.vue'
import Gallery from '../components/Gallery.vue'
import LatestPost from '../components/LatestPost.vue'
export default {
    name: 'Home',
    components: {
        Hero, Gallery, LatestPost,
    }
}
</script>
