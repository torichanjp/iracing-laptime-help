<script setup lang="ts">
</script>

<template>
  <div class="content">
    <h2>リプレイ操作</h2>
    <div class="table-container">
      <p class="note">※キー操作は、本ツールが選択（本ツールをマウスでクリック）されている必要があるのでご注意ください。</p>
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
          <td class="desc">押す毎に、2, 4, 8, 16倍と早送り速度があがります</td>
        </tr>

        <tr>
          <td class="operation">スロー再生</td>
          <td class="key"><span>NumPad 8</span></td>
          <td class="desc">押す毎に、1/2, 1/4, 1/8, 1/16倍とスローになります。押す前の状態が巻き戻しの場合は巻き戻しスロー再生になります。</td>
        </tr>

        <tr>
          <td class="operation">ライブ（現在）に戻る</td>
          <td class="key"><span>NumPad .</span></td>
          <td class="desc">現時点の映像に戻ります。</td>
        </tr>
        </tbody>
      </table>
    </div>
  </div>
</template>

<style scoped lang="scss">
</style>
