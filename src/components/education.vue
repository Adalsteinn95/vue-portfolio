<template>
  <div class='education'>
      <div>{{ msg }}</div>
  </div>
</template>

<script>
export default {
  name: 'Education',
  props: ['data'],
  data() {
    return {
        msg: 'education',
    };
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
