統計冬課題レポート(2019-01-15)
============
---------
------------------------------------
# はじめに
<span>　</span>この文章は,「統計」の冬課題として作成されたものである.  

主に,   
- **生活の実際における統計の利用**

- 以下の授業内で扱われた**統計に関する諸公式**  
  - 1 11/14 イントロダクション, データの整理  
  - 2 11/21 平均・メディアン・モード・分散・標準偏差  
  - 3 12/05 相関・回帰, 確率の考え方  
  - 4 12/12 正規分布, 二項分布  
  - 5 12/19 母集団と標本  
  - 6 12/26 平均の推定, t分布  

について記述する.  

<span>　</span>またこの文章は, **Markdown+MathJax** を用いて作成したものである.

------------------------------------
# 1) 統計の諸公式まとめ
##~第一回より~
### ①大きさ$N$のデータの階級幅の目安$n$
$$ n = 1 + \frac{log N}{log 2} (スタージェスの公式)\tag{1}$$  
$$ n = 1.7 ^3 \sqrt{N} (鈴木の公式)\tag{2} $$  
### ②範囲(レンジ)$R$
$$ R = Max - Min \tag{3}$$
$$(範囲R)=(最大値)-(最小値)$$
### ③($a_{i-1}<x_i\leqq a_i$の)階級幅
$$ h = a_{i+1}-a_i\tag{4}$$  
$$(階級幅h)=(一階級の範囲の下端a_{i+1})-(上端a_i)$$
### ④階級値
$$ x_i = \frac{a_i+a_{i+1}}{2}\tag{5}$$
$$(階級値x_i=階級の中央値)={(一階級の範囲の上端a_i)+(下端a_{i+1})}÷2$$
### ⑤累積度数
$$ F_j = \sum_{i=1}^{j}f_i\tag{6} $$
$$(累積度数F_j)=(前の階級までの度数(f_{1...j-1})の合計)+(求める階級の度数f_j)$$
### ⑥相対度数(=度数の総計$n$に対する一階級の度数$f_i$の比率)
$$ p_i \Bigl( = \frac{f_i}{n} \Bigr) = \frac{f_i}{\sum_{j=1}^{k}} \tag{7}$$
$$(相対度数p_i)=(一階級の度数f_i)÷(度数の総計n)$$
### ⑦累積相対度数  
$$P_j=\sum_{i=1}^{j}p_i\tag{8}$$  
$$(累積度数P_j)=(前の階級(j-1番目)までの相対度数の合計)+(求める階級の相対度数P_j)$$  

##~第二回より~
###