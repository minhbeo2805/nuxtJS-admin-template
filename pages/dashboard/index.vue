<template>
  <el-row>
    <div class="side-bar-container">
      <side-bar/>
    </div>
    <div class="main-container">
      <div class="breadcrumb-container">
        <breadcrumb/>
      </div>
      <div class="dashboard-container">
        <div class="dashboard-text">name: minh</div>
      </div>
    </div>
  </el-row>
</template>

<script>
import SideBar from "@/components/SideBar/SideBar";
import Breadcrumb from "@/components/Breadcrumb/Breadcrumb";
export default {
  components: {
    SideBar,
    Breadcrumb
  }
};
</script>

<style lang="scss" scoped>
.dashboard {
  &-container {
    margin: 30px;
  }
  &-text {
    font-size: 30px;
    line-height: 46px;
  }
}

.side-bar-container {
  transition: width 0.28s;
  width: 210px !important;
  background-color: #2d3a4b;
  height: 100%;
  position: fixed;
  font-size: 0px;
  top: 0;
  bottom: 0;
  left: 0;
  overflow: hidden;
}

.main-container {
  min-height: 100%;
  -webkit-transition: margin-left 0.28s;
  transition: margin-left 0.28s;
  margin-left: 210px;
  position: relative;
  background-color: #ffffff;
}

.dashboard-container {
  min-height: calc(100vh - 50px);
  width: 100%;
  position: relative;
  overflow: hidden;
}
</style>


