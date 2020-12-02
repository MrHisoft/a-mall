<template>
  <div class="container">
    <!-- slt -->
    <div class="content">
      <TabsItem v-for="(item, index) of navs" :key="`nav${index}`">
        <img
          slot="nav-icon"
          :src="require(`assets/img/tabbar/${item.urlName}.svg`)"
          @click="tabsClick(index)"
          alt=""
          v-if="index !== currentIndex"
        />
        <img
          slot="nav-icon"
          :src="require(`assets/img/tabbar/${item.urlName}_active.svg`)"
          @click="tabsClick(index)"
          alt=""
          v-if="index === currentIndex"
        />
        <span slot="nav-name" :class="{ colors: currentIndex === index }">{{
          item.name
        }}</span>
      </TabsItem>
    </div>
  </div>
</template>

<script>
import TabsItem from "components/content/home/TabsItem";
export default {
  name: "navtabs",
  components: {
    TabsItem,
  },
  data() {
    return {
      currentIndex: 0,
      navs: [
        {
          urlName: "home",
          name: "首页",
        },
        {
          urlName: "category",
          name: "分类",
        },
        {
          urlName: "shopcart",
          name: "购物车",
        },
        {
          urlName: "profile",
          name: "我的",
        },
      ],
    };
  },
  computed: {},
  watch: {},
  methods: {
    tabsClick(index) {
      this.currentIndex = index;
    },
  },
};
</script>

<style lang="scss" scoped>
.container {
  display: flex;
  align-items: flex-end;
}
.content {
  width: 100%;
  display: flex;
  height: 49px;
  border-top: 1px solid #f5f5f5;
  justify-content: center;
  align-items: center;
  background-color: #f9f9f9;
  border: 1px solid red;
  // section {
  //   flex: 1;
  //   align-items: center;
  //   display: flex;
  //   flex-direction: column;
  //   justify-content: center;
  //   img {
  //     width: 24px;
  //     height: 24px;
  //     vertical-align: middle;
  //   }
  //   span {
  //     font-size: 14px;
  //   }
  // }
  .colors {
    color: rgb(255, 71, 109);
  }
}
</style>
