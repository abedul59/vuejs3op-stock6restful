<template>
    

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
    
</template>
      
<script>
      
      export default {
        name: 'TotalScore',
        components: {
      
        },
      
        props: {
          inputText2: String,
          cStockName: String,
          cNewestSeason: String,
          cSign1: String,
          cSign2: String,
          cSign3: String,
          cSign4: String,
          cSign5: String,
          cSign6: String,
          }, 
    
        data(){
          return {
        
          }
        },
      
        computed: {
      
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
      