<template>
  <div id="app" class="container mx-auto">
    <div class="bg-white mx-auto mt-8 p-8 max-w-m shadow-lg rounded-lg overflow-hidden">
      <h1>The User Component</h1>
      <p>I'm an awesome user!</p>
      <button @click="changeName" class="text-xl mt-4 font-hairline rounded-full px-4 py-1 leading-normal bg-white border border-purple text-purple hover:bg-purple hover:text-white">Change my name!</button>
      <hr class="border">
      <div class="flex mb-4">
        <div class="w-1/2 mr-4">
          <user-details :name="1"></user-details>
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
  data() {
    return {
      name: 'Igor'
    }
  },
  methods: {
    changeName() {
      this.name = 'Anna'
    }
  },
  name: 'app',
  components: {
    UserDetails,
    EditUser
  }
}
</script>

<style>
  html {
    font-size: 18px;
  }
</style>
