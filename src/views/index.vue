<template>
  <div class="app-container home">
    <el-row :gutter="20">
      <el-col>
        <div class="data-tj-block" v-for="item in dataItems">
          <p style="margin-bottom: 10px">
            <span class="tj-label">{{ item.oneLabel }}</span>
            <span class="tj-data">{{ item.oneData }}</span>
          </p>
          <p>
            <span class="tj-label">{{ item.twoLabel }}</span>
            <span class="tj-data">{{ item.twoData }}</span>
          </p>
        </div>
      </el-col>
    </el-row>
    <el-row :gutter="20">
      <el-col :sm="24" :lg="12" style="padding-left: 20px">

      </el-col>

      <el-col :sm="24" :lg="12" style="padding-left: 50px">

      </el-col>
    </el-row>
    <el-divider/>
    <el-row :gutter="20">
      <el-col :xs="24" :sm="24" :md="12" :lg="8">
        <el-card class="update-log">
          <div slot="header" class="clearfix">
            <span>捐赠支持</span>
          </div>
          <div class="body">
            <img
              src="https://oscimg.oschina.net/oscnet/up-d6695f82666e5018f715c41cb7ee60d3b73.png"
              alt="donate"
              width="100%"
            />
            <span style="display: inline-block; height: 30px; line-height: 30px"
            >你可以请作者喝杯咖啡表示鼓励</span
            >
          </div>
        </el-card>
      </el-col>
    </el-row>
  </div>
</template>

<script>
export default {
  name: "index",
  data() {
    return {
      // 版本号
      version: "3.5.0",
      dataItems: {}
    };
  },
  created() {
    let that = this;
    that.dataItems = [
      {oneLabel: '库存总量：', oneData: '200', twoLabel: '库存成本：', twoData: '1000.00'},
      {oneLabel: '现金：', oneData: '200.00', twoLabel: '银行存款：', twoData: '1000.00'},
      {oneLabel: '客户欠款：', oneData: '200.00', twoLabel: '供应商欠款：', twoData: '1000.00'},
      {oneLabel: '销售收入：', oneData: '200.00', twoLabel: '商品毛利（本月）：', twoData: '200.00'},
      {oneLabel: '采购金额（本月）：', oneData: '200.00', twoLabel: '商品种类（本月）：', twoData: '200.00'}
    ]
  }
  ,
  methods: {
    goTarget(href) {
      window.open(href, "_blank");
    }
  }
}
</script>

<style scoped lang="scss">
.home {

  font-family: "open sans", "Helvetica Neue", Helvetica, Arial, sans-serif;
  font-size: 13px;
  color: #676a6c;
  overflow-x: hidden;

  .data-tj-block {
    border: 1px solid rgba(228, 228, 228, 1);
    float: left;
    margin-right: 30px;
    padding: 15px 10px;
    min-width: 250px;
    font-size: 16px;

    p {
      margin: 0px;
      padding: 0px;
    }

    p .tj-data {
      float: right;
      padding-right: 20px;
    }
  }

  .col-item {
    margin-bottom: 20px;
  }

  ul {
    padding: 0;
    margin: 0;
  }

  ul {
    list-style-type: none;
  }

  h4 {
    margin-top: 0px;
  }

  h2 {
    margin-top: 10px;
    font-size: 26px;
    font-weight: 100;
  }

  p {
    margin-top: 10px;
  }

  b {
    font-weight: 700;
  }
}

.update-log {
  ol {
    display: block;
    list-style-type: decimal;
    margin-block-start: 1em;
    margin-block-end: 1em;
    margin-inline-start: 0;
    margin-inline-end: 0;
    padding-inline-start: 40px;
  }
}
</style>

