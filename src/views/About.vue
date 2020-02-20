
<template>
  <div class="about">
    <h1>This is an about page</h1>
    <input type="text" v-model="about" name="about" placeholder="Type...">
    {{ about }}
  </div>
</template>

<script>
  export default {
    name: "About",
    data() {
      return {
        about: ''
      }
    },
    created() {
      
    }
  }
</script>

<style scoped>

</style>

