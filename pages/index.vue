<template>
  <div class="main fill-height pa-8">
    <v-row no-gutters>
      <v-col cols="8">
        <v-row no-gutters>
          <v-col
            cols="3"
            v-for="(button, index) in buttonsList"
            :key="index"
            class="pr-8"
          >
            <button-statistic :item="button" />
          </v-col>
        </v-row>

      </v-col>
      <v-col cols="4">
        <calendar/>
      </v-col>
    </v-row>
    <v-row no-gutters>
      <v-col cols="4">
        <clients-list :newClients="newClients"/>
      </v-col>
      <v-col cols="8">
        234
      </v-col>
    </v-row>
  </div>
</template>

<script>
import ButtonStatistic from '~/components/ButtonStatistic.vue'
import Calendar from '~/components/Calendar.vue'
import ClientsList from '../components/ClientsList'

export default {
  data: () => ({
    buttonsList: [
      { title: 'Clients', icon: 'mdi-account-multiple', quantity: 128 },
      { title: 'Completed tasks', icon: 'mdi-clipboard-check', quantity: 32 },
      { title: 'Notifications', icon: 'mdi-bell', quantity: 2 },
      { title: 'Reports', icon: 'mdi-alert-octagon', quantity: 4 },
    ],
    newClients: [
      {
        name: 'Nicci Troiani',
        location: 'Chicago, IL',
        photo: 'https://randomuser.me/api/portraits/women/90.jpg'
      },
      {
        name: 'George Fields',
        location: 'New York, NY',
        photo: 'https://randomuser.me/api/portraits/men/70.jpg'
      },
      {
        name: 'Jones Dermot',
        location: 'San Francisco, CA',
        photo: 'https://randomuser.me/api/portraits/men/11.jpg'
      },
      {
        name: 'Jane Doe',
        location: 'New York, NY',
        photo: 'https://randomuser.me/api/portraits/women/67.jpg'
      },
    ]
  }),
  components: {
    ClientsList,
    ButtonStatistic,
    Calendar
  }
}
</script>

<style lang="scss" scoped>

</style>
