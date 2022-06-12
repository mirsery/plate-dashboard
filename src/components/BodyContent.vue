<template>
  <div style="height: 100%;width: 100%">
    <dv-border-box-10 style="height: 100%;width: 100%">
      <div style="display: flex;height: 100%;width: 100%">
        <div style="height: 100%;width: 25%;text-align: center">
          <div style="margin-top: 5%;color: rgba(89, 229, 245);font-size: 25px;">总收入分析</div>
          <dv-active-ring-chart :config="config" style="width:100%;height: 90%"/>
        </div>
        <div style="height: 96%;width: 50%;margin-top: 0.5%" id="map">

        </div>
        <div style="height: 100%;width: 25%">
          <div style="margin-top: 5%;color: rgba(89, 229, 245);font-size: 25px;">收入TOP10</div>
          <dv-capsule-chart :config="cap_config" style="width:90%;height:85%;"/>
        </div>
      </div>

    </dv-border-box-10>
  </div>
</template>

<script>
export default {
  name: "BodyContent",
  data() {
    return {
      config: {
        radius: '70',
        activeRadius: '75',
        lineWidth: 70,
        data: [
          {
            name: '支付宝',
            value: 554244
          },
          {
            name: '微信',
            value: 122230
          },
          {
            name: '现金',
            value: 71228
          },
          {
            name: '银行卡',
            value: 201221
          }
        ],
        digitalFlopStyle: {
          fontSize: 25
        },
        color: [ '#67e0e3', '#9fe6b8', '#ffdb5c', '#ff9f7f'],
        showOriginValue: true
      },
      cap_config: {
        data: [
          {
            name: 'A小区',
            value: 16733
          },
          {
            name: 'B小区',
            value: 12312
          },
          {
            name: 'C小区',
            value: 9834
          },
          {
            name: 'D小区',
            value: 7512
          },
          {
            name: 'E小区',
            value: 6621
          },
          {
            name: 'F小区',
            value: 9834
          },
          {
            name: 'G小区',
            value: 7512
          },
          {
            name: 'H小区',
            value: 6621
          },
          {
            name: 'I小区',
            value: 7512
          },
          {
            name: 'J小区',
            value: 6621
          }
        ],
        colors: ['#e062ae', '#fb7293', '#e690d1', '#32c5e9', '#37a2da', '#32c5e9', '#67e0e3', '#9fe6b8', '#ffdb5c', '#ff9f7f', '#fb7293'],
        unit: '元',
        showValue: true
      }
    }
  },
  methods: {
    initMaps() {

      window.init = function () {
        var map = new AMap.Map('map', {
          zoom: 16,
          center: [120.586497, 31.275735],
          resizeEnable: true,
          mapStyle: 'amap://styles/98ca64a58963dc7a53fdb499532981fe'
        })
      }
    }
  },
  mounted() {
    this.initMaps()
  }
}
</script>

<style scoped>
@font-face {
  font-family: LEDFont;
  src: url('../assets/font/UnidreamLED.ttf');
}

</style>
