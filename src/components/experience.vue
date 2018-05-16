<template>
  <div class='experience'>
      <div>{{ msg }}</div>
  </div>
</template>

<script>
export default {
  name: 'Experience',
  props: ['data'],
  data() {
    return {
        msg: 'experience',
    };
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
