<template>
  <v-list
    two-line
    class="clients-list"
  >
    <v-subheader class="clients-list__title">New Clients</v-subheader>
    <v-list-item
      v-for="client in newClients"
      :key="client.name"
    >
      <v-list-item-avatar>
        <img :src="client.photo">
      </v-list-item-avatar>

      <v-list-item-content>
        <v-list-item-title v-text="client.name"></v-list-item-title>

        <v-list-item-subtitle v-text="client.location"></v-list-item-subtitle>
      </v-list-item-content>

      <v-list-item-action>
        <v-btn icon>
          <v-icon>mdi-dots-vertical</v-icon>
        </v-btn>
      </v-list-item-action>
    </v-list-item>

  </v-list>
</template>

<script>
  export default {
    props: {
      newClients: Array
    }
  }
</script>

<style lang="scss" scoped>
.clients-list {
  background: #212936;
  border: 1px solid #313C4E;
  border-radius: 4px;

  &__title {
    color: #AFBDD1;
    font-weight: 500;
    font-size: 20px;
    letter-spacing: 0.15px;
  }

  .v-icon {
    color: #56657F;
  }
}
</style>
