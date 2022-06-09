<template>
  <div id="app">
    <dv-full-screen-container>
      <div style="height:10%;">
        <TitleVue/>
      </div>
      <div style="height:85%;">
        <BodyMainVue/>
      </div>
    </dv-full-screen-container>
  </div>
</template>

<script>
import TitleVue from "./components/Title.vue"
import BodyMainVue from "./components/BodyMain.vue"
export default {
  name: 'App',
  components:{
    TitleVue,
    BodyMainVue
  }
}
</script>

<style>
#app {
  height: 100vh;
  width: 100vw;
  background-color: rgb(40, 42, 54);
  display: flex;
    flex-direction: column;
    justify-content: space-between;
    align-items: center;
    flex-wrap: nowrap;
}
</style>
