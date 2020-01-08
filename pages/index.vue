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
        <v-card-text>
          <div class="text-center">
            See the size of the icon bellow.
          </div>
        </v-card-text>
        <v-card-actions>
          <v-btn href="https://gitlab.com" depressed>
            <v-icon
              left
            >mdi-gitlab</v-icon> GitLab
          </v-btn>
        </v-card-actions>
      </v-card>
    </v-col>
  </v-row>
</template>

<script>
  // @vue/component
  const component = {
  };

  export default component;
</script>
