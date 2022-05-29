<template>
  <h1 class="header-container" :style="{backgroundColor:bgColor,color:color,fontSize:fSize+'px'}">{{title}}</h1>
</template>

<script>
export default {
  name: 'Header',
  props: {
    title: {
      type: String,
      default: '標題'
    },
    bgColor: {
      type: String,
      default: 'rgb(38, 176, 148)'
    },
    color: {
      type: String,
      default: 'white'
    },
    fSize: {
      type: Number,
      default: 12
    }
  }
}
</script>

<style lang="less" scoped>
.header-container{
  position: fixed;
  width: 100%;
  top:0;
  height: 45px;
  line-height: 45px;
  text-align: center;
  z-index: 9;
}
</style>