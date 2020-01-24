<template>
  <div>
    <div class="ui secondary pointing menu">
      <a href="/" class="active item">
        Image Storage
      </a>
      <div class="right menu">
        <div v-if="isLoggedIn">
          Gallery
          Upload
          <a class="ui item" @click="logout"> Log Out</a>
        </div>
        <a v-else class="ui item" @click="login">
          Login
        </a>
      </div>
    </div>
  </div>
</template>

<script>
import { mapActions, mapGetters } from 'vuex'

export default {
  name: 'AppHeader',
  computed: mapGetters(['isLoggedIn']),
  methods: mapActions(['login', 'logout'])
}
</script>

<style scoped>

</style>