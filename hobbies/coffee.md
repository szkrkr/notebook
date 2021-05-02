# COFFEE



### 豆

<div id="coffee_taste_chart" ></div>

||Name|産地|焙煎所|所感|
|--|--|--|--|--|--|
|1|[インドネシアスマトラ マンデリン Taboo［SG］](https://www.awashima.shop/?pid=150758821)|インドネシア|淡島コーヒー|苦味はあるけど、舌には残らない。深入りにしても美味しいかも|


<script type="text/javascript">
  google.charts.load('current', {'packages':['corechart']});
  google.charts.setOnLoadCallback(drawSeriesChart);
  function drawSeriesChart() {
    var data = google.visualization.arrayToDataTable([
      ['ID', 'Sweetness/Bitter', 'Acidity/Body', 'Type', 'like'],
      ['インドネシアスマトラ マンデリン Taboo［SG］',    80, 80, 'Black', 1],
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
          fontSize: 5,
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
          fontSize: 11
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

### 淹れ方

#### ギア

|TYPE|名前|会社|小売価格|所感|
|--|--|--|--|--|
|グラインダー|[コーヒーミル・コラム](https://www.hario.com/seihin/productdetail.php?product=CM-502C)|HARIO|¥3,850|お洒落|
|ポット|[細口ポット0.7ℓ](https://www.kalita.co.jp/products/stainless/1964)|Kalita|¥6,050|結構太く感じるがこれで良いのか？|
|ドリッパー|[V60透過ドリッパ-01クリア](https://www.hario.com/seihin/productdetail.php?product=VD-01T-15CP)|HARIO|¥715|一穴|
|ドリッパー|[ガラスドリッパー155](https://www.kalita.co.jp/products/waveseries/2023)|Kalita|¥2,310|ウェーブシリーズ|
|スケール|[V60ドリップスケール](https://www.hario.com/seihin/productdetail.php?product=VSTN-2000B)|HARIO|¥6,600||
|フレンチプレス|[KENYA](https://www.bodum.com/jp/ja/10685-01j-kenya)|bodum|¥4,050||

#### RECORDS

||コーヒー豆量|湯量|湯温|蒸らし時間|ドリップ時間|所感|
|--|--|--|--|--|--|
|2021-05-02|23.0g|?(失敗)|83°|0:30|2:30|湯量が多く、薄くなってしまったかも。コーヒーサーバーが必要。|
