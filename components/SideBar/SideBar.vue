<template>
    <el-col :span="3">
      <el-menu
        default-active="2"
        class="el-menu-vertical-demo"
        @open="handleOpen"
        @close="handleClose"
        background-color="#2d3a4b"
        text-color="#fff"
        active-text-color="#ffd04b"
      >
        <el-menu-item index="1">
          <template slot="title">
            <i class="el-icon-menu"></i>
            <span>Dashboard</span>
          </template>
        </el-menu-item>
        <el-submenu index="2">
          <template slot="title">
            <i class="el-icon-menu"></i>
            <span>Example</span>
          </template>
          <el-menu-item-group>
            <el-menu-item index="2-1">Table</el-menu-item>
            <el-menu-item index="2-2">Tree</el-menu-item>
          </el-menu-item-group>
        </el-submenu>
        <el-menu-item index="3">
          <i class="el-icon-document"></i>
          <span>Form</span>
        </el-menu-item>
        <el-submenu index="4">
          <template slot="title">
            <i class="el-icon-menu"></i>
            <span>Nested</span>
          </template>
          <el-menu-item-group>
            <el-menu-item index="4-1">
              <template slot="title">
                <i class="el-icon-menu"></i>
                <span>Menu1</span>
              </template>
            </el-menu-item>
            <el-submenu index="4-2">
              <template slot="title">
                <i class="el-icon-menu"></i>
                <span>Menu2</span>
              </template>
              <el-menu-item index="4-2-1">Menu2-1</el-menu-item>
              <el-menu-item index="4-2-2">Menu2-2</el-menu-item>
            </el-submenu>
            <el-menu-item index="4-3">
              <template slot="title">
                <i class="el-icon-menu"></i>
                <span>Menu3</span>
              </template>
            </el-menu-item>
            <el-menu-item index="4-2">Tree</el-menu-item>
          </el-menu-item-group>
        </el-submenu>
        <el-menu-item index="5">
          <i class="el-icon-setting"></i>
          <span>Navigator Four</span>
        </el-menu-item>
      </el-menu>
    </el-col>
</template>

<script>
export default {
  methods: {
    handleOpen(key, keyPath) {
      console.log(key, keyPath);
    },
    handleClose(key, keyPath) {
      console.log(key, keyPath);
    }
  }
};
</script>

