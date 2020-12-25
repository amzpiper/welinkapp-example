<template>
  <header class="App-header">
    <!-- back按钮 -->
    <router-link to="/" v-if="show" >
      <img id="back" :src="backImg" />
    </router-link>
    <router-link to="/" v-if="!show">
      <i class="icon-24 icon-24-sort tab-business"></i>
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
  position: fixed;
  width: 100%;
  top:0px;
  z-index: 99999999;
  height: 50px;
  color: #fff;
  text-align: center;
  line-height: 50px;
  background-color: #343745;
  // background-color: #fff;
  padding-top:20px;
  border-bottom: 1px solid #aaa;
}

header #back {
  position: absolute;
  top: 29px;
  left: 6px;
  width: 32px;
  height: 32px;
}
header .tab-business{
  position: absolute;
  top: 33px;
  left: 10px;
}
</style>
