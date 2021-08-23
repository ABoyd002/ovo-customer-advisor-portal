<template>
  <v-app>
    <v-app-bar app dark color="primary">
      <v-toolbar-title>
        <nuxt-link to="/" class="white--text text-decoration-none">
          OVO Advisor Center
        </nuxt-link>
      </v-toolbar-title>
    </v-app-bar>

    <v-navigation-drawer
      app
      value="true"
      color="primary lighten-4"
      expand-on-hover
    >
      <v-list nav>
        <v-list-item
          v-for="(item, i) in links"
          :key="`link-${i}`"
          :to="item.link"
        >
          <v-list-item-icon>
            <v-icon v-text="item.icon" />
          </v-list-item-icon>
          <v-list-item-title>{{ item.name }}</v-list-item-title>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>

    <v-main>
      <Nuxt />
    </v-main>
  </v-app>
</template>

<script>
export default {
  data() {
    return {
      links: [
        {
          name: "Home",
          link: "/",
          icon: "mdi-home",
        },
        {
          name: "Phone Fixes",
          link: "/phone-fix",
          icon: "mdi-phone",
        },
      ],
    };
  },
};
</script>
