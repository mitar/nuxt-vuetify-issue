<template>
  <v-row>
    <v-col
      sm="10"
      offset-sm="1"
      md="8"
      offset-md="2"
      xl="6"
      offset-xl="3"
    >
      <v-card>
        <v-alert v-if="error.statusCode === 404" type="error">
          {{ pageNotFound }}.
        </v-alert>
        <v-alert v-else type="error">
          {{ otherError }}.
        </v-alert>
      </v-card>
    </v-col>
  </v-row>
</template>

<script>
  // @vue/component
  const component = {
    props: {
      error: {
        type: Object,
        default: null,
      },
    },
    head() {
      const title = this.error.statusCode === 404 ? this.pageNotFound : this.otherError;
      return {
        title,
      };
    },
    data() {
      return {
        pageNotFound: 'Not found',
        otherError: 'An error occurred',
      };
    },
  };

  export default component;
</script>
