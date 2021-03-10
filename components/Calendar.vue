<template>
  <div class="calendar">
    <v-date-picker
      v-model="date"
      first-day-of-week="1"
      :weekday-format="weekDay"
      color="#00BCD4"
      locale="en-En"
      no-title
      full-width
    ></v-date-picker>
  </div>
</template>

<script>
  export default {
    data () {
      return {
        date: new Date().toISOString().substr(0, 10),
      }
    },
    methods: {
      weekDay(date) {
        return new Date(date).toLocaleString('en-En', { weekday: 'short' });
      }
    }
  }
</script>

<style lang="scss">
.calendar {
  .theme--dark.v-picker__body {
    background-color: #212936;
  }

  .v-date-picker-table--date .v-btn {
    height: 48px;
    width: 48px;
    font-size: 16px;
    letter-spacing: 0.15px;
    font-weight: 400;
    color: #AFBDD1;
  }

  .v-date-picker-table {
    height: 100%;
    padding-bottom: 24px;
  }

  .theme--dark .v-date-picker-header__value button {
    color: #AFBDD1 !important;
    font-weight: 500;
    font-size: 14px;
    line-height: 21px;
    letter-spacing: 0.1px;
  }

  .v-date-picker-header {
    padding: 24px 16px 16px 16px;

    .v-icon {
      color: #8997B1;
    }
  }

  .v-date-picker-table--date th {
    font-size: 12px;
    letter-spacing: 0.4px;
    color: #313C4E;
  }
}
</style>
