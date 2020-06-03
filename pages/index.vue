<template>
  <v-row align="center" justify="center">
    <v-col cols="6">
      <v-card>
        <v-card-title class="headline">Nuxt-boilerplate</v-card-title>
        <v-card-text>
          <p>
            Lorem ipsum dolor sit amet, consectetur adipisicing elit. Aspernatur
            blanditiis corporis dicta esse est fuga fugit ipsa itaque labore
            natus neque nesciunt nisi, possimus quasi reiciendis rerum similique
            soluta voluptatum.
          </p>
          <p class="text-center">
            Lorem ipsum dolor sit amet, consectetur adipisicing elit. Aspernatur
            blanditiis corporis dicta esse est fuga fugit ipsa itaque labore
            natus neque nesciunt nisi, possimus quasi reiciendis rerum similique
            soluta voluptatum.
          </p>
          <div class="text-xs-right">
            <em><small>&mdash; RoscaS</small></em>
          </div>
          <hr class="my-3" />
          <a href="https://nuxtjs.org/" target="_blank">
            Nuxt Documentation
          </a>
          <br />
          <a href="https://github.com/nuxt/nuxt.js" target="_blank">
            Nuxt GitHub
          </a>
        </v-card-text>
        <v-card-actions>
          <v-spacer />
          <v-btn color="primary" @click="fetch">
            Axios
          </v-btn>
          <v-btn color="primary" nuxt to="/inspire">
            Inspire
          </v-btn>
        </v-card-actions>
      </v-card>
    </v-col>
  </v-row>
</template>

<script>

export default {
  methods: {
    fetch() {
      this.$axios.get("/articles")
      .then(r => console.log(r))
      .catch(e => console.log(e))
    }
  }
}
</script>
