<template>

  <div class="hello">
    <h1>{{ msg }}</h1>
  
    <input type="text" v-model="inputText2" placeholder="輸入台股代號">
    <button @click="handleSubmit">Submit2</button>
    <div v-if="result2">
      <p>Result2: {{ result2 }}</p>
    </div>


  </div>
  <br>
  

 <br>
 
<total-score v-bind="stock6data2"></total-score>
 <br>
<stock-s1gn :cSign6="stock6data.cSign6"></stock-s1gn>

</template>

<script>
import StockS1gn from './StockS1gn.vue'
import TotalScore from './TotalScore.vue'



export default {
  name: 'Stock6Sign',
  components: {
    StockS1gn,
    TotalScore
  },

  props: {

  }, 
  data(){
    const stock6data2 = {};
    return {
      stock6data2,
      stock6data: {},
      inputText2: '',
      result2: '',
      Url: '',
      cStockName: '',
      cNewestSeason: '',
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
          this.stock6data = response;
          this.stock6data2 = response;
          console.log(this.stock6data);
          this.cStockName = cStockName;
          this.cNewestSeason = cNewestSeason;
          
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
