<template>
  <div>
    <a-layout id="components-layout-demo-side" style="min-height: 100vh;">
      <a-layout-sider :trigger="null" v-model="collapsed" collapsible>
        <div class="logo" />
        <SideMenu />
      </a-layout-sider>
      <a-layout>
        <a-layout-header style="background: #fff; padding: 0;">
          <Header />
        </a-layout-header>
        <a-layout-content style="margin: 0 16px;">
          <router-view></router-view>
        </a-layout-content>
        <a-layout-footer style="text-align: center;">
          <Footer />
        </a-layout-footer>
      </a-layout>
    </a-layout>
  </div>
</template>

<script>
import Header from "./Header";
import Footer from "./Footer";
import SideMenu from "./SideMenu";
export default {
  components: {
    Header,
    Footer,
    SideMenu,
  },
  data() {
    return {
      collapsed: false,
    };
  },
};
</script>
<style lang="less"></style>
