<template>



  <div class="hello">
    <h1>{{ msg }}</h1>
    <h1>{{ msg }}</h1>

    <h1>{{price}}</h1><br>
    <h1>{{quantity}}</h1><br>
    <h1>{{price * quantity}}</h1><br>
    <h1>{{subtotal1}}</h1><br>
    <h1>{{subtotal2()}}</h1><br>

    <input v-model = "message1" placeholder="edit me!">
    <p>Message is {{ message1 }}</p>

    <textarea v-model="message2" placeholder="add multiple lines"></textarea>
    <p><span>Multiline message is:</span> {{ message2 }}</p>

    <button>click me!</button>

    <button v-bind:disabled="isBtnDisabled">click me2!</button>

    <button @click="plus">click me3!</button>
    <p>Message is {{ count }}</p>


    <input type="text" v-model="inputText" placeholder="Type something">
    <button @click="showResult">Submit</button>
    <div v-if="result">
      <p>Result: {{ result }}</p>
    </div>

    <input type="text" v-model="inputText2" placeholder="Type something2">
    <button @click="handleSubmit">Submit2</button>
    <div v-if="result2">
      <p>Result2: {{ result2 }}</p>
    </div>


  </div>
  <br>
  <div>
 

 <div  v-if="cSign1">
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
 </div>

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
      isBtnDisabled: true,
      price: 1000,
      quantity: 5.5,
      message1: "",
      message2: "",
      count: 0,
      inputText: '',
      inputText2: '',
      result: '',
      result2: '',
      Url: ''
     

    }
  },

  computed: {
    subtotal1: function(){
      return this.price * this.quantity;
    } 
  },

  methods: {
    subtotal2: function(){
      return this.price * this.quantity;
    },
    plus(){
      this.count++;
    },

    showResult() {
          this.result = this.inputText;
        },

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
