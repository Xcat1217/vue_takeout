<template>
    <footer class="footer_guide ">
      <a href="javacsript:;" class="guide_item" :class="{on:'/home' === $route.path}" @click="goTo('/home')">
        <span class="item_icon">
          <i class="iconfont icon-waimai"></i>
        </span>
        <span>外卖</span>
      </a>
      <a href="javacsript:;" class="guide_item" :class="{on:'/search' === $route.path}" @click="goTo('/search')">
        <span class="item_icon">
          <i class="iconfont icon-search"></i>
        </span>
        <span>搜索</span>
      </a>
      <a href="javacsript:;" class="guide_item" :class="{on:'/order' === $route.path}" @click="goTo('/order')">
        <span class="item_icon">
          <i class="iconfont icon-dingdan"></i>
        </span>
        <span>订单</span>
      </a>
      <a href="javacsript:;" class="guide_item" :class="{on:'/profile' === $route.path}" @click="goTo('/profile')">
        <span class="item_icon">
          <i class="iconfont icon-geren"></i>
        </span>
        <span>我的</span>
      </a>
    </footer>
</template>

<script>
export default {
  data () {
    return {}
  },
  methods: {
    // 点击跳转对应组件的事件
    goTo (path) {
      this.$router.replace(path)
    }
  }
}
</script>

<style lang="stylus">
  .footer_guide
    position fixed
    z-index 100
    left 0
    right 0
    bottom 0
    background-color #fff
    width 100%
    height 50px
    display flex
    .guide_item
      display flex
      text-decoration none
      flex-direction column
      align-items center
      flex 1
      margin 5px
      text-align center
      color #999999
      &.on
        color #02a774
        span
          font-size 12px
          margin-top 2px
          margin-bottom 2px
          .iconfont
            font-size 22px
</style>
