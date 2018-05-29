<template>
  <div class='header'>
    <img src="../assets/vinna.jpg">
    <h2>{{ title }}</h2>
  </div>
</template>

<script>
export default {
  name: 'Header',
  props: ['title','about'],
  data() {
    return {
        msg: 'hallo',
    };
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

h2 {
  margin-top: 20px;
  font-size: 3em;
  font-family: 'Herr Von Muellerhoff', cursive;
}

.header > img {
  margin-top: 50px;
  border: 2px solid black;
  border-radius: 60%;
}

</style>
