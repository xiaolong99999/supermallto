<template>
  <div class="tab-bar-item" @click="itemClick">
    <div v-if="!isActive"><slot  name="item-icon"></slot></div>
    <div v-else><slot name="item-icon-active"></slot></div>
<!--    <div v-bind:class="{active:isActive}"><slot name="item-text"></slot></div>-->
    <div :style="activeStyle"><slot name="item-text"></slot></div>
  </div>
</template>

<script>
export default {
  name: "TabBarItem",
  props:{
    path:String,
    activeColor:{
      type:String,
      // 默认红色
      default:'red'
    }

  },
  data(){
    return {
      // isActive:false
    }
  },
  computed:{
    // 判断点击的path
    isActive(){
      return this.$route.path.indexOf(this.path) !==-1
    },

    // 处于活跃状态就使用this.cativecolor 非活跃默认为空

    activeStyle(){
      return this.isActive ? {color:this.activeColor} : {}
    }


  },
  methods:{
    itemClick(){
      this.$router.replace(this.path)
    }
  }
}
</script>

<style scoped>
  .tab-bar-item{
    /*平均分配宽度*/
    flex: 1;
    /*居中显示*/
    text-align: center;
    /*tabbar一般高度*/
    height: 49px;
    font-size: 14px;
  }

  .tab-bar-item img{
    width: 24px;
    height: 24px;
    margin-top: 3px;
    /*去除图片下面的3像素*/
    vertical-align: middle;
    margin-bottom: 2px;
  }


</style>
