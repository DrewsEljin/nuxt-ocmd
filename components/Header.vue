<template>
  <header>
    <v-container>
      <nuxt-link to="/">
        <img src="@/assets/images/ocmd.png" alt="" srcset="">
      </nuxt-link>
    </v-container>
  </header>
</template>

<script>
export default {
  name: 'HeaderComponent',
  data () {
    return {
      title: 'Footer'
    }
  }
}
</script>

<style scoped>
header {
  height: 90px;
  width: 100%;
  background: #404040;
}
</style>
