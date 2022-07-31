<script setup lang="ts">
</script>

<template>
  <div class="content">
    <h2>画面</h2>
    <div class="table-container">
      <div class="para">
        <h3>メイン画面</h3>
        <img src="../assets/images/LapTable1.png" alt="Laptime table"/>
      </div>
      <!-- ヘッダStart -->
      <div class="para">
        <h3>ヘッダ</h3>
        <p class="image header"><img src="../assets/images/LapTable1.png" alt="Laptime table"/></p>
        <table>
          <thead>
            <tr>
              <td>項目</td>
              <td>説明</td>
            </tr>
          </thead>
          <tbody>
            <tr>
              <td>
                <p class="image help-icon"><img src="../assets/images/LapTable1.png" alt="Laptime table"/></p>
              </td>
              <td>
                本ヘルプをブラウザで表示します。
              </td>
            </tr>
            <tr>
              <td>
                <p>SubSessionId</p>
              </td>
              <td>
                <p>iRacingのサブセッションID。iRacing UIに表示される結果に一致します。</p>
                <p>FUELストラテジースプレッドシートと連携する場合にこのIDと、CarIdxが必要になります。</p>
              </td>
            </tr>
            <tr>
              <td>
                <p>気温</p>
              </td>
              <td>
                <p>レース中の（恐らくフィニッシュ/スタートライン付近の）気温です。単位摂氏（℃）</p>
              </td>
            </tr>
            <tr>
              <td>
                <p>路温</p>
              </td>
              <td>
                <p>セッション中の（恐らくフィニッシュ/スタートライン付近の）路面温度です。単位摂氏（℃）</p>
              </td>
            </tr>
            <tr>
              <td>
                <p>SoF</p>
              </td>
              <td>
                <p>そのセッションのSoFです。マルチクラスの場合はマルチクラス毎に表示されます</p>
                <p>チーム戦の場合は、車に乗り込んだドライバーが対照になりますので、時間経過につれて変化することになります。</p>
                <p>SDK Gamingは、現在乗り込んでいるドライバーのみが対照になりますので本数値とは異なります。</p>
                <p>他のツールの仕様は把握していません。</p>
                <p>ツール終了時に本数値は自動保存されるので、次回ツール起動時も正しい値になります。</p>
              </td>
            </tr>
          </tbody>
        </table>
      </div>
      <!-- ヘッダEnd -->

      <!-- ラップテーブルStart -->
      <div class="para">
        <h3>ラップテーブル</h3>
        <p class="image lap-table"><img src="../assets/images/LapTable1.png" alt="Laptime table"/></p>
        <table class="lap-table">
          <thead>
          <tr>
            <td>項目</td>
            <td>表示例</td>
            <td>説明</td>
          </tr>
          </thead>
          <tbody>
            <tr>
              <td>
                <p>Pos</p>
              </td>
              <td rowspan="2">
                <p class="image pos" style="text-align: center;"><img src="../assets/images/LapTable1.png" alt="Laptime table"/></p>
              </td>
              <td>
                <p>現在のクラス順位です。数秒おきに更新されます。</p>
              </td>
            </tr>
            <tr>
              <td>
                <p>All</p>
              </td>
              <td>
                <p>現在のセッション全体の順位です。すなわち、別クラスを含めた総合順位です。</p>
                <p>数秒おきに更新されます。</p>
              </td>
            </tr>
            <tr>
              <td>
                <p>Car#</p>
              </td>
              <td rowspan="2">
                <p class="image number"><img src="../assets/images/LapTable1.png" alt="Laptime table"/></p>
              </td>
              <td>
                <p>車番（カーナンバー）です。</p>
              </td>
            </tr>
            <tr>
              <td>
                <p>CarIdx</p>
              </td>
              <td>
                <p>iRatingが高い順に1から割り当てられます。iRacing内で暗黙に利用されているIDです。</p>
                <p>他のツールで対象のドライバー（またはチーム）のラップ情報のみ取得したい場合などに利用します。</p>
              </td>
            </tr>
            <tr>
              <td>
                <p>Team</p>
              </td>
              <td rowspan="2">
                <p class="image name"><img src="../assets/images/LapTable1.png" alt="Laptime table"/></p>
              </td>
              <td>
                <p>チーム戦の場合はチーム名、個人戦の場合は個人名が表示されます。</p>
              </td>
            </tr>
            <tr>
              <td>
                <p>Driver</p>
              </td>
              <td>
                <p>個人名が表示されます。個人戦の場合は表示されません（ツールバージョンによる）</p>
              </td>
            </tr>
            <tr>
              <td>
                <p>LastPit</p>
              </td>
              <td rowspan="2">
                <p class="image pit"><img src="../assets/images/LapTable1.png" alt="Laptime table"/></p>
              </td>
              <td>
                <p>最後にピットに入った周です。</p>
              </td>
            </tr>
            <tr>
              <td>
                <p>PitStops</p>
              </td>
              <td>
                <p>ピットに入った回数です。例では5周目（の終わり）にピットに入ったことを示しています。</p>
                <p>ただし、ツールを再起動した場合は、クラウドのデータから回数を計算するため、アップロードされているクラウドのデータに依存します。</p>
              </td>
            </tr>
            <tr>
              <td>
                LapComp
              </td>
              <td>
                <p class="image lap-comp"><img src="../assets/images/LapTable1.png" alt="Laptime table"/></p>
              </td>
              <td>
                <p>周回数です。</p>
                <p>例えば、スタート後、１周してフィニッシュラインを超えた時点で１となります。</p>
                <p>反映まで多少のタイムラグがあります（数秒）</p>
                <p>下のバーは、現周回の走っている位置を示します。この場合は、6周走り、7周目の半分を超えた辺りを走行していることを示しています。</p>
              </td>
            </tr>
            <tr>
              <td>
                <p>ΔSec</p>
              </td>
              <td rowspan="2">
                <p class="image delta"><img src="../assets/images/LapTable1.png" alt="Laptime table"/></p>
              </td>
              <td>
                <p>自車（スペクテーターの場合は選択しているドライバー（チーム））との差を「分：秒」で表示します。</p>
                <p>この差は、自車の直近のラップタイムをベースに計算されるため、ラップタイムがない場合は「00:00」と表示されます。</p>
              </td>
            </tr>
            <tr>
              <td>
                <p>ΔLap</p>
              </td>
              <td>
                <p>自車（スペクテーターの場合は選択しているドライバー（チーム））との差を周で表示します。</p>
                <p>例えば、自車と半周差がある場合は「0.5」、１周差がある場合は「1.0」と表示されます。</p>
                <p>自車より遅い（後ろにいる）場合は、マイナス表示となります。</p>
              </td>
            </tr>
            <tr>
              <td>
                <p>LapTime</p>
              </td>
              <td rowspan="2">
                <p class="image lap-time"><img src="../assets/images/LapTable1.png" alt="Laptime table"/></p>
              </td>
              <td>
                <p>ラップタイムを直近40周分表示します。</p>
                <p>左が最新になります。</p>
                <p>下の段は、自車とのタイム差です。緑は相手の方が遅い、赤は相手の方が速いことを示しています。</p>
                <p>例は、赤表示なので、相手の車が1.481秒速いことを示しています。</p>
              </td>
            </tr>
            <tr>
              <td>
                <p>LapTime差</p>
              </td>
              <td>
                <p>ラップタイムを直近40周分表示します。</p>
                <p>左が最新になります。</p>
                <p>下の段は、自車とのタイム差です。緑は相手の方が遅い、赤は相手の方が速いことを示しています。</p>
                <p>例は、赤表示なので、相手の車が1.481秒速いことを示しています。</p>
              </td>
            </tr>
          </tbody>
        </table>

        <h4>その他</h4>
        <table class="lap-table">
          <thead>
          <tr>
            <td>項目</td>
            <td>説明</td>
          </tr>
          </thead>
          <tbody>
          <tr>
            <td>
              <p>黄色の文字</p>
            </td>
            <td>
              <p>自車を表します。スペクテーターの場合は、選択した車（カメラに映っている車）になります。</p>
            </td>
          </tr>
          <tr>
            <td>
              <p>青色の文字</p>
            </td>
            <td>
              <p>カメラに映っている車を表します。カメラの切り替えは、ラップ表の切り替えたい車の行をクリックします。</p>
            </td>
          </tr>
          <tr>
            <td>
              <p>ソート</p>
            </td>
            <td>
              <p>Pos、CarIdx、Teamヘッダをクリックすると、昇順、降順でソートします。</p>
              <p>CarIdxは、iRatingの順番に並べたい場合に便利です。</p>
            </td>
          </tr>
          <tr>
            <td>
              <p>ラップタイムを刻んだドライバー確認</p>
            </td>
            <td>
              <p>各ラップにマウスオーバーすると、ドライバー名、iRatingを表示します。</p>
              <p>チーム戦の時に利用します。</p>
              <p>ピットでドライバーチェンジしているか、前と現在のドライバーの実力比較など。</p>
            </td>
          </tr>
          </tbody>
        </table>

      </div>
      <!-- ラップテーブルEnd -->

      <!-- フッタStart -->
      <div class="para">
        <h3>フッタ</h3>
        <p class="image footer"><img src="../assets/images/LapTable1.png" alt="Laptime table"/></p>
        <table class="lap-table">
          <thead>
          <tr>
            <td>項目</td>
            <td>説明</td>
          </tr>
          </thead>
          <tbody>
            <tr>
              <td>
                <p>自分のラップだけ送信する</p>
              </td>
              <td>
                <p>チームインで共有したり、別ツールで利用したりするために、ラップ情報を都度クラウドにアップロードしています。</p>
                <p>FUEL情報は運転しているドライバーからのみ取得できるため、運転中はこのツールを起動していなければなりません。</p>
                <p>通信環境が良くない場合は、有効にする（ボタンが青色の状態）ことで自車情報のみアップロードします。</p>
                <p>ただし、有効にした状態で他のメンバーがラップツールを起動していないと他車の情報がクラウドにアップロードされず、あとになって他のメンバーがラップツールを起動しても他車の情報が見れないことになるので、基本無効にしておいてください。</p>
              </td>
            </tr>
          </tbody>
        </table>
      </div>
      <!-- フッタEnd -->
    </div>
  </div>
</template>

<style scoped lang="scss">
p.image {
  position: relative;
  overflow: hidden;
  img {
    position: relative;
  }
}

p.header {
  height: 30px;
  img {
    top: -30px;
  }
}

p.lap-table {
  height: 460px;
  img {
    top: -55px;
  }
}

p.footer {
  height: 30px;
  img {
    top: -596px;
  }
}

p.help-icon {
  height: 30px;
  width: 25px;
  img {
    top: -30px;
    left: -3px;
  }
}

p.pos {
  height: 70px;
  width: 60px;
  img {
    top: -182px;
    left: 0;
    transform-origin: top left 0;
    transform: scale(2.0, 2.0);
  }
}

p.number {
  height: 70px;
  width: 60px;
  img {
    top: -182px;
    left: -76px;
    transform-origin: top left 0;
    transform: scale(2.0, 2.0);
  }
}

p.name {
  height: 58px;
  width: 60px;
  img {
    top: -238px;
    left: -112px;
    transform-origin: top left 0;
    transform: scale(1.5, 1.5);
  }
}

p.pit {
  height: 70px;
  width: 60px;
  img {
    top: -950px;
    left: -454px;
    transform-origin: top left 0;
    transform: scale(2.0, 2.0);
  }
}

p.lap-comp {
  height: 54px;
  width: 70px;
  img {
    top: -188px;
    left: -400px;
    transform-origin: top left 0;
    transform: scale(1.5, 1.5);
  }
}

p.delta {
  height: 54px;
  width: 70px;
  img {
    top: -188px;
    left: -468px;
    transform-origin: top left 0;
    transform: scale(1.5, 1.5);
  }
}

p.lap-time {
  height: 54px;
  width: 88px;
  img {
    top: -188px;
    left: -540px;
    transform-origin: top left 0;
    transform: scale(1.5, 1.5);
  }
}

table.lap-table {
  td > p {
    margin-top: 0;
    margin-bottom: 0;
  }
}
</style>
