<template>
  <div id="tab-bar">
    <slot></slot>
  </div>
</template>

<script>

export default {
  name: "TabBar"
}
</script>

<style scoped>
  #tab-bar{
    /*设置水平排列*/
    display: flex;
    /*设置背景颜色*/
    background-color: #f6f6f6;

    /*移动到最下面*/
    position: fixed;
    left: 0;
    right: 0;
    bottom: 0;

    /*设置阴影*/
    box-shadow: 0 -3px 1px rgba(100,100,100,.2);
  }

</style>