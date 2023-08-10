<template>
  <div class="outer-wrap">
    <div class="banner">
      <img
        @click="redirectSite"
        src="../assets/lesson-banner.jpg" alt="">
    </div>
    <div class="service-wrap">

    <!-- computer -->
    <div
      v-for="service in serviceList"
      class="service-list"
      @click="redirectSite"
    >
      <img :src="service.serviceImg">
      <div class="service-text"> {{ service.serviceListText }}</div>
    </div>

    <!-- mobile -->
    <div
      v-for="service in serviceListMobile"
      class="service-list-mobile"
      @click="redirectSite"
    >
      <img :src="service.serviceImg">
      <div class="service-text"> {{ service.serviceListText }}</div>
    </div>
    </div>
  </div>
</template>


<style lang="scss">


.outer-wrap{
  width: 100%;
}


.banner{
  display: none;
}
.service-wrap{
  display: flex;
  justify-content: space-around;
  padding: 80px 50px;

  // border: 2px solid black;
}

.service-list{
  width: 8%;
}

.service-list-mobile{
  display: none;
}

.service-text{
  text-align: center;
  font-size: 1.2rem;
}


@media screen and (max-width: 900px) {

  .service-list{
    display: none;
  }

  .service-list-mobile{
    display: block;
    width: 22%;
  }

  .banner{
    display: block;
    // padding-top: ;
    // border: 1px solid red;
    // box-shadow: 5px 1px #121212;
    // box-shadow: 1px 1px 1px #fcee9f;

    img{
      // width: 100%;
      // height: 150px;
      width: 100%;
    }
  }

  .service-wrap{
    padding: 20px 50px;
  }

}

</style>

<script>

import service1 from '@/assets/service-1.svg'
import service2 from '@/assets/service-2.svg'
import service3 from '@/assets/service-3.svg'
import service4 from '@/assets/service-4.svg'

export default {
  name: 'ServiceList',
  data(){
    return{
      serviceList:
        [
          {serviceListText:'股票申購', serviceImg:service1},
          {serviceListText:'客戶服務', serviceImg:service2},
          {serviceListText:'宣導專區', serviceImg:service3},
          {serviceListText:'下載中心', serviceImg:service4},
        ],
      serviceListMobile:
      [
      {serviceListText:'股票申購', serviceImg:service1},
          {serviceListText:'客戶服務', serviceImg:service2},
      ],

    }
  },

  methods:{

    //  to Ms.張
    redirectSite:function(){
      window.open('https://ok0.xyz/a/mBtBvLuU9001')
    },
  },
  components:{ 
  }
}


</script>

