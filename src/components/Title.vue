<template>
  <div style="text-align:center">
    <dv-decoration-8 :color="['#2e6099', '#2e6099']" style="width:40%;height:5vh;float:left"/>
    <span class="pd_title">智慧停车场大数据平台</span>
    <dv-decoration-8 :color="['#2e6099', '#2e6099']" :reverse="true" style="width:40%;height:5vh;float:right"/>
    <div class="pd_LED_TIME">{{date}}&nbsp;&nbsp;&nbsp;{{time}}&nbsp;&nbsp;&nbsp;{{getWeekDate}}</div>
  </div>
</template>
<script>
export default {
  name: 'TitleVue',
  data() {
    return {
      time: ''
    }
  },
  methods: {
    timeRefresh() {
      let date = new Date();
      let hh = this.commonFormat(date.getHours());
      let mf = this.commonFormat(date.getMinutes());
      let ss = this.commonFormat(date.getSeconds());
      this.time = hh + " : " + mf + " : " + ss;
    },

    commonFormat(val){
      if(val < 10){
        if(val === 1){
          return "0 1";
        }
        return "0"+val;
      }

      if(Math.floor(val/10)===1){
        if(val % 10 === 1){
          return "  1  1  ";
        }
        return " 1 " + Math.floor(val/10);
      }
      if(val % 10===1){
        return Math.floor(val/10)+" "+1;
      }
      return val;
    },
    currentTime() {
      setInterval(this.timeRefresh, 500);
    },
  },
  created() {
    this.currentTime();
  },
  computed: {
    date(){
      let date = new Date();
      let yy = date.getFullYear();
      let mm = this.commonFormat(date.getMonth() + 1);
      let dd = this.commonFormat(date.getDate());
      return  yy + "-" + mm + "-" + dd;
    },
    getWeekDate() {
      let now = new Date();
      let day = now.getDay();
      let weeks = ["星期日", "星期一", "星期二", "星期三", "星期四", "星期五", "星期六"];
      return weeks[day];
    }
  }

}
</script>
<style scoped>
@font-face {
  font-family: LEDFont;
  src: url('../assets/font/UnidreamLED.ttf');
}

.pd_title {
  font-size: 40px;
  font-weight: bolder;
  color: rgba(89, 229, 245)
}

.pd_LED_TIME {
  font-size: xx-large;
  position: absolute;
  right: 100px;
  top: 0.5vh;
  color: white;
  font-family: LEDFont,"宋体";
  color: rgba(89, 229, 245)
}

</style>
