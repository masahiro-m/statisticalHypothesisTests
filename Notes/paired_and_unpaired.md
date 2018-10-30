# 対応関係について
- 検定対象となる標本データが2群間でペア(他群の場合はグループ)になっているか否かで、検定統計量の算出方法が若干異なる
- 対応あり(関連のある)データはbefore, afterというように**経時変化**を捉えたデータ
- 対応なし(独立した)データは**属性による変化**(性別、場所など)を横断面的に捉えたデータ
- 基本的に"対応あり"の方は個体間のズレが出にくいため、検定しやすくなる
  - 例) 対応あり分散分析(ANOVA)では標本間変動を分離することが可能(詳しくは[こちら](https://github.com/Wotipati/statisticalHypothesisTests/blob/master/Notes/What_is_ANOVA%3F.md#%E5%AF%BE%E5%BF%9C%E3%81%82%E3%82%8A%E4%B8%80%E5%85%83%E9%85%8D%E7%BD%AE%E5%88%86%E6%95%A3%E5%88%86%E6%9E%90))
- "対応なし"の方は一度に多くのデータが集められる
- そもそも標本をペアにして確保する（対応ありデータを集める）ことが不可能な場合もある
  - 例1) 農村と都市部の所得の差
  - 例2) 異なる二つの土壌の生育差

例) あるダイエット法の効果を検証する際
- 異なる人同士を比較する方法は**対応なし**
- 同じ人を追跡調査し、比較する方法は**対応あり**