<template>
  <header class="App-header">
    <!-- back按钮 -->
    <router-link to="/" v-if="show" >
      <img id="back" :src="backImg" />
    </router-link>
    <router-link to="/" v-if="!show">
      <i class="icon-tab icon-tab-business tab-business"></i>
    </router-link>
    <!-- 标题 -->
    {{ title }}
    <!-- 客服按钮 -->
  </header>
</template>

<script>
import backImg from './images/back.png';

export default {
  name:'Header',
  props: {
    to:String,        //header返回上层的地址
    title: String,    //header标题
    show:Boolean      //header标题是否显示返回
  },
  data() {
    return {
      backImg,
    };
  },
};
</script>

<style lang="less" scoped>
header {
  position: relative;
  width: 100%;
  top:0px;
  z-index: 99999999;
  height: 50px;
  color: #fff;
  text-align: center;
  line-height: 50px;
  background-color: #343745;
}

header #back {
  position: absolute;
  top: 9px;
  left: 6px;
  width: 32px;
  height: 32px;
}
header .tab-business{
  position: absolute;
  top: 13px;
  left: 10px;
  color: #fff;
}
</style>
