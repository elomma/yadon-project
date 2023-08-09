<template>
  <div class="fast-info-out-wrap">
    <h1 class="info-title">即時動態</h1>
    <section class="section-wrap">    
      <div class="info-left">
        <div class="button-wrap">
          <button class="info-btn btn-active">公告</button>
          <button class="info-btn">最新消息</button>
          <button class="info-btn">反詐騙專區</button>
        </div>
        <div class="info-test">
          <ul>
            <li>【集保】投資人 eNotice 抽獎活動，多重好康等著您</li>
            <li>亞東證券全新官網精彩上線</li>
            <li>發現假冒遠東集團名義之網路詐騙管道</li>
          </ul>
        </div>
        <div class="more-wrap">
          <button class="read-more">Read More</button>
        </div>
      </div>
      <!-- <div class="info-mid"></div> -->
      <div class="info-right">
        <h1 class="photo-title">大盤走勢</h1>
        <img src="../assets/stockImg.png" alt="">
      </div>
    </section>
  </div>
</template>


<style lang="scss" scoped>

.info-title{
  text-align: center;
  color: #333;
  letter-spacing: 0.14rem;
  margin:0;
  font-weight: 400;
  margin-bottom: 30px;
}

.fast-info-out-wrap{
  // display: flex;
  width: 100vw;
  // height: 250px;
  background-color: #dee5ef;
  box-sizing: border-box;
  padding: 50px 20px;

}

.section-wrap{
  display: flex;
}

.info-left, .info-right{
  width: 50%;
  height: 500px;
}
.info-right{
  text-align: center;
  img{
    width: 50%
  }
}


.info-btn{
  padding: 6px 12px;
  margin: 5px;
  border-radius: 200px;
  // width: 100px;
  border: none;
  font-size: 1.25rem;
  font-weight: bold;
  color: #b9a796;
  border: 1px solid #b9a796;
  background-color: transparent;
  letter-spacing: 1px;
}

.info-test{
  letter-spacing: 4px;
  li{
    padding: 3px 0;
    color: #333;
    font-size: 1.2rem;
  }
}

.btn-active{
  background-color:#b9a796;
  color: white;
}



.photo-title{
  font-weight: 350;
}

.read-more{
  border: 1px solid #121212;
  background-color: transparent;
  border-radius: 200px;
  padding: 6px 25px;
  font-size: 1rem;
  color: #333;
}


@media screen and (max-width: 800px) {
  .section-wrap{
    display: block
  }

  .info-left, .info-right{
    width: 100%;
    height: auto;
  }
  .info-right{
    text-align: center;
    margin: 50px 0;
    img{
      width: 65%
    }
  }

  .info-test{
    letter-spacing: 1px;
    li{
      padding: 2px 0;
      color: #333;
      font-size: 1rem;
    }
}

}

</style>

<script>

// import service1 from '@/assets/service-1.svg'
// import service2 from '@/assets/service-2.svg'
// import service3 from '@/assets/service-3.svg'
// import service4 from '@/assets/service-4.svg'

export default {
  name: 'FastInfo',
  data(){
    return{
    }
  },
}


</script>

