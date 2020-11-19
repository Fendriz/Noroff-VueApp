<template>
    <div class="recipe">
        <div class = "recipe_image">
            <img :src="recipimg" >
        </div>
        <div class ="recipe_title">
            <p>{{title}} </p><br>
        </div>
        <div class = "recipe_list">
            <b>Ingredients: </b><br><br>
               <p>{{ingredients}}</p> <br>
        </div>
        <div class="recipe_link">
            <b>Link: </b><br><br>
            <a :href="link">{{link}}</a>
        </div>
    </div>
</template>
<script>
    export default {
        name: 'recipListComponent',
        props: ['title','recipimg','ingredients','link']
    }
</script>
<style scoped>
   .recipe{
       background-color: #243A69;
       color:white;
       width: 300px;
       margin:20px;
       padding:20px;
       border-radius: 20px;
   }
   .recipe_image img {
       float:right;
       margin-left:10px;
       border-radius: 10px;
       border: solid 2px white;
   }
   .recipe_title{
       font-size:24px;
       font-weight:bold;
   }
   .recipe_link a{
       text-decoration:none;
       color:#ACB9D5;
   }
   .recipe_link a:hover{
      
       color:white;
       font-weight:bold;
   }
   b{
       text-decoration:underline;
   }
   p{
       margin:0;
   }
</style>