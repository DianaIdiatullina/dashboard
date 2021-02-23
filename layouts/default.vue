<template>
  <v-app>
    <header-component/>
    <v-main>
      <v-container>
        <nuxt />
      </v-container>
    </v-main>
  </v-app>
</template>

<script>
  import HeaderComponent from '~/components/HeaderComponent.vue'

  export default {
    components: {
      HeaderComponent
    }
  }
</script>
