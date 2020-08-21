<template>
  <div class="container latest-post">
    <h2>Latest Post</h2>
    <v-row>
      <v-col xs='12' sm='6' md='4' v-for="item in items" :key="item.id">
         <v-card flat
          class="mx-auto"
        >
        <v-img
          class="white--text align-end"
          height="200px"
          :src="item.src"
        >
          <v-card-title>{{ item.title }}</v-card-title>
        </v-img>

        <v-card-subtitle class="pb-0">{{ item.subtitle }}</v-card-subtitle>

        <v-card-text class="text--primary">
          <div>{{ item.description }}</div>
        </v-card-text>

        <v-card-actions>
          <v-btn
            text
          >
            More
          </v-btn>
        </v-card-actions>
      </v-card>
      </v-col>
    </v-row>
  </div>
</template>

<script>
  export default {
    name: 'LatestPost',
    data: () => ({
      items: [
        {
          id: 1, 
          title: 'The Wind and The Winter', 
          subtitle: 'Honour with the scenery beautiful',
          description: `Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.`,
          src: require('../assets/images/gallery/photo01.jpg'),
        },
        {
          id: 2, 
          title: 'Beauty Panorama', 
          subtitle: 'Enjoy yourself with beauty scenery',
          description: `Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.`,
          src: require('../assets/images/gallery/photo02.jpg'),
        },
        {
          id: 3, 
          title: 'Experience The Glamour', 
          subtitle: 'Enjoy Family Day with the unforgettable moment',
          description: `Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.`,
          src: require('../assets/images/gallery/photo03.jpg'),
        },
      ],
    }),
  }
</script>
