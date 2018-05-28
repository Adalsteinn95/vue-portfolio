<template>
  <div class='navigate'>
    <div v-on:click="navActive" class="nav-icon" v-bind:class="[isActive ? 'active' : '']">
      <div v-on:hover="navHover" class="nav-line"></div>
      <div v-on:hover="navHover" class="nav-line"></div>
      <div v-on:hover="navHover" class="nav-line"></div>
    </div>
    <div class='navigate__items' v-bind:class="[isActive ? 'navigate__items--on' : '']" >
      <div v-for="item in data" :key="item" >
       <h2>{{ item }}</h2>
      </div>
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
  position: absolute;
}

.navigate__items {
  position: fixed;
  left: -300px;
  display: flex;
  flex-direction: column;
  background-color: purple;
  border-radius: 10px;
  color: gold;
  transition: 0.5s ease-in;
  opacity: 0;
}


.navigate__items div {
  display: flex;
  flex-direction: column;
  height: 60px;
  justify-content: center;
  padding: 15px;
}

.navigate__items--on {
  left: 100px;
  opacity: 1;
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
