<template>
  <nav>
    <v-app-bar flat id="app-bar">
      <h1 id="title">IMA/ITP HELPER</h1>
      <v-spacer></v-spacer>
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

<style lang="sass">
#title
  color: #DADADA
  background-color: #A9A9A9
  font-weight: 900
  padding: 0 6px
  letter-spacing: 0.1rem
  font-size: 1.6rem

#app-bar
  border-bottom: 0.3rem solid #DADADA
  background-color: #E1E0E0

#profileImage
  border: 4px solid #C2C2C2
</style>