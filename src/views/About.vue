<template>
    <v-main>
        <div>
            <v-img :aspect-ratio="16/3" :src="imgAbout">
                <v-row align="end" class="lightbox white--text pa-2 fill-height">
                    <v-col>
                        <v-container>
                            <div class="headline">About Me</div>
                        </v-container>
                    </v-col>
                </v-row>
            </v-img>
        </div>
        <div class="block">
            <v-container>
                <p>Contrary to popular belief, Lorem Ipsum is not simply random text. It has roots in a piece of classical Latin literature from 45 BC, making it over 2000 years old. Richard McClintock, a Latin professor at Hampden-Sydney College in Virginia, looked up one of the more obscure Latin words, consectetur, from a Lorem Ipsum passage, and going through the cites of the word in classical literature, discovered the undoubtable source. Lorem Ipsum comes from sections 1.10.32 and 1.10.33 of "de Finibus Bonorum et Malorum" (The Extremes of Good and Evil) by Cicero, written in 45 BC. This book is a treatise on the theory of ethics, very popular during the Renaissance. The first line of Lorem Ipsum, "Lorem ipsum dolor sit amet..", comes from a line in section 1.10.32.</p>
            </v-container>
        </div>
        <div class="our-teams">
            <v-container>
                <h2 class="text-center">Our Teams</h2>
                <v-row>
                    <v-col v-for="team in teams" :key="team.id" cols="4">
                      <v-card flat
                        class="mx-auto"
                    >
                        <v-img
                        class="white--text align-end"
                        height="300px"
                        :src="team.src"
                        >
                        </v-img>
                        <v-card-subtitle class="pb-0 text-center">{{ team.title }}</v-card-subtitle>
                        <v-card-text class="text--primary text-center" >
                        <div>{{ team.name }}</div>
                        </v-card-text>
                    </v-card>
                    </v-col>
                </v-row>
            </v-container>
        </div>
    </v-main>
</template>

<script>
export default {
    name: 'About',
    data: () => ({
        imgAbout: require('../assets/images/photo02.jpg'),
        teams: [
            { id: 1, src: require('../assets/images/teams/team01.jpg'), name: 'Priscilia Stevany', title: 'Web Designer' },
            { id: 2, src: require('../assets/images/teams/team02.jpg'), name: 'Vanicia', title: 'UI/UIX' },
            { id: 3, src: require('../assets/images/teams/team03.jpg'), name: 'Muhammad Fataha', title: 'Front End Programmer' },
        ]
    }),
}
</script>
