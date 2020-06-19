<template>
  <span
    ><!-- Upper Fold - Issue search and action buttons -->
    <div id="upper-fold">
      <v-container>
        <v-row>
          <v-col cols="12" sm="12" md="12" id="upper-fold-button-container">
            <v-btn depressed class="upper-fold-button">
              <v-icon left dark>mdi-plus-circle-outline</v-icon>
              <span>Post New Issue</span>
            </v-btn>
            <v-btn depressed class="upper-fold-button">
              <v-icon left dark>mdi-calendar-clock</v-icon>
              <span>Schedule Help</span>
            </v-btn>
          </v-col>
        </v-row>
        <v-row>
          <v-col cols="12" sm="9" md="6">
            <!-- Issue Search Field -->
            <v-text-field
              label="Search Issues"
              id="search-bar"
              filled
              rounded
              color="#787878"
            >
              <template v-slot:append>
                <v-btn right icon @click="issueSearch">
                  <v-icon>mdi-comment-search-outline</v-icon>
                </v-btn>
              </template>
            </v-text-field>
          </v-col>
        </v-row>
      </v-container>
    </div>
    <!-- Lower Fold - Recent issues, helpers, courses  -->

    <div id="lower-fold">
      <v-row>
        <v-col class="lower-fold-col" cols="12" sm="12" md="5">
          <v-subheader>RECENT ISSUES</v-subheader>
          <IssueCard
            title="Javascript P5 change a variable after mouseclick event"
            timePosted="3"
            numComments="1"
          />
          <IssueCard
            title="Toggle button state from inside a class (p5.js)"
            timePosted="8"
            numComments="0"
          />
          <IssueCard
            title="How do I check out Arduinos from the shop?"
            timePosted="34"
            numComments="2"
          />
          <div id="issue-blob" class="blob">
            <v-btn text>More Issues</v-btn>
          </div>
        </v-col>
        <v-col class="lower-fold-col" cols="12" sm="12" md="4">
          <v-text-field solo flat class="search-input" label="Search Helpers">
            <template v-slot:append>
              <v-btn right icon @click="issueSearch">
                <v-icon>mdi-magnify</v-icon>
              </v-btn>
            </template></v-text-field
          >
        </v-col>
        <v-col class="lower-fold-col" cols="12" sm="12" md="3">
          <v-text-field solo flat class="search-input" label="Search Courses">
            <template v-slot:append>
              <v-btn right icon @click="issueSearch">
                <v-icon>mdi-magnify</v-icon>
              </v-btn>
            </template></v-text-field
          ></v-col
        >
      </v-row>
    </div>
  </span></template
>

<script>
import IssueCard from '@/components/IssueCard';

export default {
  components: { IssueCard },
  methods: {
    issueSearch() {
      alert('Searched Issues!');
    },
  },
};
</script>

<style lang="sass">
#upper-fold
  background-color: #E1E0E0
  border-bottom: 0.3rem solid #DADADA
  min-height: 30vh
  display: flex
  align-items: center
  justify-content: flex-start
  padding: 2rem
  .container
    margin-left: 1vw
  #upper-fold-button-container
    padding: 1rem
    .upper-fold-button
      font-weight: 800
      margin: 0 1rem 0 0
      background-color: #E7E7E7
      color: #787878
      letter-spacing: 0.04rem
      font-size: 0.9rem
  #search-bar
    color: #393939
    border-bottom-color: rgba(0,0,0,0)
    border-bottom-width: 0
    font-weight: 800
  label
    font-weight: 700!important
    font-size: 1.1rem
  .v-input__slot
    background-color: #E7E7E7!important
  .v-input__append-inner
    margin-top: 0!important
    align-self: center!important

#lower-fold
  .v-subheader
    color: #A3A3A3
    font-weight: 700
    font-size: 1.1rem
    margin-left: 10%
    margin-bottom: -1rem
  .lower-fold-col
    position: relative
    .blob
      background-color: #DFDFDF
      position: absolute
      bottom: -5%
      right: 8%
      z-index: 1
      border-radius: 0.75rem
      display: flex
      justify-content: flex-end
      align-items: flex-end
      padding: 0.4rem
    #issue-blob
      width: 60%
      height: 80%
      .v-btn__content
        color: grey
        font-weight: 700
  .search-input
    .v-input__slot
      background-color: #DDDDDD
      width: 16rem
      button
        color: #A1A1A1
      label
        color: #A1A1A1
</style>
