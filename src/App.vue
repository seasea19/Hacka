<template>
  <v-app>
    <v-app-bar
      app
      color="light blue"
      dark
    >
      <div class="d-flex align-center">
        <v-icon>Elections</v-icon>
      </div>



    </v-app-bar>

    <v-main>
      <HelloWorld/>
    </v-main>
  </v-app>
</template>

<script>
import HelloWorld from './components/HelloWorld';

export default {
  name: 'App',

  components: {
    HelloWorld,
  },

  data: () => ({
    //
  }),
};
</script>
