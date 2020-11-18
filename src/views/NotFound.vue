<template>
  <div>
    <div>404,当前页面不存在，请检查网址是否正确</div>
    <div>
      <router-link to="/">返回首页</router-link>
      <hr/>
      <a href="/">也是返回首页</a>
    </div>
  </div>
</template>

<script lang="ts">
export default {
name: "NotFound"
}
</script>

<style lang="scss" scoped>

</style>