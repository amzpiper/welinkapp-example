<template>
  <div class="App">
    <!-- header -->
    <Header :title="title" :show="isShow"></Header>

    <ul class="page">
      <li>
        <!-- defaultPage页面 -->
        <router-link to="/defaultPage" class="desc-link">{{$t('home.DefaultPage')}}</router-link>
      </li>
      <li>
        <router-link to="/fromView" class="desc-link">维修申请示例</router-link>
      </li>
      <li></li>
      <li></li>
      <li></li>
      <li></li>
    </ul>
  </div>
</template>

<script>
import Header from '../components/Header/Header';
import { mapState, mapActions } from 'vuex';
export default {
  name: 'Home',
  components: {
    Header: Header
  },
  data() {
    return {
      // 传输给header组件的标题
      title: '示例',
      // 传输给header组件的，是否显示返回箭头
      isShow: false
    };
  },
  created() {

  },
  computed: {
    ...mapState(['deviceInfo'])
  },
  methods: {
    ...mapActions(['getDeviceInfo'])
  }
};
</script>

<style lang="less" scoped>
// app
.App {
  padding-top: 70px;

  // 内容
  .page {

    // router-link样式
    .desc-link {
      display: block;
      line-height: 3em;
      border-bottom: 1px solid #ddd;
      color: #000;
      font-size: 14px;
      text-align: left;
      margin: 0 auto;
      padding-left: 15px;
    }
  }
}
</style>
