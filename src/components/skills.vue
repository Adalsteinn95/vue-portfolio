<template>
  <div class='skills'>
      <div>{{ msg }}</div>
      <div>{{ msg }}</div>
      <div>{{ msg }}</div>
  </div>
</template>

<script>
export default {
  name: 'Skills',
  props: ['data'],
  data() {
    return {
        msg: 'Skills',
    };
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

.skills {
  margin: 30px;
}

</style>
