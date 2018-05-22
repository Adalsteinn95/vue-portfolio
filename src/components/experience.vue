<template>
  <div class='experience'>
      <div>{{ data.work }}</div>
      <div>{{ data.year }}</div>
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

.experience {
  display: flex;
  justify-content: space-between;
  margin: 30px;
}

</style>
