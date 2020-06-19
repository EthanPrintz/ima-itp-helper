<template>
  <v-chip id="chip" :style="style" link>{{ name }}</v-chip>
</template>

<script>
export default {
  props: {
    name: {
      type: String,
    },
    color: {
      type: String,
    },
  },
  // Compute the background color from prop
  computed: {
    style() {
      return 'background-color: ' + this.color;
    },
  },
};
</script>

<style scoped lang="sass">
#chip
  color: #F0F0F0
  font-weight: 800
  font-size: 0.75rem
  min-width: 3rem
  display: flex
  justify-content: center
  align-items: center
  height: 1.5rem
</style>
