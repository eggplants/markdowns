統計冬課題レポート(2019-01-15_16)
============
---

---
# はじめに
<span>　</span>この文章は, **「統計」** の冬課題である.  

<span>　</span>主に,   
- １)[**以下の授業内で扱われた統計に関する公式のまとめ**](#00)  
>  - [第1回 (11/14) イントロダクション, データの整理](#aa)  
>  - [第2回 (11/21) 平均・メディアン・モード・分散・標準偏差](#bb)  
>  - [第3回 (12/05) 相関・回帰, 確率の考え方](#cc)  
>  - [第4回 (12/12) 正規分布, 二項分布](#dd)  
>  - [第5回 (12/19) 母集団と標本](#ee)  
>  - [第6回 (12/26) 平均の推定, t分布](#ff)  


- 2B)[**生活の実際における統計の利用例**](#11)


について記述する.  

<span>　</span>またこの文章は,
**[Markdown](https://daringfireball.net/projects/markdown/)<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/4/48/Markdown-mark.svg/64px-Markdown-mark.svg.png" width="30">+[$MathJax$](https://www.mathjax.org/)<img src="https://upload.wikimedia.org/wikipedia/en/thumb/5/5f/MathJax.svg/220px-MathJax.svg.png" width="30">(数式部分)** を用いて作成した.

------------------------------------
<a name="00"></a>
# 1) 統計の公式まとめ
<a name="aa"></a>
##~第1回~
### ①大きさ$N$のデータの階級幅の目安$n$
$$ n = 1 + \frac{log N}{log 2} (スタージェスの公式)\tag{1}$$  
$$ n = 1.7 ^3 \sqrt{N} (鈴木の公式)\tag{2} $$  
### ②範囲(レンジ)$R$
$$ R = \max - \min \tag{3}$$
$$(範囲R)=(最大値)-(最小値)$$
### ③($a_{i-1}<x_i\leqq a_i$の)階級幅$h$
$$ h = a_{i+1}-a_i\tag{4}$$  
$$(階級幅h)=(一階級の範囲の下端a_{i+1})-(上端a_i)$$
### ④階級値$x_i$
$$ x_i = \frac{a_i+a_{i+1}}{2}\tag{5}$$
$$(階級値x_i=階級の中央値)={(一階級の範囲の上端a_i)+(下端a_{i+1})}÷2$$
### ⑤累積度数$F_j$
$$ F_j = \sum_{i=1}^{j}f_i\tag{6} $$
$$(累積度数F_j)=(前の階級までの度数(f_{1...j-1})の合計)+(求める階級の度数f_j)$$
### ⑥相対度数$p_i$
######(=度数の総計$n$に対する一階級の度数$f_i$の比率)
$$ p_i \Bigl( = \frac{f_i}{n} \Bigr) = \frac{f_i}{\sum_{j=1}^{k}} \tag{7}$$
$$\Big(相対度数(=度数の総計nに対する一階級の度数f_iの比率)p_i\Big)$$
$$\qquad\qquad\qquad\qquad\qquad\qquad\qquad=(一階級の度数f_i)÷(度数の総和n)$$
### ⑦累積相対度数$P_j$  
$$P_j=\sum_{i=1}^{j}p_i\tag{8}$$  
$$(累積相対度数P_j)\\=(前の階級(j-1番目)までの相対度数の合計)+(求める階級の相対度数P_j)$$  
<a name="bb"></a>
##~第2回~
###①平均 $\overline{x}$(データの大きさ$N$)
- データ($x_1,x_2,…,x_N)が与えられた時.
$$\overline{x'}\Biggl(=\frac{1}{N}(x_1+x_2+・・・+{x'}_N)\Biggr)=\frac{1}{N}\sum_{k=1}^N{x'}_k\tag{9}$$
$$(平均)=\frac{(各データ値x_iの総和)}{(データの大きさN)}$$
- 度数分布が与えられた時.
$$\overline{x}\Biggl(=\frac{1}{N}(x_1f_1+x_2f_2+・・・+x_nf_n)\Biggr)=\frac{1}{N}\sum_{k=1}^nx_kf_k\tag{10}$$
$$(平均)=\frac{(階級値x_iと度数f_iの積の総和)}{(データの大きさN)}$$
###②メディアン(中央値)$\tilde{x}$
- データ($x_1\leqq ・・・\leqq x_N$)が与えられた時.
$$\tilde{x}\Bigl(=Me(x)\Big)=\begin{cases}x_{k+1} & (N=2k+1:奇数)\\  \frac{(x_k+x_{k+1})}{2} & (N=2k:偶数)\end{cases} \tag{11}$$
$$(メディアン)=\begin{cases}\big\{(データの大きさNの半分)番目の値\big\} & (Nが奇数) \\
\big\{データの大きさNの半分)番目の値と次値の中間値)\big\} & \qquad\qquad\qquad(Nが偶数)\end{cases}$$
- 度数分布が与えられた時.($Nの偶奇に依らない.$)  
($累積度数:F_i, 度数:f_i, 階級:a_i,$ 大きさ$N$のデータをascending sortして $\frac{2}{N}$ 番目が属する階級:$f_{k-1}\sim f_k$)
$$\tilde{x}=a_{k-1}+\frac{a_k-a_{k-1}}{f_k}\bigg(\frac{N}{2}-F_{k-1}\bigg)\tag{12}$$
$$(推定のメディアン)=\\$$  
$$\qquad\qquad\qquad(階級の上端a_{k-1})+\frac{(階級幅)}{(メディアンの属する階級a_kの度数)}\qquad\quad\bigg\{\frac{N}{2}-(階級a_{k-1}までの累積度数)\bigg\}$$
###③分散 $\sigma^2$(標準偏差=$\sqrt{\sigma^2}$ )
$$\sigma^2(x)=\frac{1}{N}\sum_{k=1}^N(x_k-\tilde{x})^2=\frac{1}{N}\sum_{k=1}^N(x_k-\tilde{x})^2f_k=\overline{x^2}-(\overline{x})^2\tag{13}$$
$$(分散)=(偏差の平方の総和の平均)=\\(階級値の偏差の平方の総和)\times(階級の度数)=(平方の平均)-(平均の平方)$$
###④分散の基本性質
- $x$を$a$倍, ないし $b$足し合わせた時の値$y(=ax+b)$ について,
    - $$\overline{y}=a\overline{x}+b\tag{14}$$
    - $$\sigma^2(y)=a^2\sigma^2(x)\tag{15}$$
    - $$\sigma(y)=a\sigma(x)\tag{16}$$  
###⑤チェビシェフの定理
######(=ある程度の度数の全体に占める割合(データのばらつき)を把握する定理.)
$$P(|x-\overline{x}|<k\sigma)\geqq\bigg(1-\frac{1}{k^2}\bigg)\\\Leftrightarrow P(\overline{x}-k\sigma<x<\overline{x}+k\sigma)\geqq\bigg(1-\frac{1}{k^2}\bigg) (kは任意の実数)\tag{17}$$  
$$(\overline{x}-k\sigma<x<\overline{x}+k\sigmaを満たす範囲の度数の全体に占める割合P)\geqq\bigg(1-\frac{1}{k^2}\bigg)$$
###⑥変動係数$Cv(x)$
######(=異なる単位のデータ間関係を無名数で表す.)
$$Cv(x)=\sigma/\overline{x}\tag{18}$$  
$$(変動係数)=(標準偏差)/(平均)$$  
<a name="cc"></a>
##~第3回~
###①相関関係
 $(x_i-\overline{x})(y_i-\overline{y})が\begin{cases}正\Leftrightarrow正の相関がある.\\負\Leftrightarrow負の相関がある.\end{cases}\tag{19}$  
###②共分散$C(x,y)$
$$C(x,y)=\frac{1}{N}\sum_{k=1}^N(x_k-\overline{x})(y_k-\overline{y})=\overline{xy}-\overline{x}\overline{y}\tag{20}$$
$$\begin{eqnarray}(共分散)&=&(各二値の偏差の積(x_i-\overline{x})(y_i-\overline{y})の平均)\\&=&(xyの平均)-(x,yの平均の積)\end{eqnarray}$$
###③相関係数$r(x,y)$
######(=正負が相関に対応しており, $|r|\leqq1である.$)
$$\begin{eqnarray}r(x,y)\Bigg(=\frac{1}{N}\sum_{k=1}^N\frac{(x_k-\overline{x})}{\sigma(x)}\frac{(y_k-\overline{y})}{\sigma(y)}\Bigg)&=&\frac{C(x,y)}{\sigma(x)\sigma(y)}\\&=&\frac{\overline{xy}-\overline{x}\overline{y}}{\sqrt{\overline{x^2}-(\overline{x})^2}\sqrt{\overline{y^2}-(\overline{y})^2}}\tag{21}\end{eqnarray}$$
$$\begin{eqnarray}(相関係数)&=&\bigg(\frac{x,yの共分散}{x,yの標準偏差の積}\qquad\bigg)\\&=&\frac{(xyの平均)-(x,yの平均の積)}{\sqrt{(x^2の平均)-(xの平均)^2}\qquad\sqrt{(y^2の平均)-(yの平均)^2}} \end{eqnarray}$$
###④回帰直線
- $yのxへの回帰直線$
$$(y-\overline{y})=\frac{\sigma(y)r(s,y)}{\sigma(x)}(x-\overline{x})\tag{22}$$
- $xのyへの回帰直線$
$$(y-\overline{y})=\frac{\sigma(y)}{\sigma(x)r(s,y)}(x-\overline{x})\tag{23}$$
###⑤期待値 $\mu=E(X)$
- 離散型確率変数の場合　(ex.サイコロ)
$$\mu\Big(=E(a\leqq X\leqq b)\Big)=\sum_{k=a}^{b}x_kp_k\tag{24}$$
$$(期待値)=(確率変数X\times確率P(X)の総和)$$
- 連続型確率変数の場合　(ex.体重, 身長)
$$\mu\Big(=E(X)\Big)=\int_{-\infty}^{\infty}xf(x)dx\tag{25}$$
$$(期待値)=(確率変数x\times確率密度関数f(x)の両端\mp\infty の広義積分)$$
###⑥確率変数$X$の分散$V(X)$, 標準偏差 $\sigma(X)$
$$V(X)\Bigg(=E \Big\{ (X-\mu)^2\Big\} \Bigg)=\sum_k(x_k-\mu)^2p_k\tag{26}$$
$$(分散V(X))=\big\{ (確率変数Xと期待値\muの差の平方)\times(確率P(X))の総和)\big\}$$
$$\sigma(X)=\sqrt{V(X)}\tag{27}$$
$$(標準偏差\sigma(X))=\sqrt{分散V(X)}$$  
$$(因みに, 期待値の分散V(E) は, \bigg\{X^2の期待値E(X^2)-\Big(Xの期待値E(X)\Big)^2\bigg\}で求められる. )$$
<a name="dd"></a>
##~第4回~
###①同時確率変数$g(X,Y)$ の期待値$E\big(g(X,Y)\big)$ と分散$V\big(g(X,Y)\big)$
$$E\Big(g(X,Y)\Big)=\sum_i\sum_jg(x_i,y_j)P(x_i,y_j)\tag{28}$$
$$(X,Yの同時確率変数の期待値)=\sum(x_iy_j)(x_i,y_jが同時に起こる確率P(x_i,y_j))$$
$$\begin{eqnarray}V\Big(g(X,Y)\Big)&=&E([g(X,Y)-E(g)]^2)\\&=&\sum_i\sum_j\Big[g\big(x_i,y_j\big)-E(g)\Big]^2P(X=x_i,Y=y_j)\end{eqnarray}\tag{29}$$
$$(分散)=\sum\Bigg<\bigg\{(x_iy_j)-\big( g(x,y)についての期待値\big)\bigg\}^2\\\qquad\qquad\qquad\qquad\qquad\qquad\qquad\qquad\times\big(x_i,y_jが同時に起こる確率P(x_i,y_j)\big)\Bigg>$$
###②同時確率分布の基本性質
- $X,Y$が独立である時,
  - $$E(aX+bY)=aE(X)+bE(Y)\tag{30}$$
  - $$E(XY)=E(X)E(Y)\tag{31}$$
  - $$V(aX+bY)=a^2V(X)+b^2V(Y)\tag{32}$$
###③二項分布$Bin(n,p)$ における確率$P(X)$
$$P\Big((0\leqq)X=k(\leqq n)\Big)= {}_nC_kp^k(1-p)^{n-k}\tag{33}$$
$$(確率変数X=kの起こる確率P)\\=(コンビネーションn,k)\times(Xの起こる確率p)^k\times(Xの余事象)^{n-k}$$
$$\Bigg(因みに, (コンビネーションn,r)(={}_nC_r)は, \frac{n!}{r!(n-r)!}である.\Bigg)$$
###④二項分布$Bin(n,p)$ における期待値$E(X)$ と分散$V(X)$
$$E(X)=np,\quad V(X)=npq\quad(qはpの余事象.)\tag{34, 35}$$
$$(期待値)=(試行回数)\times(Xの起こる確率)$$
$$(分散)=(試行回数)\times(Xの起こる確率とその余事象の積)$$
###⑤正規分布$N(\mu, \sigma^2)$
$$P(X=x)=N(\mu, \sigma)=\frac{1}{\sqrt{2\pi\sigma^2}}e^\frac{(x-\mu)^2}{2\sigma^2}\tag{36}$$
$$(正規分布に従う確率の分布)=(分布の中心が平均値, 幅が標準偏差である正規分布)$$
###⑥正規分布の性質
- 正規分布$N(\mu, \sigma^2)$ には以下の様な性質がある.
  - $$P(\mu- \sigma\leqq X\leqq\mu+ \sigma)\approx 68.3\%\tag{37}$$
  - $$P(\mu-2\sigma\leqq X\leqq\mu+2\sigma)\approx 95.4\%\tag{38}$$
  - $$P(\mu-3\sigma\leqq X\leqq\mu+3\sigma)\approx 99.7\%\tag{39}$$
###⑦正規分布に従う確率分布$N(\mu, \sigma)$ の値$X\to Z$ 変換
$$\bigg(Z=\frac{X-\mu}{\sigma}\bigg)は, 正規分布N(0,1)に従う.\quad\tag{40}$$
$$X:N(\mu, \sigma^2)に従う.\to Z:N(0,1)に従う.$$
###⑧ラプラスの定理
######(=nの十分大きい二項分布$Bin(n,p)$ の正規分布へ近似化する.)
$$Z=\frac{(x-\mu)}{\sigma}=\frac{X-E(X)}{\sqrt{V(X)}}=\frac{X-np}{\sqrt{npq}}\\\quad\quad(Bin(n,p)において, E(X)=np,V(X)=npq)$$
$$(試行回数が十分な二項分布内の値xに近似しているZ)=\frac{(x-分散)}{(標準偏差)}$$
<a name="ee"></a>
##~第5回~
###①標本平均 $\overline{X}$ の期待値$E(\overline{X})$ と分散$E(\overline{X})$
######(標本平均)=(標本抽出での頻度を度数と見た時の相対度数)$\times$(階級値)
$$E(\overline{X})=\mu, V(\overline{X})=\frac{\sigma^2}{n}\tag{41, 42}$$
$$(期待値)=(母平均), (分散)=\frac{(母分散)}{(標本数)}$$
###②標本分散$S^2$とその期待値及び平均$E(S^2)$
$$S^2=\frac{1}{n}\sum({X}_k-\overline{X})^2,\quad E(S^2)=\frac{n-1}{n}\sigma^2\tag{43,44}$$
$$(標本分散)=\sum(標本の偏差)^2÷(標本数),\quad(標本分散の期待値,平均)=(\frac{標本数-1}{標本数})\times(母分散)$$
###③母分散$V(X_k)$
$$\begin{eqnarray}V(X_k)&=&E\Big((X_k-E(X_k))^2\Big)\\&=&E\Big((X_k)-\mu\Big)=\sigma^2\end{eqnarray}\tag{43}$$
$$(母分散)=\bigg\{\Big((各値-期待値)^2\Big)の期待値\bigg\}$$
###④不偏分散$U^2$
######(この期待値が母分散に一致. 標本分散から母分散を求める時用いる.)
$$\begin{eqnarray}U^2\bigg(=\frac{n}{n-1}S^2\bigg)&=&\frac{n}{n-1}・\frac{1}{n}\sum(X_k-\overline{X})^2\\&=&\frac{1}{n-1}\sum(X_k-\overline{X})^2\end{eqnarray}\tag{44}$$
$$(不偏分散)=(各標本値-標本平均)^2÷（標本数－1）$$
$$\Bigg((U^2の期待値)=E(U^2)=(母分散)\Bigg)$$
###⑤中心極限定理
######(=母集団が正規分布に不従の場合で標本数$n$が十分大きい時に標本平均を正規分布へ近似化する.)
$$T=\frac{\overline{X}-E(X)}{\sqrt{V(\overline{X})}}=\frac{\overline{X}-\mu}{\sigma/\sqrt{n}}\tag{45}$$
$$標本平均\overline{X}:N(\mu, \frac{\sigma^2}{n})に近似的に従う.\to T:N(0,1)に近似的に従う.$$
###⑥信頼区間(信頼度: 95\%$\to$1.96, 99\%$\to$2.58)
######(母分散既知の場合,母平均の推定に用いるべし.)
- 母平均 $\mu$が既知で, $|T|\leqq1.96$の時の, 95\%信頼区間
  - $$P\bigg(-1.96\leqq \frac{\overline{X}-\mu}{\sigma/\sqrt{n}}(=T)\leqq 1.96\bigg)=0.95\quad(95\%)\tag{46}$$
- 母平均 $\mu$が未知の時の, $\mu$の信頼度95\%の信頼区間
  - $$\overline{x}-\frac{1.96\sigma}{\sqrt{n}} \leqq\mu\leqq\overline{x}+\frac{1.96\sigma}{\sqrt{n}}\tag{47}$$
###⑦不偏分散
######(母分散未知の場合, 自由度$k(=n-1)$ の$t$分布とともに母平均の推定に用いる.)
$$U^2\bigg(=\frac{n}{n-1}S^2\bigg)=\frac{1}{n-1}\sum(X_k-\overline{X})^2,\quad T=\frac{\overline{X}-\mu}{U/\sqrt{n}}\tag{48, 49}$$
<a name="ff"></a>
##~第6回~
###①95\%信頼区間と母平均 $\mu$の95\%信頼区間
######(母分散未知の時用いるべし.)
$$P\Bigg(-t_{n-1}(0.025)\leqq\frac{\overline{X}-\mu}{U/\sqrt{n}}(=T)\leqq t_{n-1}(0.025)\Bigg)=0.95\quad(95\%)\tag{50}$$
$$\overline{X}-\frac{t_{n-1}(0.025)U}{\sqrt{n}} \leqq\mu\leqq\overline{X}+\frac{t_{n-1}(0.025)U}{\sqrt{n}}\tag{51}$$
###②自由度$n=k$ の $\chi^2$分布
######(=標本$X_1,X_2,・・・,X_n$が独立に$N（0,1）$ に従う時のこれらの平方和 $\sum X_n^2$の従う分布. 母分散の推定に用いる. )
$$T\bigg(=\frac{1}{\sigma^2}\sum_{i=1}^{n}(X_i-\overline{X})^2\bigg)=\frac{nS^2}{\sigma^2}\quad\bigg(S^2は\frac{1}{n}\sum_{i=1}^{n}(X_i-\overline{X})^2で表される標本分散.\bigg)\tag{52}$$
###③ $\chi^2$分布における95\%信頼区間と母分散両側95\%信頼区間
$$P\Bigg(\chi_{n-1}^{2}(0.975)\leqq \frac{nS^2}{\sigma^2}(=T)\leqq\chi_{n-1}^{2}(0.025)\Bigg)=0.95\quad(95\%)\tag{53}$$
$$\frac{nS^2}{\chi_{n-1}^{2}(0.025)}\leqq\sigma\leqq\frac{nS^2}{\chi_{n-1}^{2}(0.0975)}\tag{54}$$
###④標本比 $\overline{p}$
######(=全体に対する割合(確率)である母比率の補集合. 母比率の推定に用いるべし.)
$$T=\frac{\overline{p}-p}{\sqrt{p(1-p)/n}}\tag{55}$$
$$標本比\overline{p}=X/n:N(p,\frac{p(1-p)}{n})に近似的に従う.\to T:N(0,1)に従う.$$
###⑤母比率$p$分布における95\%の信頼区間と母比率の95\%信頼区間
$$P\bigg(-1.96\leqq\frac{\overline{p}-p}{\sqrt{p(1-p)/n}}(=T)\leqq 1.96\bigg)=0.95\quad(95\%)\tag{56}$$
$$\overline{p}-1.96\sqrt{\frac{p(1-p)}{n}}\leqq p \leqq\overline{p}+1.96\sqrt{\frac{p(1-p)}{n}}\tag{57}$$
<a name="11"></a>
# 2B) 生活の実際における統計の利用例
##例その1 - 物価統計
###意味
>市場で取引される商品･サービスの価格変動を測定することを目的とした統計調査の総称であり，調査対象，価格調査段階等を異にする各種の物価統計がある。  
>(世界大百科事典 第２版の解説)  
>[コトバンク - 「物価統計」 の項目](https://kotobank.jp/word/%E7%89%A9%E4%BE%A1%E7%B5%B1%E8%A8%88-1201661)より引用
###用途
- [物価指数](https://kotobank.jp/word/%E7%89%A9%E4%BE%A1%E6%8C%87%E6%95%B0-125069#E4.B8.96.E7.95.8C.E5.A4.A7.E7.99.BE.E7.A7.91.E4.BA.8B.E5.85.B8.20.E7.AC.AC.EF.BC.92.E7.89.88)に計算し直されて, 社会の経済状況や景気の判断材料として用いられる.  

主に,
  - 需給を反映し, 景気の状況を判断する材料となる[卸売物価指数](https://kotobank.jp/word/%E5%8D%B8%E5%A3%B2%E7%89%A9%E4%BE%A1%E6%8C%87%E6%95%B0-2121#E7.99.BE.E7.A7.91.E4.BA.8B.E5.85.B8.E3.83.9E.E3.82.A4.E3.83.9A.E3.83.87.E3.82.A3.E3.82.A2)
  - 消費財の価格の水準を示す[消費者物価指数](https://kotobank.jp/word/%E6%B6%88%E8%B2%BB%E8%80%85%E7%89%A9%E4%BE%A1%E6%8C%87%E6%95%B0-79751#E7.99.BE.E7.A7.91.E4.BA.8B.E5.85.B8.E3.83.9E.E3.82.A4.E3.83.9A.E3.83.87.E3.82.A3.E3.82.A2)  

などがその代表である.
###影響
- [このサイト](https://www.tokaitokyo.co.jp/otome/investment/finance/prices/point.html)によると,「**厚生年金や国民年金などの公的年金の給付額**」に影響が出るのだという.
- またある研究員によると, 物価統計によって日銀や銀行は金融政策や融資等を行うため, その動向によって私達は間接的に影響を受けているのだという.  
(参照:[消費者物価指数（CPI）の「正体」とは？ | リコー経済社会研究所 | リコーグループ 企業・IR | リコー](http://blog.ricoh.co.jp/RISB/inout_economy/cpi.html))
##例その2 - 毎月勤労統計
###意味
> 賃金、労働時間及び雇用の変動を明らかにすることを目的に厚生労働省が実施する調査です.  
> その前身も含めると大正12年から始まっており、統計法（平成19年法律第53号）に基づき、国の重要な統計調査である基幹統計調査として実施しています。  
> 毎月勤労統計調査は、常用労働者5人以上の事業所を対象として毎月実施する全国調査及び都道府県別に実施する地方調査のほか、常用労働者1～4人の事業所を対象として年1回7月分について特別調査を実施しています。  
> [厚生労働省：毎月勤労統計調査って何？](https://www.mhlw.go.jp/topics/2006/12/tp1201-1.html#01)より引用

###用途
主に,
- **雇用保険や労災保険の給付額**を改定する際の資料  
- 民間企業等における**給与改正や人件費**の算定
- **日本の労働事情を表す**資料  

等に使われているという.
(参照:[厚生労働省：毎月勤労統計調査って何？](https://www.mhlw.go.jp/topics/2006/12/tp1201-1.html#06))  

###影響
> - 先の2019年1月12日, 2004年以降, 東京都では(…)3分の1程度の抽出調査を行っていたことが明らかになった.
> - 雇用保険や労災保険が本来より少なく支給されたなど影響が出ていたことがわかった.  
> [「毎月勤労統計」不正問題、厚労部会でヒアリング](https://blogos.com/article/351379/)より引用
