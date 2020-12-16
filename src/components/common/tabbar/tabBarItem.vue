<template>
  <div class="tab-bar-item" @click="itemClick">
    <div  v-if="!isActive">
      <slot name="item-icon"></slot>
    </div>
    <div v-else>
      <slot  name="item-icon-active"></slot>
    </div>
    <div  :style="activeStyle">
      <slot  name="item-text"></slot>
    </div>

<!--    <img src="../../assets/img/tabbar/home.png" alt="">-->
<!--    <div>首页</div>-->
  </div>
</template>

<script>
  export default {
    name: "tabBarItem",
    props:{
      link:String,
      activeColor:{
        type:String,
        default:'#d4237a'
      }
    },
    data(){
      return{
        // isActive:true,
      }
    },
   computed:{
     isActive(){
       //$route活跃路由
        return this.$route.path.indexOf(this.link) !== -1
      },
     activeStyle(){
       return this.isActive ? {color :this.activeColor} : {}
     }
   },
    methods:{
      itemClick(){
        console.log("itemcclr")
        this.$router.replace(this.link)
      }
    }
  }
</script>

<style scoped>


  .tab-bar-item{
    flex: 1;
    text-align: center;
    height: 49px;
    font-size: 14px;

  }
  .tab-bar-item img{
    width: 24px;
    height: 24px;
    vertical-align: middle;
    margin-top: 3px;

  }

</style>
