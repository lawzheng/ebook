<template>
  <transition name="slide-up">
    <div class="menu-wrapper" :class="{'hide-box-shadow': settingVisible >= 0 || !menuVisible}"
         v-show="menuVisible">
      <div class="icon-wrapper" :class="{'selected': settingVisible === 3}">
        <span class="icon-menu" @click="showSetting(3)"></span>
      </div>
      <div class="icon-wrapper" :class="{'selected': settingVisible === 2}">
        <span class="icon-progress" @click="showSetting(2)"></span>
      </div>
      <div class="icon-wrapper" :class="{'selected': settingVisible === 1}">
        <span class="icon-bright" @click="showSetting(1)"></span>
      </div>
      <div class="icon-wrapper" :class="{'selected': settingVisible === 0}">
        <span class="icon-A" @click="showSetting(0)"></span>
      </div>
    </div>
  </transition>
</template>

<script>
  import { ebookMixin } from '../../utils/mixin'
  export default {
    name: 'EbookMenu',
    mixins: [ebookMixin],
    data () {
      return {
        settingVisible: -1
      }
    },
    methods: {
      showSetting (key) {
        console.log(key)
      }
    }
  }
</script>

<style lang="less" scoped>
  @import "../../assets/styles/global.less";

  .menu-wrapper {
    position: absolute;
    bottom: 0;
    left: 0;
    z-index: 200;
    display: flex;
    width: 100%;
    height: 48px;
    box-shadow: 0 -8px 8px rgba(0, 0, 0, .15);
    font-size: 22px;
    background-color: #fff;
    &.hide-box-shadow {
      box-shadow: none;
    }
    .icon-wrapper {
      flex: 1;
      .center;
      .icon-progress {
        font-size: 24px;
      }
      .icon-A {
        font-size: 20px;
      }
    }
  }
</style>
