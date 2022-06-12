<template>
  <div style="display:flex;flex-wrap: nowrap;justify-content: space-evenly;height:100%">
    <dv-border-box-10>
      <div
          style="height: 90%;width: 100%;padding-top: 3%;display: flex;display: flex;justify-content: space-evenly;align-items: center;
color: aqua;text-align: center; font-family: LEDFont;">
        <div>
          <Icon size="50">
            <DirectionsCarSharp/>
          </Icon>
          <div style="font-size: 40px">2221</div>
          <div style="font-size: 25px">总车位数</div>
        </div>
        <div>
          <Icon size="50">
            <LocalParkingFilled/>
          </Icon>
          <div style="font-size: 40px">33</div>
          <div style="font-size: 25px">已用车位</div>
        </div>
        <div>
          <Icon size="50">
            <LocalParkingFilled/>
          </Icon>
          <div style="font-size: 40px">2221</div>
          <div style="font-size: 25px">剩余车位</div>
        </div>
        <div>
          <Icon size="50">
            <AccountTreeFilled/>
          </Icon>
          <div style="font-size: 40px">2221</div>
          <div style="font-size: 25px">总设备数</div>
        </div>
        <div>
          <Icon size="50">
            <PhoneIphoneFilled/>
          </Icon>
          <div style="font-size: 40px">433</div>
          <div style="font-size: 25px">手持设备数</div>
        </div>
        <div>
          <Icon size="50">
            <PeopleOutlineTwotone/>
          </Icon>
          <div style="font-size: 40px">122</div>
          <div style="font-size: 25px">工作人员人数</div>
        </div>
      </div>
    </dv-border-box-10>
    <dv-border-box-10 style="height: 100%;width: 100%">
      <div style="height: 100%;width: 100%;text-align: center">
        <div style="margin-top: 2%;color: rgba(89, 229, 245);font-size: 25px;">车辆进出记录</div>
        <div style="margin-top: 2%;width: 100%;height: 70%;display: flex">
          <dv-border-box-13>
            <div
                style="color: aqua;text-align: center;display: flex;height: 100%;flex-direction: column;flex-wrap: nowrap;justify-content: center;align-items: center;">
              <div>苏E88888</div>
              <div>A小区</div>
              <div>2022-06-11 11:10:00</div>
            </div>
          </dv-border-box-13>
          <dv-border-box-13>
            <div
                style="color: aqua;text-align: center;display: flex;height: 100%;flex-direction: column;flex-wrap: nowrap;justify-content: center;align-items: center;">
              <div>苏E88888</div>
              <div>A小区</div>
              <div>2022-06-11 11:10:00</div>
            </div>
          </dv-border-box-13>
          <dv-border-box-13>
            <div
                style="color: aqua;text-align: center;display: flex;height: 100%;flex-direction: column;flex-wrap: nowrap;justify-content: center;align-items: center;">
              <div>苏E88888</div>
              <div>A小区</div>
              <div>2022-06-11 11:10:00</div>
            </div>
          </dv-border-box-13>
          <dv-border-box-13>
            <div
                style="color: aqua;text-align: center;display: flex;height: 100%;flex-direction: column;flex-wrap: nowrap;justify-content: center;align-items: center;">
              <div>苏E88888</div>
              <div>A小区</div>
              <div>2022-06-11 11:10:00</div>
            </div>
          </dv-border-box-13>
          <dv-border-box-13>
            <div
                style="color: aqua;text-align: center;display: flex;height: 100%;flex-direction: column;flex-wrap: nowrap;justify-content: center;align-items: center;">
              <div>苏E88888</div>
              <div>A小区</div>
              <div>2022-06-11 11:10:00</div>
            </div>
          </dv-border-box-13>
        </div>
      </div>
    </dv-border-box-10>
  </div>
</template>

<script>
import {
  LocalParkingFilled,
  DirectionsCarSharp,
  AccountTreeFilled,
  PeopleOutlineTwotone,
  PhoneIphoneFilled
} from '@v2icons/material'
import {Icon} from '@v2icons/utils'

export default {
  name: "BodyTail",
  components: {
    DirectionsCarSharp,
    LocalParkingFilled,
    PeopleOutlineTwotone,
    PhoneIphoneFilled,
    AccountTreeFilled,
    Icon
  }
}
</script>

<style scoped>

</style>
