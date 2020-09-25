<template>
  <div class="[ row ]">
    <div class=" [col-sm-12] "></div>
    <div class=" [col-sm-12] ">
       <div>
         <h3>{{message}}</h3>
       </div>
       <form>
         
       </form>
    </div>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'App',
  components: {
    HelloWorld
  },

    mounted: function() {
    fetch("http://www.recipepuppy.com/api/", {
      method: 'get'
    })
      .then((response) => {
        return response.json()
      })
      .then((jsonData) => {

      })
  },
    
}


</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
