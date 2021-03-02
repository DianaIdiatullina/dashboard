<template>
  <v-navigation-drawer
    absolute
    permanent
    class="nav-drawer"
  >
    <template v-slot:prepend>
      <v-list-item two-line>
        <v-list-item-avatar>
          <img src="https://randomuser.me/api/portraits/men/17.jpg">
        </v-list-item-avatar>

        <v-list-item-content>
          <v-list-item-title class="nav-drawer__user">Aaron Young</v-list-item-title>
        </v-list-item-content>
      </v-list-item>
    </template>

    <v-divider></v-divider>

    <v-list
      dense
      class="menu-list px-2"
    >
      <v-list-item
        v-for="item in menuList"
        :key="item.title"
        class="px-2"
      >
        <v-list-item-icon>
          <v-icon>{{ item.icon }}</v-icon>
        </v-list-item-icon>

        <v-list-item-content>
          <v-list-item-title>{{ item.title }}</v-list-item-title>
        </v-list-item-content>
      </v-list-item>
    </v-list>

    <v-divider></v-divider>

    <v-list
      dense
      class="menu-list px-2"
    >
      <v-subheader>Settings</v-subheader>
      <v-list-item
        v-for="itemList in menuListSecond"
        :key="itemList.title"
        class="px-2"
      >
        <v-list-item-icon>
          <v-icon>{{ itemList.icon }}</v-icon>
        </v-list-item-icon>

        <v-list-item-content>
          <v-list-item-title>{{ itemList.title }}</v-list-item-title>
        </v-list-item-content>
      </v-list-item>
    </v-list>
  </v-navigation-drawer>
</template>

<script>
  export default {
    data: () => ({
      menuList: [
        { title: 'Dashboard', icon: 'mdi-view-dashboard' },
        { title: 'Messages', icon: 'mdi-message-text' },
        { title: 'My Tasks', icon: 'mdi-clipboard-text' },
        { title: 'Clients', icon: 'mdi-account-multiple' },
      ],
      menuListSecond: [
        { title: 'Main Settings', icon: 'mdi-cog' },
        { title: 'Integrations', icon: 'mdi-plus-box' }
      ]
    })
  }
</script>

<style lang="scss" scoped>
  .theme--dark .nav-drawer {
    background-color: #212936;

    &__user {
      color: #AFBDD1;

    }

    .menu-list {
      .v-subheader {
        color: #56657F;
      }

      .v-list-item {
        &__title {
          color: #56657F;
        }

        .v-icon {
          color: #56657F;
        }

        &:hover {
          background: #2B3648;
          border-radius: 4px;

          .v-list-item__title {
            color: #00BCD4;
          }

          .v-icon {
            color: #00BCD4;
          }
        }
      }

    }
  }
</style>
