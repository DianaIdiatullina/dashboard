<template>
  <v-app>
    <nav-component/>

    <v-main class="pa-0">
      <v-container class="pa-0">
        <nuxt />
      </v-container>
    </v-main>
  </v-app>
</template>

<script>
  import NavComponent from '~/components/NavComponent.vue'

  export default {
    components: {
      NavComponent
    }
  }
</script>

<style lang="scss">
</style>
