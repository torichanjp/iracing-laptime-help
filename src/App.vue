<script setup lang="ts">
// This starter template is using Vue 3 <script setup> SFCs
// Check out https://vuejs.org/api/sfc-script-setup.html#script-setup
import Help from './components/Help.vue'
</script>

<template>
  <Help msg="iRacingラップテーブルツールヘルプ" />
</template>

<style lang="scss">
@import "./assets/scss/variables";

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: left;
  color: $main-color;
  margin-top: 60px;
}

a {
  color: $link-color;
}

div.content {
  width: $width;
  margin: 1em auto;
}

table {
  width: $width;
  margin: 1em auto;
  border-collapse: collapse;
}

th {
  background-color: $th-bk-color;
  color: $th-color;
  height: 2em;
}

td {
  background-color: $td-bk-color;
  height: 2em;
  padding: .5em;
  border: 1px solid gray;

  span {
    display: inline-block;
    border: 1px solid gray;
    padding: .5em;
    border-radius: 3px;
    background-color: #3C444C;
    color: white;
    font-weight: bold;
    min-width: 3em;
  }
  &.operation {
    width: 15em;
  }
  &.key {
    width: 8em;
    text-align: center;
  }
  &.desc {
    text-align: left;
    width: 20em;
  }
}

.note {
  color: red;
}

label {
  margin: 0 0.5em;
  font-weight: bold;
}

code {
  background-color: #eee;
  padding: 2px 4px;
  border-radius: 4px;
  color: #304455;
}

ul {
  text-align: left;
  list-style:none;
}

li{
  position: relative;
  padding-left: 10px;
}

li:before {
  content: "";
  position: absolute;
  top: .35em;
  left: 0;
  width: 0;
  height: 0;
  border-width: 5px;
  border-style: solid;
  border-color: transparent transparent transparent #8b6b4e;
}

.fade-enter-active, .fade-leave-active {
  transition: opacity .5s ease;
}

.fade-enter-from, .fade-leave-to {
  opacity: 0;
}
</style>
