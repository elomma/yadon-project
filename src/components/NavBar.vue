<template>
  <div>

  <!-- computer -->
  <div class="nav-wrap">
    <div class="nav-left">
      <img class='yadon-img' :src="logo">
      <div class="img-tri"></div>
    </div>
    <div class="nav-right">
      <div class="right-top">
        <span
          v-for="info in companyInfo"
          class="info-list"
        > {{ info }}
        </span>
      </div>
      <div class="right-bottom">
        <div 
          v-for="service in ServiceList"
          class="bottom-service"
        >
        {{ service }}
        </div>

        <!-- 登入下單按鈕 -->
        <div 
          class="bottom-btn btn-order"
        >
          登入下單
        </div>
        <div 
          class="bottom-btn btn-open"
        >
          立即開戶
        </div>
      </div>
    </div>
  </div>

  <!-- mobile -->
  <div class="nav-wrap-mobile">
    <div class="mobile-logo">
      <img class='yadon-img-mobile' :src="logo">
    </div>
    <div class="mobile-humburger">
      <div class="ham-line"></div>
      <div class="ham-line"></div>
      <div class="ham-line"></div>
    </div>
  </div>
  </div>
</template>


<style lang="scss">

.nav-wrap{
  display:flex;
  background-color: #333;
  height: 95px;
  // padding: 3px;
}

.yadon-img{
  z-index: 999;
  width: 320px;
  background: #e60012;
}

.img-tri{
    position: absolute;
    top: 0;
    left: 319px;
    border-style: solid;
    border-width: 95px 95px 0 0;
    border-color: #e60012 transparent transparent transparent;
}


.info-list{
  color: #fff;
  font-size: 1.15rem;
  font-family: Arial, 'Noto Sans TC', 'Microsoft JhengHei', Helvetica Neue, Helvetica, sans-serif;
  letter-spacing: 7px;
}
.nav-right{
  position: absolute;
  width: 75%;
  height: 95px;
  right:0;

  .right-top{
      display: flex;
      align-items: center;
      justify-content: end;
      height: 50%;
      color: white;

  }

  .right-bottom{
    display: flex;
    justify-content: end;
    align-items: center;

    height: 50%;
    color: white;
    width: 100%;
  }
}


.bottom-service{
  width: 15%;
  text-align: center;
  font-size: 1.25rem;
}

.bottom-btn{
  width: 15%;
  text-align: center;
  font-size: 1.35rem;
  border-radius: 100px;
  margin: 0 2px;
  padding: 5px;
}

.btn-order{
  border: 1px solid white;
}
.btn-open{
  background-color:red;
}

// mobile

.nav-wrap-mobile{
  z-index: 99;
  position: fixed;
  display:none;
  width: 100%;
  height: 65px;
  background-color: #e60012;
  padding: 10px 0;
}

.mobile-logo{
  width: 94%;
  height: 100%;
  // background-color: #fff;
  margin-right: auto;
}


.mobile-humburger{

  width: 6%;
  padding: 10px;

  .ham-line{
    height: 4px;
    background-color: #fff;
    margin: 8px 0;
  }
}
.yadon-img-mobile{
  z-index: 999;
  width: 215px;
  background: #e60012;
}



@media screen and (max-width: 1200px) {

  .nav-right{
  position: absolute;
  width: 70%;
  height: 95px;
  right:0;
  // font-size: 1rem;

  .right-top{

  }

  .right-bottom{

  }

  .bottom-btn{
    width: 10%;
    font-size: 1rem;
    padding: 5px;
  }
  }

}

@media screen and (max-width: 1100px) {
  .nav-wrap{
    display: none;
  }

  .nav-wrap-mobile{
    display: flex;
  }
}

</style>

<script>

import yadonLogo from "../assets/yadon-logo.svg"

export default {
  name: 'Navbar',
  data(){
    return{
      logo:yadonLogo,
      companyInfo:['遠東集團/', '關於亞東/','營業據點/','人才招募/','English'],
      ServiceList:['證券','期貨','債券','承銷','股務代理','投顧'],
      memberBtn:['登入下單','立即開戶'],
    }
  }
}
</script>

