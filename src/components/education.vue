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
      <div class='eduaction__logo'>
        <img :src="data.logo" alt="">
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
  justify-content: space-around;
  min-width: 500px;
  max-width: 800px;
  margin: 60px auto;
  font-size: 1.5em;
}

.education img { 
  max-width: 200px;
  max-height: 100px;
}

.education > div {
  align-self: center;
  padding: 10px;
}

@media (max-width: 600px) {
  .education {
    font-size: 1em;
  }
}

</style>
