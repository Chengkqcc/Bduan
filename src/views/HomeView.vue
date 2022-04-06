<template>
  <div class="home">
    <el-container>
      <el-header class="header">
        <div class="top_left">
          <el-radio-group v-model="isCollapse">
            <el-button
              icon="el-icon-s-fold"
              @click="fn1"
              class="btn"
            ></el-button>
          </el-radio-group>
          <p class="title">后台管理系统</p>
        </div>
        <div class="top_right">
          <el-tooltip class="item" content="全屏" placement="top-start">
            <el-button icon="el-icon-rank"></el-button>
          </el-tooltip>
          <el-tooltip
            class="item"
            content="有2条未读信息"
            placement="top-start"
          >
            <el-button icon="el-icon-bell"></el-button>
          </el-tooltip>
          <div class="userImg">
            <img
              src="https://lin-xin.gitee.io/example/work/static/img/img.146655c9.jpg"
              alt=""
            />
          </div>
          <el-dropdown>
            <p>admin</p>
            <el-dropdown-menu slot="dropdown">
              <el-dropdown-item>项目仓库</el-dropdown-item>
              <el-dropdown-item>退出登录</el-dropdown-item>
            </el-dropdown-menu>
          </el-dropdown>
        </div>
      </el-header>
      <el-container>
        <div class="el-aside">
          <el-menu 
            default-active="1-4-1"
            class="el-menu-vertical-demo"
            @open="handleOpen"
            @close="handleClose"
            :collapse="isCollapse"
          >
            <el-menu-item index="1">
              <i class="el-icon-menu"></i>
              <span slot="title">系统首页</span>
            </el-menu-item>
            <el-menu-item index="2">
              <i class="el-icon-document"></i>
              <span slot="title">基础表格</span>
            </el-menu-item>
            <el-menu-item index="3">
              <i class="el-icon-setting"></i>
              <span slot="title">tab选项卡</span>
            </el-menu-item>
            <el-submenu index="4">
              <template slot="title">
                <i class="el-icon-location"></i>
                <span>表单相关</span>
              </template>
              <el-menu-item index="4-1">基本表单</el-menu-item>
              <el-submenu index="4-2">
                <template slot="title">三级菜单</template>
                <el-menu-item index="4-2-1">富文本编辑器</el-menu-item>
                <el-menu-item index="4-2-2">markdown编辑器</el-menu-item>
              </el-submenu>
              <el-menu-item index="4-3">文件上传</el-menu-item>
            </el-submenu>
            <el-menu-item index="5">
              <i class="el-icon-setting"></i>
              <span slot="title">自定义图标</span>
            </el-menu-item>
            <el-menu-item index="6">
              <i class="el-icon-document"></i>
              <span slot="title">schart图表</span>
            </el-menu-item>
            <el-submenu index="7">
              <template slot="title">
                <i class="el-icon-location"></i>
                <span>拖拽组件</span>
              </template>
              <el-menu-item index="4-1">拖拽列表</el-menu-item>
              <el-menu-item index="4-1">拖拽弹框</el-menu-item>
            </el-submenu>
            <el-menu-item index="8">
              <i class="el-icon-document"></i>
              <span slot="title">国际化功能</span>
            </el-menu-item>
            <el-submenu index="9">
              <template slot="title">
                <i class="el-icon-location"></i>
                <span>错误处理</span>
              </template>
              <el-menu-item index="4-1">权限测试</el-menu-item>
              <el-menu-item index="4-1">404页面</el-menu-item>
            </el-submenu>
            <el-menu-item index="10">
              <i class="el-icon-document"></i>
              <span slot="title">支持作者</span>
            </el-menu-item>
          </el-menu>
        </div>
        <el-main>Main</el-main>
      </el-container>
    </el-container>
  </div>
</template>

<script>
export default {
  name: "HomeView",
  components: {},
  data() {
    return {
      isCollapse: false,
    };
  },
  methods: {
    handleOpen(key, keyPath) {
      console.log(key, keyPath);
    },
    handleClose(key, keyPath) {
      console.log(key, keyPath);
    },
    fn1() {
      this.isCollapse = !this.isCollapse;
    },
  },
};
</script>
<style scoped>
*{
  color: #fff;
}
.el-menu{
  background: #324157;
}
.userImg img {
  width: 100%;
  height: 100%;
}
.userImg {
  width: 50px;
  height: 50px;
  border-radius: 50%;
  overflow: hidden;
  margin: 10px;
}
.top_right button {
  height: 50px;
  width: 50px;
  background: transparent;
  border: none;
}
.top_left button{
  height: 50px;
  width: 70px;
  background: transparent;
  border: none;
}
.top_left{
  display: flex;
  align-items: center;
}
.top_right {
  display: flex;
  align-items: center;
}
.header {
  display: flex;
  padding-left: 0;
  justify-content: space-between;
}
.el-submenu >>> .el-submenu__title {
  display: flex !important;
  align-items: center;
  color: #Fff;
  background: #324157;
}
.el-menu-item {
  text-align: left;
  min-width: 200px;
  color: #Fff;
  background: #324157;
}
.el-header {
  background-color: #b3c0d1;
  color: #fff;
  text-align: center;
  line-height: 60px;
  background: #242f42;
}
.el-main {
  background-color: #e9eef3;
  color: #fff;
  text-align: center;
}
.el-aside {
  background-color:#324157; 
  color: #fff;
  text-align: center;
  height: 100vh;
}
</style>
