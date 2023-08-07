<template>
  <div class="service-wrap">

    <!-- computer -->
    <div
      v-for="service in serviceList"
      class="service-list"
      @click="redirectSire"
    >
      <img :src="service.serviceImg" alt="">
      <div class="service-text"> {{ service.serviceListText }}</div>
    </div>

    <!-- mobile -->
    <div
      v-for="service in serviceListMobile"
      class="service-list-mobile"
      @click="redirectSire"
    >
      <img :src="service.serviceImg" alt="">
      <div class="service-text"> {{ service.serviceListText }}</div>
    </div>
  </div>
</template>


<style lang="scss">


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


@media screen and (max-width: 800px) {

  .service-list{
    display: none;
  }

  .service-list-mobile{
    display: block;
    width: 25%;
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
    redirectSire:function(){
      window.open('https://line.me/ti/p/xBwukU2BYG')
    },
  },
  components:{ 
  }
}


</script>

