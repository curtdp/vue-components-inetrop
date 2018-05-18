<template>
  <div class="bg-red-light mx-auto mt-4 p-8 max-w-m border border-red shadow-lg rounded-lg overflow-hidden">
    <h1>You may view User Details here</h1>
    <p>Many details</p>
    <p>User Name: {{ name }}</p>
    <p>User Age: {{ userAge }}</p>
    <button @click="resetName" class="text-xl mt-4 font-hairline rounded-full px-4 py-1 leading-normal bg-green-lightest border border-green text-green hover:bg-green hover:text-white">Reset Name</button>
    <button @click="resetFn" class="text-xl mt-4 font-hairline rounded-full px-4 py-1 leading-normal bg-green-lightest border border-green text-green hover:bg-green hover:text-white">ResetFn Name</button>
  </div>
</template>

<script>
  import { eventBus } from '../main.js'
  export default {
    props: {
      name: String,
      resetFn: Function,
      userAge: Number
    },
    methods: {
      reverseName() {
        return this.name.split("").reverse().join("");
      },
      resetName() {
        this.$emit('nameWasReset', 'Igor');
      }
    },
    created() {
      eventBus.$on('ageWasEdited', (age) => {
        this.userAge = age;
      })
    }
  }
</script>

<style scoped>

</style>