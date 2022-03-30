<template>
  <div id="app">
    <div id="titleBar" class="flex justify-end p-2 text-white">
      <div @click="minimize" class="mx-1 w-5 h-5 rounded-full bg-green-500 flex justify-center items-center font-bold hover:bg-green-700 transition-all">
        -
      </div>
      <div @click="close" class="mx-1 mr-2 w-5 h-5 rounded-full bg-red-500 flex justify-center items-center font-bold hover:bg-red-700 transition-all">
        x
      </div>
    </div>
    <router-view/>
  </div>
</template>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
#titleBar {
  -webkit-app-region: drag;
  background: #2A2A2A;
}
</style>

<script>
import 'electron'
export default {
  
  methods:{
    minimize(){
     remote.BrowserWindow.getFocusedWindow().minimize();
    },
    close(){

    }
  }
}
</script>