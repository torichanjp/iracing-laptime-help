<script setup lang="ts">
</script>

<template>
  <div class="content">
    <h2>カメラ操作</h2>
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
          <td class="desc">iRacingのカメラをTV1 Mixedに切り替えます。ただし対応していないサーキットはフロント視点になります。</td>
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
  </div>
</template>
