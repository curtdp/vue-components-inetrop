<template>
  <div class="bg-green-light mx-auto mt-4 p-8 max-w-m border border-green shadow-lg rounded-lg overflow-hidden">
    <h1>You may edit the User here</h1>
    <p>Edit me!</p>
    <p>User Age: {{ userAge }}</p>
    <button @click="editAge" class="text-xl mt-4 font-hairline rounded-full px-4 py-1 leading-normal bg-green-lightest border border-green text-green hover:bg-green hover:text-white">Edit Age</button>
  </div>
</template>

<script>
  export default {
    props: ['userAge'],
    methods: {
      editAge() {
        this.userAge = 30;
        this.$emit('ageWasEdited', this.userAge)
      }
    },
  }
</script>

<style scoped>

</style>