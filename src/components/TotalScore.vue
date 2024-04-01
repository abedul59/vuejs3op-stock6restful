<template>
<div>
 

 <div>
     <table>
     <tr>
     <td><h1>指標1</h1></td>
     <td><h1>{stock6data.cSign1}</h1></td>
     </tr>
     <tr>
     <td><h1>指標2</h1></td>
     <td><h1>{stock6data.cSign2}</h1></td>
     </tr>
     <tr>
     <td><h1>指標3</h1></td>
     <td><h1>{stock6data.cSign3}</h1></td>
     </tr>
     <tr>
     <td><h1>指標4</h1></td>
     <td><h1>{stock6data.cSign4}</h1></td>
     </tr>
     <tr>
     <td><h1>指標5</h1></td>
     <td><h1>{stock6data.cSign5}</h1></td>
     </tr>
     <tr>
     <td><h1>指標6</h1></td>
     <td><h1>{stock6data.cSign6}</h1></td>
     </tr>
     </table>
 </div>
 </div>
  
  
</template>
  
<script>

  export default {
    name: 'TotalScore',

    props: {
    stock6data: Object
  },    

    data(){
      return {
        

      }
    },
  
    computed: {

    },
  
    methods: {
 
  
  }
  
  }
  
  </script>
  
  <!-- Add "scoped" attribute to limit CSS to this component only -->
  <style scoped>
  h3 {
    margin: 40px 0 0;
  }
  ul {
    list-style-type: none;
    padding: 0;
  }
  li {
    display: inline-block;
    margin: 0 10px;
  }
  a {
    color: #42b983;
  }
  </style>
  