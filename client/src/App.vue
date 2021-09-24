<template>
  <v-app>
    <LogoBar> </LogoBar>
  </v-app>
</template>

<script>
import LogoBar from '@/components/LogoBar.vue';
// import axios from 'axios';
export default {
  name: 'App',
  cars: [],
  components: {
    LogoBar,
  },
  data: () => ({
    //
  }),
};
</script>
