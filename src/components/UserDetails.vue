<template>
  <div class="bg-red-light mx-auto mt-4 p-8 max-w-m border border-red shadow-lg rounded-lg overflow-hidden">
    <h1>You may view User Details here</h1>
    <p>Many details</p>
    <p>User Name: {{ name }}</p>
    <p>User Reversed Name: {{ reverseName() }}</p>
  </div>
</template>

<script>
  export default {
    props: {
      name: String
    },
    methods: {
      reverseName() {
        return this.name.split("").reverse().join("");
      }
    }
  }
</script>

<style scoped>

</style>