<template>
  <div class='header'>
    <img src="../assets/vinna.jpg">
    <h1>{{ title }}</h1>
  </div>
</template>

<script>
export default {
  name: 'Header',
  props: ['title','about'],
  data() {
    return {
        msg: 'hallo',
    };
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
