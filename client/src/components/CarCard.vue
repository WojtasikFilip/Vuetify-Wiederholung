<template>
  <v-card class="my-6 mx-4" max-width="370">
    <v-img height="250" :src="c.image"></v-img>
    <v-card-title>{{ c.title }}</v-card-title>
    <v-card-text>
      <v-row align="center" class="mx-0 text-subtitle-1">
        Owner: <b>{{ c.owner.firstName }} {{ c.owner.lastName }}</b>
      </v-row>
      <p>Year: <b>{{ c.yearOfMake }}</b></p>
      <p>Miles: <b>{{ c.miles }}</b></p>
      <p>Price: <b>{{ c.price }}</b></p>

      <p>
        {{ c.description }}
      </p>
    </v-card-text>
  </v-card>
</template>

<script>
export default {
  props: {
    c: {
      type: Object,
    },
  },
};
</script>

<style lang="scss" scoped></style>
