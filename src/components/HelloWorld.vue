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

<table border="2" cellpadding="1" cellspacing="5"  style="border:1px solid black;margin-left:auto;margin-right:auto;">
<caption><FONT SIZE="6">六大指標</FONT></caption>
<tr>	
<td style="background-color:#D3A4FF;" align="center"><div><FONT SIZE="7">台股代號：</FONT></div></td>
<td align="center"><div><FONT SIZE="7">{{mess}}</FONT></div></td>
</tr>

<tr>	
<td style="background-color:#D3A4FF;" align="center"><div><FONT SIZE="7">股票名稱：</FONT></div></td>
<td align="center"><div><FONT SIZE="7">{{stock_name}}</FONT></div></td>
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
