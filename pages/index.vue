<template>
  <div>
    <HeaderComponent />
    <section class="top-introduction">
      <img width="100%" src="~/static/images/bg/index-top.png" alt="" />
      <div class="top-introduction-text">
        <p style="font-size: 40px">瑞可创新</p>
        <p style="font-size: 16px">
          成立于2017年，主要从事无人机等家庭生活娱乐消费电子产品的设计、研发与销售；拥有多项发明及实用新型专利和自主知识产权软件控制系统,
          是国家高新技术科技企业，省级专精特新企业。
        </p>
        <p style="font-size: 16px">
          在全球多个国家注册了Ruko品牌，深耕美国、欧洲市场已拥有数百万忠实用户,致力于成为全球国际知名消费电子品牌
        </p>
      </div>
    </section>
    <FooterComponent />
  </div>
</template>

<script>
import HeaderComponent from "~/components/HeaderComponent.vue";
import FooterComponent from "~/components/FooterComponent.vue";
import { Col, Row } from "element-ui";

export default {
  name: "IndexPage",
  components: {
    HeaderComponent,
    FooterComponent,
  },
};
</script>

<style scoped>
.top-introduction {
  position: relative;
  display: inline-block;
}
.top-introduction img {
  display: block;
  width: 100%;
}
.top-introduction-text {
  position: absolute;
  top: 50%;
  left: 6%;
  width: 30%;
  transform: translateY(-50%);
  color: #fff;
}
</style>
