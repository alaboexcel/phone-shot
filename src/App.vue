<template>
  <v-app>
    <v-content>
      <headercomponent/>
      <router-view></router-view>
    </v-content>
  </v-app>
</template>

<script>
import headercomponent from './components/headercomponent';

export default {
  name: 'App',

  components: {
    headercomponent,
  },

  data: () => ({
    //
  }),
};
</script>
