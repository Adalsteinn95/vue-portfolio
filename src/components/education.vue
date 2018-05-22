<template>
  <div class='education'>
      <div>
        <h2>{{ data.school }}</h2>
      </div>
      <div>
        <h2>{{ data.subject }}</h2>
      </div>
      <div>
        <h2>{{ data.year }}</h2>
      </div>
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

.education {
  display: flex;
  justify-content: space-between;
  margin: 50px;
}
</style>
