<script setup lang="ts">
import { ref, computed, onMounted } from 'vue'

defineProps<{ msg: string }>()

const count = ref(0)
const doubleCount = computed(() => Math.pow(count.value, 2))

onMounted(() => {
  count.value = 10
})
</script>

<template>
  <h1>{{ msg }}</h1>

  <p class="note">※キー操作は、本ツールが選択（本ツールをマウスでクリック）されている必要があるのでご注意ください。</p>

  <h2>リプレイ操作</h2>
  <div class="table-container">
    <table>
      <thead>
      <tr>
        <th class="operation">動作</th>
        <th>キー</th>
        <th>説明</th>
      </tr>
      </thead>

      <tbody>

      <tr>
        <td class="operation">再生再開／一時停止</td>
        <td class="key"><span>NumPad 5</span></td>
        <td class="desc"></td>
      </tr>

      <tr>
        <td class="operation">巻き戻し</td>
        <td class="key"><span>NumPad 4</span></td>
        <td class="desc">押す毎に、2, 4, 8, 16倍と巻き戻し速度があがります</td>
      </tr>

      <tr>
        <td class="operation">早送り</td>
        <td class="key"><span>NumPad 6</span></td>
        <td class="desc">押す毎に、2, 4, 8, 16倍と巻き戻し速度があがります</td>
      </tr>

      <tr>
        <td class="operation">スロー再生</td>
        <td class="key"><span>NumPad 8</span></td>
        <td class="desc">押す毎に、1/2, 1/4, 1/8, 1/16倍とスローになります。押す前の状態が巻き戻しの場合は巻き戻しスロー再生になります。</td>
      </tr>
      </tbody>
    </table>
  </div>

  <h2>カメラ操作</h2>
  <div class="table-container">
    <table>
      <thead>
      <tr>
        <th class="operation">動作</th>
        <th>キー</th>
        <th>説明</th>
      </tr>
      </thead>

      <tbody>
      <tr>
        <td class="operation">カメラを自車に戻す</td>
        <td class="key"><span>NumPad 0</span></td>
        <td class="desc">他のチーム・ドライバーを表示中にこのキーを押すと、自チームの表示に切り替えます</td>
      </tr>

      <tr>
        <td class="operation">コックピット視点切り替え</td>
        <td class="key"><span>F1</span></td>
        <td class="desc">iRacingのカメラをCockpitに切り替えます</td>
      </tr>

      <tr>
        <td class="operation">遠い後ろ視点切り替え</td>
        <td class="key"><span>F2</span></td>
        <td class="desc">iRacingのカメラをFar chaseに切り替えます</td>
      </tr>

      <tr>
        <td class="operation">TV1視点切り替え</td>
        <td class="key"><span>F3</span></td>
        <td class="desc">iRacingのカメラをTV1に切り替えます</td>
      </tr>

      <tr>
        <td class="operation">TV Mixed視点切り替え</td>
        <td class="key"><span>F4</span></td>
        <td class="desc">iRacingのカメラをTV1 Mixedに切り替えます</td>
      </tr>

      <tr>
        <td class="operation">上から視点切り替え</td>
        <td class="key"><span>F5</span></td>
        <td class="desc">iRacingのカメラをBlimpに切り替えます</td>
      </tr>

      <tr>
        <td class="operation">遠い上から視点切り替え</td>
        <td class="key"><span>F6</span></td>
        <td class="desc">iRacingのカメラをChopperに切り替えます</td>
      </tr>

      <tr>
        <td class="operation">右リヤタイヤ視点切り替え</td>
        <td class="key"><span>F7</span></td>
        <td class="desc">iRacingのカメラをRR Suspに切り替えます</td>
      </tr>

      <tr>
        <td class="operation">右フロントタイヤ視点切り替え</td>
        <td class="key"><span>F8</span></td>
        <td class="desc">iRacingのカメラをRF Suspに切り替えます</td>
      </tr>

      <tr>
        <td class="operation">左リヤタイヤ視点切り替え</td>
        <td class="key"><span>F9</span></td>
        <td class="desc">iRacingのカメラをLR Suspに切り替えます</td>
      </tr>

      <tr>
        <td class="operation">左フロントタイヤ視点切り替え</td>
        <td class="key"><span>F10</span></td>
        <td class="desc">iRacingのカメラをLF Suspに切り替えます</td>
      </tr>

      <tr>
        <td class="operation">フロント視点切り替え</td>
        <td class="key"><span>F11</span></td>
        <td class="desc">iRacingのカメラをRear chaseに切り替えます</td>
      </tr>

      <tr>
        <td class="operation">後ろ視点切り替え</td>
        <td class="key"><span>F12</span></td>
        <td class="desc">iRacingのカメラをChaseに切り替えます</td>
      </tr>
      </tbody>
    </table>
  </div>
</template>

<style scoped lang="scss">
a {
  color: #42b983;
}

table {
  width: 800px;
  margin: 1em auto;
  border-collapse:  collapse;
}

th {
  background-color: #555;
  color: white;
  height: 2em;
}
td {
  background-color: white;
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
</style>
