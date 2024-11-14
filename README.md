# Look at My Life

使い方
1. このリポジトリをクローンする
2. 現状の収支を```index.html```内の```initialData```に書き込む
``` javascript
if (!initialData) {
        // 初期データポイントの配列を作成
        //自分で使用する際はここを変更してください
        var initialDataPoints = [
            ['2023/10/1', 0], 
            ['2023/10/2', 0],
            ['2023/10/3', 0]
        ];
        var labels = [];
        var data = [];
        initialDataPoints.forEach(function(item) {
            labels.push(item[0]);
            data.push(item[1]);
        });
        initialData = {
            labels: labels,
            datasets: [{
                data: data,
                borderColor: '#94C3FF',
                backgroundColor: '#E5F9FF',
                fill: true,
                tension: 0.4
            }]
        };
        // 初期データをlocalStorageに保存
        saveChartDataToLocalStorage(initialDataPoints);
    }
```

3. 使う
4. jsonファイルで現状のデータを出力できます

## 注意
localStorageを使っています
キャッシュを削除するとデータが消える可能性があります
