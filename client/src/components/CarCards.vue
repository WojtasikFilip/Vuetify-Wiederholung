<template>
  <div>
    <CarCard :c="c" v-for="c of cars" :key="c.id"> </CarCard>
  </div>
</template>

<script>
import CarCard from '@/components/CarCard.vue';
export default {
  props: {
    cars: {
      type: Array,
    },
  },
  components: {
    CarCard,
  },
};
</script>

<style lang="scss" scoped></style>
