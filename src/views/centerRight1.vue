<template>
  <div id="centerRight1">
    <div class="bg-color-black">
      <div class="d-flex pt-2 pl-2">
        <span>
          <icon name="chart-line" class="text-icon"></icon>
        </span>
        <div class="d-flex">
          <span class="fs-xl text mx-2">任务完成排行榜</span>
        </div>
      </div>
      <div class="d-flex jc-center body-box">
        <dv-scroll-board class="dv-scr-board" :config="config" />
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      config: {
        header: ['地市', '闲置整改完成数量（处）'],
        data: [
          ['苏州', "<span  class='colorGrass'>90%</span>"],
          ['常州', "<span  class='colorGrass'>80%</span>"],
          ['无锡', "<span  class='colorGrass'>70%</span>"],
          ['宿迁', "<span  class='colorGrass'>64%</span>"],
          ['南通', "<span  class='colorGrass'>55%</span>"],
          ['连云港', "<span  class='colorGrass'>43%</span>"],
          ['淮安', "<span  class='colorGrass'>34%</span>"],
          ['盐城', "<span  class='colorGrass'>26%</span>"],
          ['扬州', "<span  class='colorGrass'>13%</span>"],
          ['镇江', "<span  class='colorGrass'>9%</span>"]
        ],
        rowNum: 7, //表格行数
        headerHeight: 35,
        headerBGC: '#0f1325', //表头
        oddRowBGC: '#0f1325', //奇数行
        evenRowBGC: '#171c33', //偶数行
        index: true,
        indexHeader: '排名',
        columnWidth: [60, 80, 200],
        align: ['center', 'center', 'center']
      }
    }
  }
}
</script>

<style lang="scss" scoped>
$box-height: 410px;
$box-width: 300px;
#centerRight1 {
  padding: 16px;
  padding-top: 20px;
  height: $box-height;
  width: $box-width;
  border-radius: 5px;
  .bg-color-black {
    height: $box-height - 30px;
    border-radius: 10px;
  }
  .text {
    color: #c3cbde;
  }
  .body-box {
    border-radius: 10px;
    overflow: hidden;
    .dv-scr-board {
      width: 270px;
      height: 340px;
    }
  }
}
</style>
