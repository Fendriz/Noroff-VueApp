<template>
    <div class="container">
        <div v-for="item in recipes" :key="item">
            <recipListComponent v-bind:title="item.title"
                                v-bind:recipimg="item.thumbnail"
                                v-bind:ingredients="item.ingredients"
                                v-bind:link="item.href"
            ></recipListComponent>
        </div>
    </div>
    
</template>

<script>

import recipListComponent from './recipListComponent'
export default {
  name: 'recipeList',
  components: {
    recipListComponent
  },
  data(){
    return{
        
        
      recipes: []
    }
  },
  beforeMount: function(){
    const app = this;
    const cors = 'http://cors-anywhere.herokuapp.com/'
    const url = 'http://www.recipepuppy.com/api/'
    fetch(cors+url)
    .then(function(res){
      return res.json();
    })
    .then(function(res){
      
        app.recipes = res.results;
    })

  }

}
</script>

<style>
.body{
    font-family: Arial, Helvetica, sans-serif;
}
.container{
    display:flex;
    flex-wrap: wrap;
    justify-content: space-around;
}
</style>