<template>
  <div class='referrals'>
      <div>{{ data.name }}</div>
      <div>{{ data.position }}</div>
      <div>{{ data.contact }}</div>
  </div>
</template>

<script>
export default {
  name: 'Referrals',
  props: ['data'],
  data() {
    return {
        msg: 'referrals',
    };
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
