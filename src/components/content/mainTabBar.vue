<template>
  <tab-bar>
    <tab-bar-item link="/home" activeColor="#d4237a">
      <img slot="item-icon" src="~assets/img/tabbar/home.png" alt="">
      <img  slot="item-icon-active" src="~assets/img/tabbar/home-active.png" alt="">
      <div slot="item-text">首页</div>
    </tab-bar-item>

    <tab-bar-item link="/category">
      <img slot="item-icon" src="~assets/img/tabbar/modular.png" alt="">
      <img slot="item-icon-active" src="~assets/img/tabbar/modular-active.png" alt="">
      <div slot="item-text">分类</div>
    </tab-bar-item>

    <tab-bar-item link="/cart">
      <img slot="item-icon" src="~assets/img/tabbar/cart.png" alt="">
      <img slot="item-icon-active" src="~assets/img/tabbar/cart-active.png" alt="">
      <div slot="item-text">购物车</div>
    </tab-bar-item>

    <tab-bar-item link="/profile">
      <img slot="item-icon" src="~assets/img/tabbar/user.png" alt="">
      <img slot="item-icon-active" src="~assets/img/tabbar/user-active.png" alt="">
      <div slot="item-text">我的</div>
    </tab-bar-item>

  </tab-bar>
</template>

<script>

  import TabBar from 'components/common/tabbar/tabBar'
  import tabBarItem from 'components/common/tabbar/tabBarItem'

  export default {
    name: "mainTabBar",
    components:{
      TabBar,
      tabBarItem
    },
  }
</script>

<style scoped>

</style>
