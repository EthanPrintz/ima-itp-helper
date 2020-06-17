<template>
  <v-app>
    <!-- Navbar -->
    <Navbar />
    <!-- Main content -->
    <v-content id="content">
      <v-col cols="12" sm="6" md="3">
        <!-- Issue Search Field -->
        <v-text-field
          label="Search Issues"
          id="search-bar"
          filled
          rounded
          @click:append="issueSearch"
          append-icon="mdi-comment-search-outline"
        ></v-text-field>
      </v-col>
    </v-content>
  </v-app>
</template>

<script>
import Navbar from "@/components/Navbar";
export default {
  name: "App",
  components: { Navbar },
  data: () => ({
    //
  }),
  methods: {
    issueSearch() {
      alert("Searched Issues!");
    }
  }
};
</script>

<style lang="sass">
#content
  background-color: #E5E5E5
#search-bar
  color: #787878
  border-bottom-color: rgba(0,0,0,0)
  border-bottom-width: 0
</style>