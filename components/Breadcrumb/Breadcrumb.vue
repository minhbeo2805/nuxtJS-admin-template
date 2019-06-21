<template>
  <div class="nav-bar">
    <el-col :span="10">
      <div class="breadcrumb-container">
        <el-breadcrumb separator="/">
          <el-breadcrumb-item v-for="(item) in levelList" :key="item.path">
            <span>{{ item.path }}</span>
          </el-breadcrumb-item>
        </el-breadcrumb>
      </div>
    </el-col>
  </div>
</template>
<script>
export default {
  watch: {
    $route() {
      console.log("watch");
      this.getBreadcrumb();
    }
  },
  created() {
    this.getBreadcrumb();
  },
  data() {
    return {
      levelList: null
    };
  },
  methods: {
    getBreadcrumb() {
      // only show routes with meta.title

      this.levelList = this.$route.matched;
      console.log(this.levelList);
    }
  }
};
</script>
<style lang="scss" scoped>
.nav-bar {
    position: fixed;
  height: 50px;
  overflow: hidden;
  position: relative;
  background: #fff;
  box-shadow: 0 1px 4px rgba(0, 21, 41, 0.08);

  .breadcrumb-container {
    float: left;
    .el-breadcrumb {
      display: inline-block;
      font-size: 14px;
      line-height: 50px;
      margin-left: 8px;
    }
  }
}
</style>

