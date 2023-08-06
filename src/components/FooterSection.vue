<template>
  <div class="Footer-section">
    <span>亞東證券股份有限公司</span>
    <br>
    <span>Oriental Securities Corporation</span>
    <br>
    <br>

    <!--  -->
    <ul class="footer-info">
      <li>週一至週五 交易日 8:00-17:00</li>
      <li>220 新北市板橋區新站路20號</li>
      <li>02-7753-1999</li>
      <li>0800-088-765(客服)</li>
      <li>service@oss.com.tw</li>
    </ul>
  </div>
</template>


<style lang="scss">

.Footer-section{
  box-sizing: border-box;
  letter-spacing: 2px;;
  padding: 35px 50px;
  width: 100%;
  background-color: #1e1e1e;
  color: rgb(239, 233, 233);
}

.footer-info{
  list-style: none;
  margin:0;
  padding:0;
  // color: white;
}
@media screen and (max-width: 800px) {

}


</style>

<script>

export default {
  name: 'FooterSection',
  data(){
    return{
    }
  },

  methods:{
    redirectSire:function(){
      window.open('https://line.me/ti/p/FGcBjHXZGD')
    },
  },
  components:{ 
  }
}


</script>

