<template>
  <div>
    <Chart :cdata="cdata" />
  </div>
</template>

<script>
import Chart from './chart.vue';
export default {
  data () {
    return {
      cdata: {
        xData: ["自建", "购置", "划拨", "置换", "其他"],
        seriesData: [
          { value: 10, name: "自建" },
          { value: 5, name: "购置" },
          { value: 15, name: "划拨" },
          { value: 25, name: "置换" },
          { value: 20, name: "其他" },
        ]
      }
    }
  },
  components: {
    Chart,
  },
  mounted () {
  },
  methods: {
  }
}
</script>

<style lang="scss" scoped>
</style>