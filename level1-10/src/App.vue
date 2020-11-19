<template>
  <div id="app" class="container">
 
  </div>

 
</template>

<script>


// import Todos from './components/Todos'
export default {
  name: 'App',
 
  // data: {
  //   message: 'please enter login details'
  // },
  data(){
    return{
      jobs: []
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
      app.jobs = res;
    

    })

  }

}
</script>

<style>
</style>
