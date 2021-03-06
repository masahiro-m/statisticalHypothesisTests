# Levene's-test
ルビーン検定
- 等分散の検定
- 対立仮説は「少なくとも１つの水準の母集団分散が他の水準の母集団分散とは異なる」
- F検定よりも正規性の仮定が厳しくないため、統計ソフトで多く用いられる
- 多くのパラメトリック検定は等分散性を前提としているため、この検定を用いて事前に等分散かどうかを検定する
- **分散が異なる場合に有意差が確認される** ことに注意


### 使い方
##### データの準備
- `testData.csv`に比較したい標本を`,`で区切りながら貼り付ける  
- 群間で対応しているデータが同じ列に並ぶように貼る
- 各行の先頭に群の名前を書く
- 3群以上あっても検定可能

```
GroupA,2,4,3,1,2,3,3,2,3,1
GroupB,2,2,3,2,3,3,1,2,3,1
GroupC,2,1,1,1,2,3,2,2,2,3
```

##### 実行
- 有意水準0.05で実行
```
python levene\'s-test.py
```
- 有意水準を設定したい場合
```
python levene\'s-test.py --level 0.01
```

- 別にデータを用意している場合
```
python levene\'s-test.py --input "csvファイルへのパス"
```

##### 結果
p値(p-value)が出力される  
有意差が観測された場合は`*`がつく
```
python levene\'s-test.py

p-value = 0.884504110648
```
