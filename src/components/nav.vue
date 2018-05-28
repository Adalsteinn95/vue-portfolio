<template>
  <div class='navigate'>
    <div v-for="item in data" :key="item" >
      <h2>{{ item }}</h2>
    </div>
    <h1>{{ data[0] }}</h1>
    <div v-on:click="navActive" class="nav-icon" v-bind:class="[isActive ? 'active' : '']">
      <div v-on:hover="navHover" class="nav-line"></div>
      <div v-on:hover="navHover" class="nav-line"></div>
      <div v-on:hover="navHover" class="nav-line"></div>
    </div>
  </div>

</template>

<script>
export default {
  name: "navigate",
  props: ["data"],
  data() {
    return {
      msg: "hallo",
      navHover: 'hello',
      isActive: false,
    };
  },
  methods: {
    navActive: function() {
      this.isActive = !this.isActive;
    }
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.navigate {
}

.nav-line {
  height: 5px;
  margin: 10px;
  width: 50px;
  background-color:	#B22222;
}

.nav-icon {
  position: absolute;
  transition: 0.3s ease-in;
}

.nav-icon:hover {
  transform: scale(1.1);
}

.nav-line {
  transition: 0.5s ease-in-out;
}

.active {
  transition: 0.5s ease-in-out;
}

.active div {
  transition: 0.5s ease-in-out;
}
.active div:nth-child(1){
  position: absolute;
  top: 15px;
  transform: rotate(-45deg);
}

.active div:nth-child(2){
  opacity: 0;
}

.active div:nth-child(3){
  transform: rotate(45deg);
}

</style>
