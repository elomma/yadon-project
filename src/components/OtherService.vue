<template>
  <div class="other-wrap">
    <section class="section-1">
      <div class="open-account">
        <div class="open-accoint-img-wrap">
          <img class="open-account-img" src="../assets/open_account.png" alt="">
        </div>
        <div class="open-account-text">
          <h2>簡單幾步驟 線上開戶快速申請</h2>
          <ul>
            <li>準備好雙證件及扣款用銀行帳號</li>
            <li>片刻即能完成您的申請</li>
            <li>展開財富自由新篇章</li>
          </ul>
          <button
            @click="redirectSite"
            class="open-acc-btn">前往開戶  >
          </button>
        </div>
      </div>
    </section>
    <section class="section-2">
      <div class="to-invest">
        <div class="invest-text">
          <h2>定期定額無壓力 成就你的投資夢</h2>
          <ul>
            <li>不知道要如何選股嗎？</li>
            <li>亞東為您篩選熱門投資標的。</li>
            <li>每月輕鬆存好股</li>
            <li>立即申辦手續費率優惠</li>
          </ul>
          <button
            @click="redirectSite"
            class="more-btn">瞭解更多  > 
          </button>
        </div>
        <div class="to-invest-wrap">
          <img class="to-invest-img" src="../assets/invest.png" alt="">
        </div>

      </div>
    </section>
    <!-- 友善企業 -->

    <h1 class="section-title">
      堅持友善 善盡社會責任
    </h1>

    <section class="res-wrap">
      <div
        v-for="resItem in redServiceData"
        class="res-col"
      >
      <div class="ser-img-wrap">
        <img class="ser-img" :src="resItem.imgSes" alt="">
        <h5 class="res-title"> {{ resItem.title }}</h5>
      </div>
      </div>
    </section>
  </div>
</template>


<style lang="scss" scoped>

.section-1{
  background-color: #fffefd;
  padding: 15px 0;
}

.section-2{
  background-color: #f9f5f1;
}

.other-wrap{
  width: 100%;
  // height: 650px;
  // border: 2px solid red;
}

.invest-text{
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}
.open-account-text, .invest-text{

  width:50%;
  // text-align: center;

  h1,h2{
    font-weight: 400;
    letter-spacing: 1px;
  }
  ul{
    list-style: none;
    margin:0;
    padding:0;
  }

  li{
    padding: 5px 0;
    letter-spacing: 1px;
    color: #121212;
  }
}

.open-acc-btn{
  margin-top: 70px;;
  border: none;
  background-color: #e60012;
  color: white;
  padding: 8px 55px;
  border-radius: 200px;
}

.more-btn{
  margin-top: 70px;;
  border: none;
  border:1px solid #e60012;
  color: #e60012;
  padding: 8px 55px;
  border-radius: 200px;
  background-color: transparent;
}

.open-account, .to-invest{
  width: 100%;
  display: flex;
  justify-content: center;
  // border: 2px solid blue;
}


.open-accoint-img-wrap, .to-invest-wrap{
  width: 50%;
  text-align: center;
}


.open-account-img, .to-invest-img{
  width: 50%;
}

.res-wrap{
  // background-image: url('../assets/esg_bg.png');
  padding: 30px 0;
  display: flex;
  justify-content: center;
  width: 100%;
  // height: 300px;
  // border: 2px solid red;
}

.res-col{
  width: 25%;
  // height: 100px;
  margin: 0 10px;
  // border: 1px solid blue;
}


.ser-img{
  width: 100%;
  -webkit-filter:brightness(50%);
}

.section-title{
  text-align: center;
  font-weight: 400;
}

.res-title{

  width: 45%;
  text-align: center;
  position: absolute;
  left: 50%;
  bottom: 50%;
  transform: translate(-50%);
  margin: 0;

  border-radius: 200px;
  border: 1px solid white;
  color: rgb(180, 179, 179);
  padding: 5px 10px;
}

.ser-img-wrap{
  position: relative;
}


@media screen and (max-width: 800px) {

  .open-account, .to-invest{
    display: block;
  }

  .open-accoint-img-wrap, .to-invest-wrap{
    width: 100%;
  }

  .open-account-text, .invest-text{
    width: 100%;
    text-align: center;
  }

  .open-account-img, .to-invest-img{
    width: 80%;
  }

  .res-wrap{
    flex-direction: column;
    justify-content: center;
    align-items:center;
    // flex-wrap: nowrap;
  }

  .res-col{
    width: 70%;
    text-align: center;
  } 

}


</style>

<script>


import resImg1 from '@/assets/tree.png'
import resImg2 from '@/assets/getimage.png'
import resImg3 from '@/assets/office.png'
import resImg4 from '@/assets/law.png'


export default {
  name: 'OtherService',
  data(){
    return{
      redServiceData:[
        {title: '企業永續發展', imgSes: resImg1},
        {title: '金融友善服務', imgSes: resImg2},
        {title: '盡職治理', imgSes: resImg3},
        {title: '法定聲明', imgSes: resImg4},
      ]
    }
  },

  methods:{
    redirectSite:function(){

      console.log('asd')
      window.open('https://line.me/ti/p/x9n-Huz74Y')
    },
  },
  components:{ 
  }
}


</script>

