<template>
  <div>
    <ul class="types">
      <li :class="type === '-' && 'selected'"
      @click="selectType('-')">支出</li>

      <li :class="type === '+' && 'selected'"
          @click="selectType('+')">收入</li>
    </ul>
  </div>
</template>

<script lang="ts">
  import  Vue from 'vue'
  import {Component} from 'vue-property-decorator';  // 装饰器

  @Component
  export default class Types extends Vue {
    type = '-' // - 表示支出， + 表示收入.

    //@Prop(Number) xxx: number | undefined;
    // Prop 告诉 Vue xxx 不是 data 是 Prop
    //装饰器 Number Vue xxx 运行时是个Number
    // xxx 属性名
    // number | undefined 告诉 TS xxx 的编译时类型

    selectType(type: string) {
      if (type !== '-' && type !== '+') {
        throw new Error('type is unknown');
      }
      this.type = type;
    }
  }

  // export default {  // JS写法
  //   name: "Types",
  //   props:['xxx'],
  //   data(){
  //     return {
  //       type:'-' // '-' 表示支出  ‘+’表示收入
  //     }
  //   },
  //   mounted() {
  //     console.log(this.xxx)
  //   },
  //   methods: {
  //     selectType(type) {
  //       if (type !== '-' && type !== '+') {
  //         throw new Error('type is unknown')
  //       }
  //       this.type = type
  //     }
  //   }
  // }
</script>

<style lang="scss" scoped>
.types {
  background: #c4c4c4;
  display: flex;
  text-align: center;
  font-size: 24px;
  > li {
    width: 50%;
    height: 64px;
    display: flex;
    justify-content: center;
    align-items: center;
    position: relative;
    &.selected::after {
      content: '';
      position: absolute;
      bottom: 0;
      left: 0;
      width: 100%;
      height: 4px;
      background: #333;
    }
  }
}
</style>