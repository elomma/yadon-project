<template>
  <div id="app">


    <NavBar/>
    <Carrousel/>
    <ServiceList/>
    <FastInfo />
    <!-- <nav>
      <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link>
    </nav> -->
    <router-view/>
  </div>
</template>

<script>


import NavBar from '@/components/NavBar.vue'
import Carrousel from '@/components/Carrousel.vue'
import ServiceList from '@/components/ServiceList.vue'
import FastInfo from '@/components/FastInfo.vue'


export default {
  name: 'mainApp',
  components:{ 
    NavBar,
    Carrousel,
    ServiceList,
    FastInfo
  }
}
</script>

<style lang="scss">

html, body{
  margin:0;
  padding: 0;
}

</style>
