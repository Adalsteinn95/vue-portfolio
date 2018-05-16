<template>
  <div class='other'>
      <div>{{ msg }}</div>
  </div>
</template>

<script>
export default {
  name: 'Other',
  props: ['data'],
  data() {
    return {
        msg: 'other',
    };
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
