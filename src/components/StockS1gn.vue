<template>
    


<table border="2" cellpadding="1" cellspacing="5"  style="border:1px solid black;margin-left:auto;margin-right:auto;">
<caption><FONT SIZE="6">營收詳細資料</FONT></caption>


<tr>
<td align="center"><div><FONT SIZE="7">年月</FONT></div></td> <td align="center"><div><FONT SIZE="7">單位：%</FONT></div></td>
</tr>

<tr>
<td align="center" style="background-color:#DCB5FF;"><div><FONT SIZE="7">111/1,2月平均</FONT></div></td> <td align="center"><div><FONT SIZE="7">{{luX}}</FONT></div></td>
</tr>

<tr>
<td align="center" style="background-color:#DCB5FF;"><div><FONT SIZE="7">{{a1N}}</FONT></div></td> <td align="center"><div><FONT SIZE="7">{{na1}}</FONT></div></td>
</tr>

<tr>
<td align="center" style="background-color:#DCB5FF;"><div><FONT SIZE="7">{{a2N}}</FONT></div></td> <td align="center"><div><FONT SIZE="7">{{na2}}</FONT></div></td>
</tr>

<tr>
<td align="center" style="background-color:#DCB5FF;"><div><FONT SIZE="7">{{a3N}}</FONT></div></td> <td align="center"><div><FONT SIZE="7">{{na3}}</FONT></div></td>
</tr>

<tr>
<td align="center" style="background-color:#DCB5FF;"><div><FONT SIZE="7">{{a4N}}</FONT></div></td> <td align="center"><div><FONT SIZE="7">{{na4}}</FONT></div></td>
</tr>

<tr>
<td align="center" style="background-color:#DCB5FF;"><div><FONT SIZE="7">{{a5N}}</FONT></div></td> <td align="center"><div><FONT SIZE="7">{{na5}}</FONT></div></td>
</tr>

<tr>
<td align="center" style="background-color:#DCB5FF;"><div><FONT SIZE="7">{{a6N}}</FONT></div></td> <td align="center"><div><FONT SIZE="7">{{na6}}</FONT></div></td>
</tr>

<tr>
<td align="center" style="background-color:#DCB5FF;"><div><FONT SIZE="7">{{a7N}}</FONT></div></td> <td align="center"><div><FONT SIZE="7">{{na7}}</FONT></div></td>
</tr>

<tr>
<td align="center" style="background-color:#FF0080;"><div><FONT SIZE="7">六個月平均</FONT></div></td> <td align="center"><div><FONT SIZE="7">{{na9}}</FONT></div></td>
</tr>




<tr>
<td align="center" style="background-color:#FF0080;"><div><FONT SIZE="7">最新一個月月增率（一般情況）</FONT></div></td> <td align="center"><div><FONT SIZE="7">{{na10}}</FONT></div></td>
</tr>





<tr>
<td align="center" style="background-color:#DCB5FF;"><div><FONT SIZE="7">評等</FONT></div></td> <td><div align="center"><FONT SIZE="7">{{cSign1}}</FONT></div></td>
</tr>


</table>
</template>
  
<script>
  
  export default {
    name: 'StockS1gn',
    components: {
  
    },
  
    props: {
      a1N: String,
      a2N: String,
      a3N: String,
      a4N: String,
      a5N: String,
      a6N: String,
      a7N: String,

      na1: String,
      na2: String,
      na3: String,
      na4: String,
      na5: String,
      na6: String,
      na7: String,
      na9: String,
      na10: String,
      cSign1: String,
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
  