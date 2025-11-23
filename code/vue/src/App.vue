<template>
  <div id="app">
    <el-container>
      <el-header style="background-color: cornflowerblue">
        <img src="@/assets/logo.png" alt="" style="width: 40px;position: relative;top: 12px; margin-right: 5px" >
        <span style="font-size: 18px; color: white">hana</span>

      </el-header>

      <el-container>
        <el-aside style="background-color: #545c64;min-height: 100vh;width: 250px;overflow: hidden;">
          <el-menu :default-active="$route.path" router background-color="#545c64" text-color="#fff" active-text-color="#ffd04b">
            <el-menu-item index="/">
              <template slot="title">
                <i class="el-icon-location"></i><span>ホーム</span>
              </template>
            </el-menu-item>
            <el-submenu index="2">
              <template slot="title">
                <i class="el-icon-location"></i><span>ユーザー管理</span>
              </template>
              <el-menu-item-group>
                <el-menu-item index="/about">管理者情報</el-menu-item>
                <el-menu-item index="2-2">ユーザー情報</el-menu-item>
              </el-menu-item-group>
            </el-submenu>
            <el-submenu index="3">
              <template slot="title">
                <i class="el-icon-location"></i><span>情報管理</span>
              </template>
              <el-menu-item-group>
                <el-menu-item index="3-1">お知らせ一覧</el-menu-item>
              </el-menu-item-group>
            </el-submenu>
          </el-menu>
        </el-aside>
        <el-main><router-view/></el-main>
      </el-container>
    </el-container>

  </div>
</template>

<style>
</style>
<script lang="ts">
</script>