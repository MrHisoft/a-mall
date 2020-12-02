<template>
  <section>
    <slot name="nav-icon"></slot>
    <slot name="nav-name"></slot>
  </section>
</template>

<script>
export default {
  // name: "",
  data() {
    return {};
  },
  computed: {},
  watch: {},
  methods: {},
};
</script>

<style lang="scss" scoped>
section {
  flex: 1;
  align-items: center;
  display: flex;
  flex-direction: column;
  justify-content: center;
  img {
    width: 24px;
    height: 24px;
    vertical-align: middle;
  }
  span {
    font-size: 14px;
  }
}
</style>
