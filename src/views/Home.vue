<template>
  <div class="App">
    <!-- header -->
    <Header :title="title" :show="isShow"></Header>

    <ul class="page">
      <li>
        <!-- vueTemplateIntro -->
        <router-link to="/vueTemplateIntro" class="desc-link">{{$t('home.wlkVueTemplateIntro')}}</router-link>
      </li>
      <li>
        <!-- UI练习 -->
        <!-- defaultPage页面 -->
        <router-link to="/defaultPage" class="desc-link">{{$t('home.DefaultPage')}}</router-link>
      </li>
      <li></li>
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
      title: '示例',
      isShow: false
    };
  },
  created() {},
  computed: {
    ...mapState(['deviceInfo'])
  },
  methods: {
    ...mapActions(['getDeviceInfo'])
  }
};
</script>

<style lang="less" scoped>
.App {
  padding: 0px;

  .page {
    .desc-link {
      display: block;
      line-height: 3em;
      border-bottom: 1px solid #f5f5f5;
      color: #000;
      font-size: 14px;
      text-align: left;
      margin: 0 auto;
      padding-left: 15px;
    }
  }
}
</style>
