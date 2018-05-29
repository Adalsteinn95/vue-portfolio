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
  background: #16222A;  /* fallback for old browsers */
  background: -webkit-linear-gradient(to bottom, #3A6073, #16222A);  /* Chrome 10-25, Safari 5.1-6 */
  background: linear-gradient(to bottom, #3A6073, #16222A); /* W3C, IE 10+/ Edge, Firefox 16+, Chrome 26+, Opera 12+, Safari 7+ */
  border-radius: 10px;

  color: gold;  /* fallback for old browsers */
  color: -webkit-linear-gradient(to bottom, #EDDE5D, gold);  /* Chrome 10-25, Safari 5.1-6 */
  color: linear-gradient(to bottom, #EDDE5D, gold); /* W3C, IE 10+/ Edge, Firefox 16+, Chrome 26+, Opera 12+, Safari 7+ */
  transition: 0.5s ease-in;
  opacity: 0;
}


.navigate__items div {
  font-family: 'Raleway', sans-serif;
  font-size: 1.5em;
  display: flex;
  flex-direction: column;
  height: 60px;
  justify-content: center;
  padding: 15px;
}

.navigate__items--on {
  left: 60px;
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


@media (max-width: 1800px) {
  .navigate__items div {
    font-size: 1em;
  }
}
@media (max-width: 1750px) {
  
  .navigate__items {
    left: 30px;
  }

  
  
}

@media (max-width: 1650px) {
  .navigate__items {
    opacity: 0;
  }
}

</style>
