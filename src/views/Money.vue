<template>
  <div class="nav-wrapper">
    <div class="content">
      钱主页.vue
    </div>
  <Nav/>
  </div>
</template>

<script lang="ts">
export default {
name: "Money",
}
</script>

<style lang="scss" scoped>
  .nav-wrapper{
    border: 5px solid green;
    display: flex;
    flex-direction: column;
    height: 100vh;
  }
  .content{
    border: 5px solid saddlebrown;
    overflow: auto;
    flex-grow: 1;  // 尽量把高度都给这个content
  }
</style>