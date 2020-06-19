<template>
  <nav>
    <v-app-bar flat id="app-bar">
      <h1 id="title">IMA/ITP HELPER</h1>
      <v-spacer></v-spacer>
      <div id="name-column">
        <div id="name">Ethan Printz</div>
        <div id="points">
          <v-icon small color="grey">mdi-trophy-variant-outline</v-icon>
          <span>63 Points</span>
        </div>
      </div>
      <v-avatar>
        <!-- Profile Image - Change Later -->
        <img
          id="profileImage"
          src="https://media-exp1.licdn.com/dms/image/C4D03AQHeTuLR_eEAQw/profile-displayphoto-shrink_100_100/0?e=1597881600&v=beta&t=mnp1xV3fE4ZtDlefXg1njg8KFqNUrVqKhOAMGoRj8eo"
          alt="Ethan"
        />
      </v-avatar>
    </v-app-bar>
  </nav>
</template>

<script>
export default {};
</script>

<style scoped lang="sass">
#title
  color: #DADADA
  background-color: #A9A9A9
  font-weight: 900
  padding: 0 6px
  letter-spacing: 0.15rem
  font-size: 1.6rem
  transition: 0.1s
  cursor: pointer
#title:hover
    background-color: #66129D

#app-bar
  border-bottom: 0.3rem solid #DADADA
  background-color: #E1E0E0

#profileImage
  border: 4px solid #C2C2C2

#name-column
  height: 100%
  min-width: 8vw
  display: flex
  flex-direction: column
  align-items: flex-end
  justify-content: center
  margin-right: 1rem
  color: grey

#name
  font-size: 1.1rem
  font-weight: 800
  letter-spacing: 0.03rem

#points
  font-size: 0.85rem
  display: flex
  align-items: center
  justify-content: flex-end
  font-weight: 700
  color: #9E9E9E
  margin-top: -0.5vh
</style>
