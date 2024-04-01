<template>
    <div class="hello">

      <button @click="plus">click me3!</button>
      <p>Message is {{ count }}</p>
  
      <p>Message2 is {{ msg2 }}</p>  

  
  
    </div>
  </template>
  
  <script>
 
  export default {
    name: 'Stock6Sign202402',
    components: {
    },
    props: {
    msg2: String
     }, 
    data(){
      return {

        count: 0,
  
      }
    },
  
    computed: {

    },
  
    methods: {

      plus(){
        this.count++;
      },
  
     
  
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
  