<template>
  <div class="[ row ]">hu
   <div v-for="recipe in recipes" class=" [col-sm-12] ">
      <RecipeListingComponent      v-bind: 
      ></RecipeListingComponent> 
   </div>
  </div>
</template>

<script>
import RecipeListingComponent from './components/app.vue'
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  
data(){
  return{
    recipe: []
  }
},

beforeMount: function(){

const conversionUrl = 'https://cors-anywhere.herokuapp.com/';
const url = 'http://www.recipepuppy.com/api/';

 fetch(conversionUrl + url)
 .then(function(response) {
   return response.json();
 })
 .then(function(result) {
   app.recipe = result;
 })
}
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
