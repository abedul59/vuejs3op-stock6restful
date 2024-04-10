<template>
    

<div v-if="cSign2">
<table border="2" cellpadding="1" cellspacing="5"  style="border:1px solid black;margin-left:auto;margin-right:auto;">
<caption><FONT SIZE="6">營益率詳細資料</FONT></caption>



<tr>
<td align="center"><div><FONT SIZE="7">年季</FONT></div></td> <td align="center"><div><FONT SIZE="7">單位：%</FONT></div></td>
</tr>



<tr>
<td align="center" style="background-color:#9999CC;"><div><FONT SIZE="7">{{b1N}}</FONT></div></td>
 <td align="center"><div><FONT SIZE="7">{{b1}}</FONT></div></td>
</tr>

<tr>
<td align="center" style="background-color:#9999CC;"><div><FONT SIZE="7">{{b2N}}</FONT></div></td> 
<td align="center"><div><FONT SIZE="7">{{b2}}</FONT></div></td>
</tr>

<tr>
<td align="center" style="background-color:#9999CC;"><div><FONT SIZE="7">{{b3N}}</FONT></div></td> 
<td align="center"><div><FONT SIZE="7">{{b3}}</FONT></div></td>
</tr>

<tr>
<td align="center" style="background-color:#9999CC;"><div><FONT SIZE="7">{{b4N}}</FONT></div></td> 
<td align="center"><div><FONT SIZE="7">{{b4}}</FONT></div></td>
</tr>

<tr>
<td align="center" style="background-color:#9999CC;"><div><FONT SIZE="7">{{b5N}}</FONT></div></td> 
<td align="center"><div><FONT SIZE="7">{{b5}}</FONT></div></td>
</tr>

<tr>
<td align="center" style="background-color:#9999CC;"><div><FONT SIZE="7">{{b6N}}</FONT></div></td> 
<td align="center"><div><FONT SIZE="7">{{b6}}</FONT></div></td>
</tr>

<tr>
<td align="center" style="background-color:#9999CC;"><div><FONT SIZE="7">{{b7N}}</FONT></div></td> 
<td align="center"><div><FONT SIZE="7">{{b7}}</FONT></div></td>
</tr>


<tr>
<td align="center" style="background-color:#9999CC;"><div><FONT SIZE="7">{{b8N}}</FONT></div></td> 
<td><div align="center"><FONT SIZE="7">{{b8}}</FONT></div></td>
</tr>


<tr>
<td align="center" style="background-color:#2894FF;"><div><FONT SIZE="7">近四季平均</FONT></div></td>
 <td><div align="center"><FONT SIZE="7">{{b9}}</FONT></div></td>
</tr>


<tr>
<td align="center" style="background-color:#2894FF;"><div><FONT SIZE="7">最新一季季增率</FONT></div></td> 
<td><div align="center"><FONT SIZE="7">{{b10p}}</FONT></div></td>
</tr>

<tr>
<td align="center" style="background-color:#9999CC;"><div><FONT SIZE="7">評等</FONT></div></td> 
<td><div align="center"><FONT SIZE="7">{{cSign2}}</FONT></div></td>
</tr>
</table>


</div>
</template>
      
    <script>
      
      export default {
        name: 'StockS2gn',
        components: {
      
        },
      
        props: {
  
          cb1N: String,   
          cb2N: String,
          cb3N: String,
          cb4N: String,
          cb5N: String,
          cb6N: String,
          cb7N: String,
          cb8N: String,

          
          cb1: String,   
          cb2: String,
          cb3: String,
          cb4: String,
          cb5: String,
          cb6: String,
          cb7: String,
          cb8: String,
          cb9: String,
          cb10p: String,
          cSign2: String,
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
      