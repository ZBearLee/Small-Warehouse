<template>
  <div class="hello">
    <ul class="components-list">
      <li v-for="(item,index) in componentLists" :key="index">
        <router-link :to="item.url" class="add_bottom">
          <span class="txt">{{item.text}}</span>
        </router-link>
      </li>
    </ul>
  </div>
</template>

<script>

export default {
  name: "HelloWorld",
  data() {
    return {
      isActive: true,
      componentLists: [{ text: "动画组件", url: "/animation" }]
    };
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>
ul,
li {
  list-style: none;
}
a {
  text-decoration: none;
}
.components-list {
  display: flex;
}
</style>
