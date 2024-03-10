<template>
  <div>
    <ul class="nav">
      <nuxt-link to="/">首页</nuxt-link>
      <nuxt-link to="/join">加入我们</nuxt-link>
      <nuxt-link to="/">
        <img src="~/static/images/icon/nav-log.png" alt="nav-log" />
      </nuxt-link>
      <nuxt-link to="/cooperation">商务合作</nuxt-link>
      <nuxt-link to="/article">最新资讯</nuxt-link>
    </ul>
    <el-backtop :bottom="20" :right="20">
      <div
        style="
           {
            height: 100%;
            width: 100%;
            background-color: #f2f5f6;
            border-radius: 5px;
            box-shadow: 0 0 6px rgba(0, 0, 0, 0.12);
            text-align: center;
            line-height: 40px;
            color: #1989fa;
            z-index: 9999;
          }
        "
      >
        <i class="el-icon-top"></i>
      </div>
    </el-backtop>
  </div>
</template>

<script>
import { Backtop } from "element-ui";

export default {
  name: "HeaderComponent.vue",
};
</script>

<style>
body {
  margin: 0;
}

ul {
  padding-left: 0;
}

.nav {
  display: flex;
  justify-content: center;
  align-items: center;
}

/* 未访问的链接 */
a:link {
  padding: 0 15px;
  color: black;
  text-decoration: none;
}

/* 访问过的链接 */
a:visited {
  color: black;
}

/* 鼠标悬停时 */
a:hover {
  color: blue;
}

/* 鼠标点击时 */
a:active {
  color: blue;
}
</style>
