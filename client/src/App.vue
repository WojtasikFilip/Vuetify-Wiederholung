<template>
  <v-app>
    <LogoBar> </LogoBar>
    <CarCards :cars="cars" />
  </v-app>
</template>

<script>
import LogoBar from '@/components/LogoBar.vue';
import CarCards from '@/components/CarCards.vue';
// import CarCard from '@/components/CarCard.vue';
import axios from 'axios';
export default {
  name: 'App',

  components: {
    LogoBar,
    CarCards,
    // CarCard,
  },
  data: () => ({
    cars: [],
    //
  }),
  created() {
    this.getCars();
  },
  methods: {
    async getCars() {
      let { data } = await axios({
        url: 'http://localhost:3000/cars',
        method: 'GET',
      });
      this.cars = data;
    },
  },
};
</script>
