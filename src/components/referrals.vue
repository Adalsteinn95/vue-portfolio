<template>
  <div class='referrals'>
      <div>{{ msg }}</div>
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
