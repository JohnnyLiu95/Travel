<template>
    <div class="header">
        <div class="header-left">
          <span class="iconfont icon-back"></span>
        </div>
        <div class="header-input">
          <span class="iconfont icon-search"></span>
          输入城市/景点/游玩主题
        </div>
        <div class="header-right">
          城市
          <span class="iconfont icon-dropdown"></span>
        </div>
    </div>
</template>

<script>
export default {
  name: 'HomeHeader'
}
</script>

<style lang="stylus" scoped>
  .header
    display: flex
    height: .86rem
    background: #00bcd4
    line-height: .86rem
    color: #fff
    .header-left
      width: .64rem
      text-align: center
    .header-input
      flex: 1
      height: .64rem
      margin-top: .12rem
      margin-left: .2rem
      background: #fff
      border-radius: .1rem
      line-height: .64rem
      color: #ccc;
      padding-left: .2rem
    .header-right
      width: 1.24rem
      float: right
      text-align: center
      span
        font-size: .16rem

</style>
