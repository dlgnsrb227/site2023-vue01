<template>
  <HeaderCont attr="header__wrap bg-blue nanumneo" />
  <router-view />
  <FooterCont attr="footer__wrap section nanumneo" />
</template>

<script>
// @ is an alias to /src
import HeaderCont from "@/components/layout/HeaderCont.vue";
import FooterCont from "@/components/layout/FooterCont.vue";

export default {
  components: {
    HeaderCont,
    FooterCont,
  },
};
</script>

<style lang="scss">
@import "style.scss";
</style>
