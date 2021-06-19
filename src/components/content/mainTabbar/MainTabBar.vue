<template>
  <tab-bar>
    <tab-bar-item path="/home">
      <template v-slot:item-icon>
        <img src="../assets/img/tabbar/首页.svg">
      </template>
      <template v-slot:item-icon-active>
        <img src="../assets/img/tabbar/首页_active.svg">
      </template>
      <template v-slot:item-text>
        <div>首页</div>
      </template>
    </tab-bar-item>

    <tab-bar-item path="category">
      <template v-slot:item-icon>
        <img src="../assets/img/tabbar/分类.svg">
      </template>
      <template v-slot:item-icon-active>
        <img src="../assets/img/tabbar/分类_active.svg">
      </template>
      <template v-slot:item-text>
        <div>分类</div>
      </template>
    </tab-bar-item>

    <tab-bar-item path="/cart">
      <template v-slot:item-icon>
        <img src="../assets/img/tabbar/购物车.svg">
      </template>
      <template v-slot:item-icon-active>
        <img src="../assets/img/tabbar/购物车_active.svg">
      </template>
      <template v-slot:item-text>
        <div>购物车</div>
      </template>
    </tab-bar-item>

    <tab-bar-item path="/profile">
      <template v-slot:item-icon>
        <img src="../assets/img/tabbar/我的.svg">
      </template>
      <template v-slot:item-icon-active>
        <img src="../assets/img/tabbar/我的_actice.svg">
      </template>
      <template v-slot:item-text>
        <div>我的</div>
      </template>
    </tab-bar-item>

  </tab-bar>
</template>

<script>
import TabBar from '../components/tabbar/TabBar'
import TabBarItem from '../components/tabbar/TabBarItem'


export default {
name: "MainTabBar",
  components:{
    TabBar,
    TabBarItem
  }
}
</script>

<style scoped>

</style>
