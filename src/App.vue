<template>
  <div id="app" class="container mx-auto">
    <div class="bg-white mx-auto mt-8 p-8 max-w-m shadow-lg rounded-lg overflow-hidden">
      <h1>The User Component</h1>
      <p>I'm an awesome user!</p>
      <hr class="border">
      <div class="flex mb-4">
        <div class="w-1/2 mr-4">
          <user-details></user-details>
        </div>
        <div class="w-1/2">
          <edit-user></edit-user>
        </div>
      </div>
    </div>
  </div>
</template>

<script>

import UserDetails from './components/UserDetails.vue'
import EditUser from './components/EditUser.vue'
export default {
  name: 'app',
  components: {
    UserDetails,
    EditUser
  }
}
</script>

<style>
  body {

  }
</style>
