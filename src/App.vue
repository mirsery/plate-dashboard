<template>
  <div>
    <dv-full-screen-container>
      <div id="app">
        <div style="height:5%;width: 100%">
          <TitleVue/>
        </div>
        <div style="height:15%;width: 100%">
         <BodyTitle/>
        </div>
        <div style="height:50%;width: 100%">
          <BodyContent/>
        </div>
        <div style="height:25%;width: 100%">
          <BodyTail/>
        </div>

      </div>
    </dv-full-screen-container>
  </div>
</template>

<script>
import TitleVue from "./components/Title.vue"
import BodyTitle from "@/components/BodyTitle";
import BodyContent from "@/components/BodyContent";
import BodyTail from "@/components/BodyTail";

export default {
  name: 'App',
  components: {
    BodyTail,
    BodyContent,
    BodyTitle,
    TitleVue,
  }
}
</script>

<style>
#app {
  height: 100vh;
  width: 100vw;
  background-color: rgb(21, 24, 73);
  display: flex;
  justify-content: space-evenly;
  align-items: center;
  flex-direction: column;
  align-content: center;
}
</style>
