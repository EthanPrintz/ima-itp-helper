<template>
  <v-card flat id="container">
    <p id="time-passed">{{timePosted}} MINUTES AGO</p>
    <h2 id="title">{{title}}</h2>
    <v-chip-group>
      <TechChip name="Javascript" color="#E6B767" />
      <TechChip name="P5" color="#E1527C" />
    </v-chip-group>
  </v-card>
</template>

<script>
import TechChip from "@/components/TechChip.vue";
export default {
  props: {
    chips: {
      type: Array
    },
    timePosted: {
      type: String
    },
    title: {
      type: String
    }
  },
  components: { TechChip }
};
</script>

<style scoped lang="sass">
#container
  width: 80%
  margin: 1rem 10%
  background-color: #F0F0F0
  border-radius: 0.5rem
  padding: 1rem
  #time-passed
    color: #B0B0B0
    font-size: 0.8rem
    font-weight: 700
  #title
    font-size: 1.2rem
    color: #5A5A5A
    margin-top: -1rem
    font-weight: 800
</style>  