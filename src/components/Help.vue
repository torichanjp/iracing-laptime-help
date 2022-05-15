<script setup lang="ts">
import {ref} from 'vue'
import BasicHelp from "./BasicHelp.vue"
import CameraHelp from "./CameraHelp.vue"
import ReplayHelp from "./ReplayHelp.vue"
import WindowHelp from "./WindowHelp.vue"

defineProps<{ msg: string }>()

const selectedNav = ref(BasicHelp)
</script>

<template>
  <div class="content">
    <h1>{{ msg }}</h1>
  </div>

  <div class="nav">
    <div @click="selectedNav = BasicHelp">基本</div>
    <div @click="selectedNav = WindowHelp">画面</div>
    <div @click="selectedNav = ReplayHelp">リプレイ操作</div>
    <div @click="selectedNav = CameraHelp">カメラ操作</div>
  </div>

  <transition name="fade" mode="out-in">
    <component :is="selectedNav"/>
  </transition>
</template>

<style scoped lang="scss">
@import "../assets/scss/variables";

$nav-height: 3em;

.nav {
  margin: 1em auto;
  div {
    text-align: center;
    display: inline-block;
    border: 1px solid $main-color;
    border-radius: $border-radius;
    min-width: 24%;
    height: $nav-height;
    line-height: $nav-height;
    font-weight: bold;
    color: $main-color;
    background-color: lightgray;
    cursor: pointer;
    &:hover {
      background-color: $main-color;
      color: white;
    }
  }
  width: $width;
}
</style>
