<template>

   
  
   <div v-if="cSign1">
       <table>
       <tr>
       <td><h1>指標1</h1></td>
       <td><h1>{{cSign1}}</h1></td>
       </tr>
       <tr>
       <td><h1>指標2</h1></td>
       <td><h1>{{cSign2}}</h1></td>
       </tr>
       <tr>
       <td><h1>指標3</h1></td>
       <td><h1>{{cSign3}}</h1></td>
       </tr>
       <tr>
       <td><h1>指標4</h1></td>
       <td><h1>{{cSign4}}</h1></td>
       </tr>
       <tr>
       <td><h1>指標5</h1></td>
       <td><h1>{{cSign5}}</h1></td>
       </tr>
       <tr>
       <td><h1>指標6</h1></td>
       <td><h1>{{cSign6}}</h1></td>
       </tr>
       </table>
   </div>
   
  
  </template>
  
  <script>
  
  export default {
    name: 'TotalScore',
    components: {
  
    },
  
    props: {
        stock6data: {
            type: Object
        }
    }, 
    data(){
      return {
        cSign1: "",
        cSign2: "",     
        cSign3: "",
        cSign4: "",
        cSign5: "",
        cSign6: "",
    
      }
    },
  
    computed: {
        response(){
            return {
            'cSign1': this.cSign1,
            'cSign2': this.cSign2,
            'cSign3': this.cSign3,
            'cSign4': this.cSign4,
            'cSign5': this.cSign5,
            'cSign6': this.cSign6,
        }
        }
    },
  
    methods: {

        },      
  
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
  