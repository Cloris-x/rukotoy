<template>
  <div>
    <HeaderComponent />
    <div>cooperation</div>
    <FooterComponent />
  </div>
</template>

<script>
import HeaderComponent from "/components/HeaderComponent.vue";
import FooterComponent from '~/components/FooterComponent.vue'

export default {
  name: "IndexPage",
  components: {
    HeaderComponent,
    FooterComponent
  },
};
</script>
