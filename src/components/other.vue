<template>
  <div class='other'>
      <h1>{{ data.header }}</h1>
      <div v-for="item in data.items ">
        <div>{{ item }}</div>
      </div>
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

h1 {
  font-size: 2em;
}

.other {
  border: 2px solid royalblue;
}

</style>
