<template>
  <div class="App">
    <!-- header -->
    <Header :title="title" :show="isShow"></Header>

    <!-- page -->
    <!-- <div class="weui-popedom-box">
      <div class="con">
        <i class="icon-big icon-big-nopermission"></i>
        <p class="tip guide">您暂无权限，去别处逛逛？</p>
      </div>
    </div>
    <div class="weui-popedom-box">
      <div class="con">
        <i class="icon-big icon-big-nodata"></i>
        <p class="tip guide">没有XXX，休息一下</p>
      </div>
    </div>
    <div class="weui-popedom-box">
      <div class="con">
        <i class="icon-big icon-big-pcbrower"></i>
        <p class="tip guide">请到PC上查看文件</p>
      </div>
    </div>
    <div class="weui-popedom-box">
      <div class="con">
        <i class="icon-big icon-big-networkoutage"></i>
        <p class="tip guide">网络不给力</p>
      </div>
    </div>
    <div class="weui-popedom-box">
      <div class="con">
        <i class="icon-big icon-big-busysystem"></i>
        <p class="tip guide">系统繁忙，请稍等一下</p>
      </div>
    </div>
    <div class="weui-popedom-box">
      <div class="con">
        <i class="icon-big icon-big-build"></i>
        <p class="tip guide">模块正在建设中</p>
      </div>
    </div>-->

    <div class="weui-popedom-box message-box">
      <div class="con">
        <i class="icon-big icon-big-noresource"></i>
        <p class="tip guide">茫茫大海，找不到页面</p>
      </div>
    </div>
  </div>
</template>

<script>
import Header from '../components/Header/Header';
import { mapState, mapActions } from 'vuex';
export default {
  name: 'DefaultPage',
  components: {
    Header: Header
  },
  data() {
    return {
      title: '找不到页面',
      isShow: true
    };
  },
  created() {},
  computed: {},
  methods: {}
};
</script>

<style lang="less" scoped>
.App {
  padding: 0em;
  
  .message-box{
    top:50px;
  }
}
</style>
