# COFFEE



### 豆

<div id="coffee_taste_chart" ></div>
<script type="text/javascript">
  google.charts.load('current', {'packages':['corechart']});
  google.charts.setOnLoadCallback(drawSeriesChart);
  function drawSeriesChart() {
    var data = google.visualization.arrayToDataTable([
      ['ID', 'Sweetness/Bitter', 'Acidity/Body', 'Type', 'like'],
      ['インドネシアスマトラ マンデリン Taboo［SG］', 80, 80, 'Black', 1],
      ['タンザニア　マンデリン フレンチロースト', 70, 80, 'Black', 1],
      ['エチオピア ナチュラル', 0, -80, 'Brown', 1]
    ]);

    var options = {
      title: 'Coffee Tastes',
      hAxis: {
        title: 'Acidity/Body',
        baseline: 0,
        baselineColor: '#000000',
        maxValue: 100,
        minValue: -100,
        textStyle: {
          fontSize: 3,
        }
      },
      vAxis: {
        title: 'Sweetness/Bitter',
        baseline: 0,
        maxValue: 100,
        minValue: -100,
      },
      bubble: {
        textStyle: {
          fontSize: 3
        }
      },
      height: 800,
      width: 800,
      legend: {
        position: 'none',
      },
      series: { 
        'Black': {
          color: 'black',
        }
      }
    };

    var chart = new google.visualization.BubbleChart(document.getElementById('coffee_taste_chart'));
    chart.draw(data, options);
  }
</script>

<iframe width="100%" height="800px" src="https://docs.google.com/spreadsheets/d/e/2PACX-1vR18QQQIA3VTQJu-M6h1281CkHYEU_GsR8nv4uxjUn5E4AI3ZP1YjOVkSR0swIGorUuc3QroEF1lo-S/pubhtml?gid=250228079&single=true"></iframe>

### 淹れ方

#### ギア

||名前|会社|小売価格|所感|
|--|--|--|--|--|
|グラインダー|[ポーレックス コーヒーミル2 ミニ](https://www.amazon.co.jp/%E3%83%9D%E3%83%BC%E3%83%AC%E3%83%83%E3%82%AF%E3%82%B9-Porlex-%E3%82%B3%E3%83%BC%E3%83%92%E3%83%BC%E3%83%9F%E3%83%AB%E3%83%BB%E2%85%A1%E3%83%9F%E3%83%8B-%E3%82%B3%E3%83%BC%E3%83%92%E3%83%BC%E3%83%9F%E3%83%AB2-%E3%83%9F%E3%83%8B/dp/B082L26FLX/ref=asc_df_B082L26FLX/?tag=jpgo-22&linkCode=df0&hvadid=342371031535&hvpos=&hvnetw=g&hvrand=12126799065747940805&hvpone=&hvptwo=&hvqmt=&hvdev=c&hvdvcmdl=&hvlocint=&hvlocphy=1009307&hvtargid=pla-853428177076&psc=1&tag=&ref=&adgrpid=72532999647&hvpone=&hvptwo=&hvadid=342371031535&hvpos=&hvnetw=g&hvrand=12126799065747940805&hvqmt=&hvdev=c&hvdvcmdl=&hvlocint=&hvlocphy=1009307&hvtargid=pla-853428177076)|Porlex|¥6,910|粗さが均一、回してても変わりにくい。臼型。|
|ポット|[細口ポット1.2ℓ](https://www.kalita.co.jp/products/stainless/1964)|Kalita|¥6,050|結構太く感じるがこれで良いのか？|
|ドリッパー|[V60透過ドリッパ-01クリア](https://www.hario.com/seihin/productdetail.php?product=VD-01T-15CP)|HARIO|¥715|一穴|
|ドリッパー|[ガラスドリッパー155](https://www.kalita.co.jp/products/waveseries/2023)|Kalita|¥2,310|ウェーブシリーズ|
|スケール|[V60ドリップスケール](https://www.hario.com/seihin/productdetail.php?product=VSTN-2000B)|HARIO|¥6,600||
|フレンチプレス|[KENYA](https://www.bodum.com/jp/ja/10685-01j-kenya)|bodum|¥4,050||

#### 欲しいギア
||名前|会社|小売価格|所感|
|--|--|--|--|--|
|ドリッパー|[ガラスドリッパー155](https://www.kalita.co.jp/products/waveseries/2023)|Kalita|¥2,310|ウェーブシリーズ|
|フレンチプレス|[KENYA](https://www.bodum.com/jp/ja/10685-01j-kenya)|bodum|¥4,050||

#### RECORDS

<iframe width="100%" height="800px" src="https://docs.google.com/spreadsheets/d/e/2PACX-1vR18QQQIA3VTQJu-M6h1281CkHYEU_GsR8nv4uxjUn5E4AI3ZP1YjOVkSR0swIGorUuc3QroEF1lo-S/pubhtml?gid=0&single=true"></iframe>