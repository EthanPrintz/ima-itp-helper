<template>
  <v-card flat id="container">
    <p id="time-passed">{{ timePosted }} MINUTES AGO</p>
    <h2 id="title">{{ title }}</h2>
    <v-chip-group>
      <TechChip name="Javascript" color="#E6B767" />
      <TechChip name="P5" color="#E1527C" />
      <TechChip name="Web" color="#527FE1" />
    </v-chip-group>
    <v-icon x-large id="comments">mdi-comment-outline</v-icon>
    <div id="comment-num">{{ numComments }}</div>
  </v-card>
</template>

<script>
import TechChip from '@/components/TechChip.vue';
export default {
  props: {
    chips: {
      type: Array,
    },
    timePosted: {
      type: String,
    },
    title: {
      type: String,
    },
    numComments: {
      type: String,
    },
  },
  components: { TechChip },
};
</script>

<style scoped lang="sass">
#container
  width: 74%
  margin: 1rem 13%
  background-color: #F0F0F0
  border-radius: 0.5rem
  padding: 1rem
  position: relative
  z-index: 2
  #time-passed
    color: #B0B0B0
    font-size: 0.8rem
    font-weight: 700
  #title
    font-size: 1.1rem
    color: #5A5A5A
    margin-top: -1rem
    font-weight: 800
    line-height: 1.4rem
    width: 70%
  #comments
    position: absolute
    bottom: 1rem
    right: 1rem
    color: #D0D1D6
  #comment-num
    position: absolute
    bottom: 1.65rem
    right: 1.9rem
    z-index: 2
    color: #D0D1D6
    font-weight: 900
    font-size: 1.1rem
</style>
