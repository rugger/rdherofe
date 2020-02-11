<template>
    <div class="LandingLogin">
      <h1 class="radio-hero-text">
        I'm A Radio Hero!
      </h1>
      <v-img
        class="mx-auto pb-3"
        src="images/SoldogMedia-logo.png"
        width="175px"
        contain
      >

      </v-img>
      <v-card
        max-width="400"
        min-width="375"
        class="pa-1"
        flat
      >
        <v-card-title>
        <h2 class="orange--text text-center">
          Login to your account
        </h2>
        </v-card-title>
        <v-card-text>
        <v-form
          ref="form"
          lazy-validation
        >
          <v-text-field
            v-model="name"
            :counter="20"
            :rules="nameRules"
            label="User Name"
            required
            prepend-icon="mdi-account-circle"
          >

          </v-text-field>

          <v-text-field
            v-model="password"
            :rules="passwordRules"
            label="Password"
            required
            :type="showPassword ? 'text' : 'password'"
            prepend-icon="mdi-lock"
            :append-icon="showPassword ? ' mdi-eye' : 'mdi-eye-off'"
            @click:append="showPassword = !showPassword"
          >

          </v-text-field>
        </v-form>
        </v-card-text>
        <v-divider></v-divider>
        <v-card-actions>
          <v-btn
            class="ml-9"
            color="orange darken-2"
            href="home"
          >
            Login
          </v-btn>
          <v-spacer></v-spacer>
          <v-chip
            color="orange lighten-2"
            href="welcome"
            link
            nuxt
            small
          >
            <v-avatar left>
              <v-icon color="grey darken-2">
                mdi-help-circle
              </v-icon>
            </v-avatar>
            Forgot Password
          </v-chip>
        </v-card-actions>
      </v-card>
      <v-card
        max-width="450"
        min-width="350"
        class="mt-3"
        flat
      >
        <h4 class="black--text header text-center">
          Don't have a login? <a :href="pdemail">
          Contact {{ loginContact }}
        </a>
        </h4>
      </v-card>
    </div>
</template>

<script>
    export default {
      name: "LandingLogin",
        props: {
        },
      data () {
        return {
          loginContact: "Engineering",
          pdemail: "mailto://john@soldogmedia.ca",
          devurl: "https://soldogmedia.ca",
          showPassword: false
        }
      },
    };
</script>
<style scoped>
  .radio-hero-text {
    color: ghostwhite;
    text-align: center;
  }
</style>
