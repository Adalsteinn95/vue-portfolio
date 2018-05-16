<template>
  <div class='project'>
      <div>{{ msg }}</div>
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

</style>
