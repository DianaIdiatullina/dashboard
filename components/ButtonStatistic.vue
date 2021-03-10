<template>
  <div class="button-statistic pt-5 px-5 pb-4">
    <div class="text-center">
      <v-icon size="48">
        {{ item.icon }}
      </v-icon>
    </div>
    <div class="button-statistic__quantity text-center">
      {{ item.quantity }}
    </div>
    <div class="button-statistic__title text-center text-truncate">
      {{ item.title }}
    </div>
  </div>
</template>

<script>
  export default {
    props: {
      item: Object
    }
  }
</script>

<style lang="scss" scoped>
.button-statistic {
  background: #212936;
  border: 1px solid #313C4E;
  border-radius: 4px;
  cursor: pointer;

  .v-icon {
    color: #56657F;
  }

  &__quantity {
    color: #8997B1;
    font-size: 24px;
    line-height: 36px;
    padding: 2px 0;
  }

  &__title {
    font-size: 12px;
    line-height: 15px;
    letter-spacing: 0.4px;
    color: #56657F;
  }

  &:hover {
    background-color: #00BCD4;
    box-shadow: 0 3px 5px rgba(0, 0, 0, 0.2), 0 1px 18px rgba(0, 0, 0, 0.12), 0 6px 10px rgba(0, 0, 0, 0.14);

    .v-icon {
      color: #fff;
    }

    .button-statistic__title {
      color: rgba(255, 255, 255, 0.7);
    }

    .button-statistic__quantity {
      color: #fff;
    }
  }
}
</style>
