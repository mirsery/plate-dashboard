<template>
  <div>
    <dv-decoration-7 class="title">&nbsp;{{title}}&nbsp;</dv-decoration-7>
    <br/>
    <div class="content">
      <div class="content_body" v-for="item in data">
        <span>{{item.value}}</span><br/>
        <span>{{item.name}}</span>
      </div>
    </div>

  </div>
</template>

<script>
export default {
  name: "DigitalData",
  props:["title"],
  data() {
    return {
      "data": [
        {
          "name":"全年收入",
          "value":595684
        },
        {
          "name":"月度收入",
          "value":129392
        },
        {
          "name":"今日收入",
          "value":2735
        }
      ]
    }
  },
  methods:{
    updateData(data){
      this.data = data;
    }
  }
}
</script>

<style scoped>
@font-face {
  font-family: LEDFont;
  src: url('../assets/font/UnidreamLED.ttf');
}

.title {
  height: 10%;
  padding-top: 5%;
  color: rgba(89, 229, 245);
  font-size: 30px;
}

.content {
  display: flex;
  flex-wrap: nowrap;
  flex-direction: row;
  justify-content: space-evenly;
  align-items: center;
}

.content_body {
  color: rgba(89, 229, 245);
  height: 70%;
  font-size: 30px;
  font-family: LEDFont,fantasy;
  text-align: center;
}
.content_body >span:nth-child(1){
  font-size: 35px;
}


</style>
