<template>
  <div class='project'>
      <div class='card'>
        <div>{{ data.title }}</div>
        <div>{{ data.about }}</div>
        <a v-bind:href="data.repo">repo</a>
      </div>
  </div>
</template>

<script>
export default {
  name: 'Project',
  props: ['data'],
  data() {
    return {
        msg: 'project',
    };
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

.card {
  border: 2px solid salmon;
  max-width: 400px;
  margin: 10px;
  padding: 10px;
}

</style>
