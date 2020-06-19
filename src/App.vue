<template>
  <v-app>
    <!-- Navbar -->
    <Navbar />
    <!-- Main Content -->
    <v-content id="content">
      <router-view></router-view>
    </v-content>
  </v-app>
</template>

<script>
// Imports
import Navbar from '@/components/Navbar';

// Export data to template
export default {
  name: 'App',
  components: { Navbar },
  data: () => ({
    //
  }),
};
</script>

<style lang="sass">
#content
  background-color: #E5E5E5
  margin-top: -0.3rem
</style>
