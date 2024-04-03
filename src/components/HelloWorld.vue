<template>



  <div class="hello">
    <h1>{{ msg }}</h1>
  



    <input type="text" v-model="inputText2" placeholder="Type something2">
    <button @click="handleSubmit">Submit2</button>
    <div v-if="result2">
      <p>Result2: {{ result2 }}</p>
    </div>


  </div>
  <br>
  
 

 <div v-if="cSign1">
     <table align=center border="1">
     <tr>
     <td align=center><h1>指標1</h1></td>
     <td align=center><h1>{{cSign1}}</h1></td>
     </tr>
     <tr>
     <td align=center><h1>指標2</h1></td>
     <td align=center><h1>{{cSign2}}</h1></td>
     </tr>
     <tr>
     <td align=center><h1>指標3</h1></td>
     <td align=center><h1>{{cSign3}}</h1></td>
     </tr>
     <tr>
     <td align=center><h1>指標4</h1></td>
     <td align=center><h1>{{cSign4}}</h1></td>
     </tr>
     <tr>
     <td align=center><h1>指標5</h1></td>
     <td align=center><h1>{{cSign5}}</h1></td>
     </tr>
     <tr>
     <td align=center><h1>指標6</h1></td>
     <td align=center><h1>{{cSign6}}</h1></td>
     </tr>
     </table>
 </div>
 <br>
 <br>



</template>

<script>

export default {
  name: 'HelloWorld',
  components: {

  },

  props: {

  }, 
  data(){
    return {
      response: "",
      inputText2: '',
      result2: '',
      Url: '',
      cSign1: "",
      cSign2: "",     
      cSign3: "",
      cSign4: "",
      cSign5: "",
      cSign6: "",
  
    }
  },

  computed: {

  },

  methods: {
    handleSubmit(){

        this.result2 =  `https://stock6-restfulex.onrender.com/api/Stock6Sign202402/getstockinfo/${this.inputText2}`;

        console.log(`最新得到網址為${this.result2}`);       
        fetch(this.result2) 
        .then(data => data.json())
        .then(response => {
          const {cStockName, cNewestSeason,cSign1, cSign2, cSign3, cSign4, cSign5, cSign6} = response;
          console.log(cStockName);
          console.log(cNewestSeason);
          //const {cSign1, cSign2, cSign3, cSign4, cSign5, cSign6} = response;
          console.log(cSign1);          
          console.log(cSign2);     
          console.log(cSign3);     
          console.log(cSign4);     
          console.log(cSign5);     
          console.log(cSign6);  
          this.cSign1 = cSign1;
          this.cSign2 = cSign2;
          this.cSign3 = cSign3;
          this.cSign4 = cSign4;
          this.cSign5 = cSign5;
          this.cSign6 = cSign6;          
        });  

      

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
