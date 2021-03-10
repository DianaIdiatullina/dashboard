<template>
  <v-app>
    <nav-component/>

    <v-main>
      <div class="pa-0 ma-0">
        <nuxt />
      </div>
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
  .v-main {
    padding-left: 256px !important;
  }
</style>
