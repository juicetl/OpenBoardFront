<template>
  <div id="app">
   <router-view></router-view>
  </div>
</template>

<script>

export default {
  name: 'App',
  created(){
    this.openFullScreen()
  },
  methods:{
    openFullScreen: function(){
      console.log("loading...")
            //el-icon-loading
            const loading = this.$loading({
            lock: true,
            text: 'Loading',
            spinner: 'el-icon-loading',
            background: 'rgba(255, 255, 255, 1)'
            });
            setTimeout(() => {
                loading.close();
            }, 2000);
    }
  }
}
//font-family: 'Avenir', Helvetica, Arial, sans-serif;
</script>

<style>
#app {
  font-family: 'Times New Roman';
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  width: 100%;
  height: 100%;
  min-height:800px;
  
}

body{

  position: absolute;
  width: 99.5%;
  height: 99.5%;
  min-height:800px;
  background: #ffffff
}
body .vs-table colgroup.gutter{
    display: table-cell!important;
}
</style>

