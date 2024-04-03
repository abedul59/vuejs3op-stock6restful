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
  
<div v-if="cSign1">

<table border="2" cellpadding="1" cellspacing="5"  style="border:1px solid black;margin-left:auto;margin-right:auto;">
<caption><FONT SIZE="6">六大指標</FONT></caption>
<tr>	
<td style="background-color:#D3A4FF;" align="center"><div><FONT SIZE="7">台股代號：</FONT></div></td>
<td align="center"><div><FONT SIZE="7">{{inputText2}}</FONT></div></td>
</tr>

<tr>	
<td style="background-color:#D3A4FF;" align="center"><div><FONT SIZE="7">股票名稱：</FONT></div></td>
<td align="center"><div><FONT SIZE="7">{{cStockName}}</FONT></div></td>
</tr>

<tr>	
<td style="background-color:#D3A4FF;" align="center"><div><FONT SIZE="7">最新財報季度：</FONT></div></td>
<td align="center"><div><FONT SIZE="7">{{cNewestSeason}}</FONT></div></td>
</tr>

<tr>	
<td style="background-color:#FFA6FF;" align="center"><div><FONT SIZE="7">營收評等：</FONT></div></td>
<td align="center"><div><FONT SIZE="7">{{cSign1}}</FONT></div></td>
</tr>

<tr>	
<td style="background-color:#FFA6FF;" align="center"><div><FONT SIZE="7">營益率評等：</FONT></div></td>
<td align="center"><div><FONT SIZE="7">{{cSign2}}</FONT></div></td>
</tr>

<tr>	
<td style="background-color:#FFA6FF;" align="center"><div><FONT SIZE="7">稅後淨利評等：</FONT></div></td>
<td align="center"><div><FONT SIZE="7">{{cSign3}}</FONT></div></td>
</tr>

<tr>	
<td style="background-color:#FFA6FF;" align="center"><div><FONT SIZE="7">EPS評等：</FONT></div></td>
<td align="center"><div><FONT SIZE="7">{{cSign4}}</FONT></div></td>
</tr>

<tr>	
<td style="background-color:#FFA6FF;" align="center"><div><FONT SIZE="7">存貨週轉率評等：</FONT></div></td>
<td align="center"><div><FONT SIZE="7">{{cSign5}}</FONT></div></td>
</tr>

<tr>	
<td style="background-color:#FFA6FF;" align="center"><div><FONT SIZE="7">現金流量評等：</FONT></div></td>
<td align="center"><div><FONT SIZE="7">{{cSign6}}</FONT></div></td>
</tr>

<tr>	
<td style="background-color:#FF2D2D;" align="center"><div><FONT SIZE="7">總平均：</FONT></div></td>
<td align="center"><div><FONT SIZE="7">{{average6stock}}</FONT></div></td>
</tr>
</table>

 </div>
 <br>
 <br>



</template>

<script>
//import StockSign1 from './components/StockSign1.vue'
export default {
  name: 'Stock6Sign',
  components: {

  },

  props: {

  }, 
  data(){
    return {
      stock6data: "",
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
