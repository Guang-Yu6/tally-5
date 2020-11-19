<template>

  <nav>
    <router-link to="/money" class="item" active-class="selected">
      <Icon name="money2"/>
      记账
    </router-link>

    <router-link to="labels" class="item" active-class="selected">
      <Icon name="label2"/>
      标签
    </router-link>

    <router-link to="statistics" class="item" active-class="selected">
      <Icon name="statistics2"/>
      统计
    </router-link>
  </nav>

</template>

<script lang="ts">

export default {
name: "Nav"
}
</script>

<style lang="scss" scoped>
  nav {
  display: flex;
    box-shadow: 0 0 3px rgba(0, 0, 0, 0.25);  // 阴影
    flex-direction: row;
    font-size: 12px;
    > .item{
      padding: 2px 0;
      width: 33.33333%;
      display: flex;
      justify-content: center;
      align-items: center;
      flex-direction: column;
      .icon {
        width: 32px;
        height: 32px;
      }
    }
    > .selected {
      color: red;
    }
  }

</style>