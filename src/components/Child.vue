<template>
  <div>
    <h2>Child Component</h2>
    <p>{{ message }}</p>
  </div>
</template>

<script>
export default {
  name: 'Child',
  props: {
    message: {
      type: String,
      required: true
    }
  }
}
</script>

<style scoped>

</style>
