<template>
  <div class="App">
    <!-- header -->
    <Header :title="title" :show="isShow"></Header>

    <div class="page" style="background: #fff;">
      <!-- cell -->
      <div class="weui-cells">
        <!-- 1 -->
        <div class="weui-listview-box">
          <div class="weui-listview-box__bg">
            <div class="weui-listview-title">
              AI系列培训-Introduction to AI &
              ML-分布式与并行与交流，分布式与并行与交流,分布式与并行与交流，分布式与并行与交流,分布式与并行与交流，分布式与并行与交流
            </div>
            <div class="weui-listview-footer">
              <span>01-14 00:00</span>
            </div>
            <div class="weui-listview-footer">
              <span>已处理</span>
              -
              <span>蔡瑁</span>
            </div>
          </div>
        </div>
        <!-- 2 -->
        <div class="weui-listview-box">
          <div class="weui-listview-box__bg">
            <div class="weui-listview-title">
              AI系列培训-Introduction to AI &
              ML-分布式与并行与交流，分布式与并行与交流,分布式与并行与交流，分布式与并行与交流,分布式与并行与交流，分布式与并行与交流
            </div>
            <div class="weui-listview-footer">
              <span>01-14 00:00</span>
            </div>
            <div class="weui-listview-footer">
              <span>已处理</span>
              -
              <span>蔡瑁</span>
            </div>
          </div>
        </div>
      </div>
      <!-- 创建申请 -->
      <div class="">

      </div>
    </div>
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
      title: '维修申请',
      // 传输给header组件的，是否显示返回箭头
      isShow: true
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
// app
.App {
  padding-top: 70px;

  // 内容
  .page {
    padding: 0px 10px;
    .weui-cells {
      margin-top: 0em;
    }
    .weui-listview-box {
      border-bottom: 1px solid #ddd;
    }
    .weui-listview-title {
      font-size: 0.9em;
    }
    .weui-listview-footer {
      font-size: 0.7em;
      display: block;
    }
  }
}
</style>