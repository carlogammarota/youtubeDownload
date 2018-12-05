<template>
  <div id="app">
    <headerComponent/>
    <contenidoComponent/>
    <!-- <img src="./assets/logo.png"> -->
    <!-- <router-view/> -->
    <!-- <h1>asd</h1> -->
    <tableComponent/>
    <footerComponent/>
    
  </div>
</template>

<script>

import headerComponent from "@/components/headerComponent";
import footerComponent from "@/components/footerComponent";
import contenidoComponent from "@/components/contenidoComponent";
import tableComponent from "@/components/tablaVideos";
import Vue from 'vue'
//import BootstrapVue from 'bootstrap-vue'



//import 'bootstrap/dist/css/bootstrap.css'
import 'bootstrap-vue/dist/bootstrap-vue.css'

import Buefy from 'buefy'
import 'buefy/dist/buefy.css'

Vue.use(Buefy)

import Vuetify from 'vuetify'
 
Vue.use(Vuetify)



export default {
  name: 'App',
  components: {
    headerComponent,
    footerComponent,
    contenidoComponent,
    tableComponent
  }
}
</script>

<style>
#app {
  font-family: 'Bungee';
  text-transform: uppercase;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;

  color: #2c3e50;

}
</style>
