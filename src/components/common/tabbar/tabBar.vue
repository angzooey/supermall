<template>
    <div id="tab-bar">
      <slot></slot>
    </div>
</template>

<script>
  export default {
    name: "tabBar"
  }
</script>

<style scoped>
  @import "../../assets/css/base.css";
  #tab-bar{
    display: flex;
    position: fixed;
    background-color: #f6f6f6;
    bottom: 0;
    left: 0;
    right: 0;
    box-shadow: 0 -3px 0px rgba(100,100,100,.1);
  }

</style>
