<template>
  <div class="container">
    <NavTabs />
  </div>
</template>

<script>
import NavTabs from "components/content/home/NavTabs";
export default {
  name: "Home",
  components: {
    NavTabs,
  },
  data() {
    return {};
  },
  computed: {},
  watch: {},
  methods: {},
};
</script>

<style lang="scss" scoped>
.container{
   height: 100vh;
   // border: 1px solid rebeccapurple;
}
body{
   border: 1px solid rebeccapurple;
   background-color: royalblue;
}
</style>
