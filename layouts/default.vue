<template>
  <v-app>
    <v-app-bar
      app
      absolute
    >
      <v-toolbar-items>
        <!--
          Setting active CSS class manually.
          See: https://github.com/vuejs/vue-router/issues/2040
        -->
        <v-btn
          :class="$route.path === '/' && 'v-btn--active'"
          to="/"
          nuxt
          text
          exact
        >Index</v-btn>
      </v-toolbar-items>
      <v-spacer />
    </v-app-bar>
    <v-content>
      <v-container
        fluid
      >
        <nuxt keep-alive />
      </v-container>
    </v-content>
  </v-app>
</template>

<script>
  // @vue/component
  const component = {};

  export default component;
</script>

<style lang="scss">
  .v-toolbar__title.v-btn {
    text-transform: inherit;
    letter-spacing: inherit;
    font-weight: inherit;
  }

  .v-toolbar__title.v-btn.v-size--x-large {
    font-size: 1.25rem;
  }
</style>
