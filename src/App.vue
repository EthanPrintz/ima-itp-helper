<template>
  <v-app>
    <!-- Navbar -->
    <Navbar />
    <!-- Main content -->
    <v-content id="content">
      <div id="upper-fold">
        <v-col cols="12" sm="8" md="6">
          <div id="upper-fold-button-container">
            <v-btn depressed class="upper-fold-button">
              <v-icon left dark>mdi-plus-circle-outline</v-icon>
              <span>Post New Issue</span>
            </v-btn>
            <v-btn depressed class="upper-fold-button">
              <v-icon left dark>mdi-calendar-plus</v-icon>
              <span>Schedule Help</span>
            </v-btn>
          </div>
          <!-- Issue Search Field -->
          <v-text-field label="Search Issues" id="search-bar" filled rounded color="#787878">
            <template v-slot:append>
              <v-btn right icon @click="issueSearch">
                <v-icon>mdi-comment-search-outline</v-icon>
              </v-btn>
            </template>
          </v-text-field>
        </v-col>
      </div>
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
  margin-top: -0.3rem

#upper-fold
  background-color: #E1E0E0
  border-bottom: 0.3rem solid #DADADA
  min-height: 40vh
  display: flex
  align-items: center
  justify-content: flex-start
  padding: 2rem
  #upper-fold-button-container
    padding: 1rem
    .upper-fold-button
      font-weight: 700
      margin: 0 1rem 0 0
      background-color: #E7E7E7
      color: #787878

#search-bar
  color: #393939
  border-bottom-color: rgba(0,0,0,0)
  border-bottom-width: 0
  font-weight: 800
.v-input__slot
  background-color: #E7E7E7!important
.v-input__append-inner
  margin-top: 0!important
  align-self: center!important
</style>