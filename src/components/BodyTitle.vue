<template>
  <div style="display:flex;flex-wrap: nowrap;justify-content: space-evenly;height:100%">
    <dv-border-box-10>
      <DigitalData title="手持机汇总(元)"></DigitalData>
    </dv-border-box-10>
    <dv-border-box-10>
      <DigitalData title="临停收费汇总(元)"></DigitalData>
    </dv-border-box-10>
    <dv-border-box-10>
      <DigitalData title="月租车汇总(元)"></DigitalData>
    </dv-border-box-10>
    <dv-border-box-10>
      <DigitalData title="车场汇总(元)"></DigitalData>
    </dv-border-box-10>
  </div>
</template>

<script>
import DigitalData from "@/components/DigitalData";

export default {
  name: "BodyTitle",
  components: {DigitalData}
}
</script>

<style scoped>

</style>
