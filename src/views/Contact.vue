<template>
    <v-main>
        <div>
            <v-img :aspect-ratio="16/3" :src="imgContact">
                <v-row align="end" class="lightbox white--text pa-2 fill-height">
                    <v-col>
                        <v-container>
                            <div class="headline">Contact</div>
                        </v-container>
                    </v-col>
                </v-row>
            </v-img>
        </div>
        <div class="block py-10">
            <v-form
            ref="form"
            v-model="valid"
            lazy-validation
        >
            <v-text-field
            v-model="name"
            :counter="10"
            :rules="nameRules"
            label="Name"
            required
            ></v-text-field>

            <v-text-field
            v-model="email"
            :rules="emailRules"
            label="E-mail"
            required
            ></v-text-field>

            <v-textarea
            v-model="messages"
            :rules="messageRules"
            label="Messages"
            hint="Hint text"
            required
            ></v-textarea>

            <v-btn
            :disabled="!valid"
            color="success"
            class="mr-4"
            @click="validate"
            >
            Submit
            </v-btn>

            <v-btn
            color="error"
            class="mr-4"
            @click="reset"
            >
            Reset
            </v-btn>
        </v-form>
        </div>
        <div class="google-maps">
            <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d1982.9224699227361!2d106.94156499981271!3d-6.284104656355445!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x2e698d6f4f6116d7%3A0x17108c375994d6e6!2sJatikramat%20Jatiasih%20Bekasi!5e0!3m2!1sen!2sid!4v1598021315131!5m2!1sen!2sid" width="100%" height="400" frameborder="0"></iframe>
        </div>
    </v-main>
</template>

<script>
export default {
    name: 'Contact',
    data: () => ({
        imgContact: require('../assets/images/photo05.jpg'),
        valid: true,
        name: '',
        nameRules: [
            v => !!v || 'Name is required',
            v => (v && v.length <= 10) || 'Name must be less than 10 characters',
        ],
        email: '',
        emailRules: [
            v => !!v || 'E-mail is required',
            v => /.+@.+\..+/.test(v) || 'E-mail must be valid',
        ],
        messages: '',
        messageRules: [
            v => !!v || 'Nessages is required',
        ],
    }),
    methods: {
      validate () {
        this.$refs.form.validate()
      },
      reset () {
        this.$refs.form.reset()
      }
    },
}
</script>
