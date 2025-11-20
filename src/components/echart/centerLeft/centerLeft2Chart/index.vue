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
      cdata: [
        {
          // 名字需要与 "common/map/jiangsu.js" 地图数据文件里面定义的一一对应，不能是 "南京" 或者 "苏" 之类的缩写
          name: '南京市',
          value: 10,
          elseData:{
            // 这里放置地图 tooltip 里想显示的数据
          }
        },
        {
          name: '苏州市',
          value: 9,
        },
        {
          name: '无锡市',
          value: 8,
        },
        {
          name: '常州市',
          value: 7,
        },
        {
          name: '镇江市',
          value: 6,
        },
        {
          name: '扬州市',
          value: 5,
        },
        {
          name: '泰州市',
          value: 4,
        },
        {
          name: '南通市',
          value: 3,
        },
        {
          name: '盐城市',
          value: 2,
        },
        {
          name: '淮安市',
          value: 1,
        },
        {
          name: '宿迁市',
          value: 1,
        },
        {
          name: '徐州市',
          value: 1,
        },
        {
          name: '连云港市',
          value: 1,
        }
      ]
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