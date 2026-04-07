

ベイズ理論による統計的予測に関する文書の第 1 章「序論」の重要な数式とその意味を、体系的に解説します。

---

## 1. 多項式曲線フィッティング

### (1.1) 多項式関数

$$
y(x, \mathbf{w}) = w_0 + w_1 x + w_2 x^2 + \cdots + w_M x^M = \sum_{j=0}^{M} w_j x^j
$$

**意味**: 
- これは**多項式回帰モデル**を表しています
- $w$ はパラメータ（重み）ベクトル、$M$ は多項式の次数
- $x^j$ は $x$ の $j$ 乗
- このモデルは $w$ に関しては**線形**ですが、$x$ に関しては**非線形**です

---

### (1.2) 二乗和誤差関数（Error Function）

$$
E(\mathbf{w}) = \frac{1}{2} \sum_{n=1}^{N} \{y(x_n, \mathbf{w}) - t_n\}^2
$$

**意味**:
- 予測値 $y(x_n, w)$ と目標値 $t_n$ の**二乗誤差**の合計
- $1/2$ の係数は微分時に係数 2 を打ち消しやすくするため
- **最小二乗法**の基礎となる関数
- この関数を最小化することで、最適なパラメータ $w*$ が得られる

---

### (1.3) RMS 誤差（Root-Mean-Square Error）

$$
E_{\mathrm{RMS}} = \sqrt{2E(\mathbf{w}^*)/N}
$$

**意味**:
- 平均二乗平方根誤差
- $N$ で割ることでデータサイズが異なる場合でも比較可能
- 平方根を取ることで、目的変数 $t$ と同じ尺度（単位）になる

---

### (1.4) 正則化された誤差関数

$$
\widetilde{E}(\mathbf{w}) = \frac{1}{2} \sum_{n=1}^{N} \{y(x_n, \mathbf{w}) - t_n\}^2 + \frac{\lambda}{2} \|\mathbf{w}\|^2
$$

**意味**:
- **正則化項**（$λ/2 \|w\|^2$）を追加した誤差関数
- $\|w\|^2 = w_0^2 + w_1^2 + \cdots + w_M^2$（L2 ノルム）
- $λ$（ラムダ）は正則化パラメータ
- 大きな係数の値を防ぎ、**過学習（overfitting）**を抑制
- **リッジ回帰**（ridge regression）または**荷重減衰**（weight decay）として知られる

---

## 2. 確率論の基本

### 確率の基本法則

#### 加法定理（Sum Rule）

$$
p(X) = \sum_Y p(X, Y)
$$

**意味**:
- **周辺化**（marginalization）を表す
- 同時確率 $p(X,Y)$ を $Y$ について足し合わせて、$X$ の周辺確率を得る
- 離散変数の場合の式で、連続変数の場合は和が積分になる

---

#### 乗法定理（Product Rule）

$$
p(X, Y) = p(Y \mid X) p(X)
$$

**意味**:
- 同時確率を条件付き確率と周辺確率の積に分解
- $p(Y | X)$ は「$X$ が与えられた下での $Y$ の確率」

---

#### ベイズの定理（Bayes' Theorem）

$$
p(Y \mid X) = \frac{p(X \mid Y) p(Y)}{p(X)}
$$

**意味**:
- 条件付き確率を**逆転**させる基本的な定理
- 右辺:
  - $p(X | Y)$: **尤度**（likelihood）- パラメータ $Y$ が与えられたときデータ $X$ が見られる確率
  - $p(Y)$: **事前確率**（prior）- データを見る前の $Y$ に関する確率
  - $p(X)$: **規格化定数**（evidence）- 全ての $Y$ について $p(X | Y)p(Y)$ を和としたもの
- 左辺:
  - $p(Y | X)$: **事後確率**（posterior）- データ $X$ を観測した後の $Y$ に関する確率

---

### (1.43) ベイズ曲線フィッティングの核心

$$
p(\mathbf{w} \mid \mathcal{D}) = \frac{p(\mathcal{D} \mid \mathbf{w}) p(\mathbf{w})}{p(\mathcal{D})}
$$

**意味**:
- データ $\mathcal{D}$ を観測した後のパラメータ $\mathbf{w}$ の**事後分布**
- **事後確率 ∝ 尤度 × 事前確率**というベイズ推論の基本式
- $\mathcal{D} = \{t_1, \dots, t_N\}$ は観測されたデータ集合

---

### (1.44) 規格化定数

$$
p(\mathcal{D}) = \int p(\mathcal{D} \mid \mathbf{w}) p(\mathbf{w}) \, d\mathbf{w}
$$

**意味**:
- ベイズの定理の分母
- 事後分布が確率密度関数として規格化されることを保証
- パラメータ $w$ に関する**周辺化**（marginalization）

---

## 3. ガウス分布（正規分布）

### (1.46) 1 変数ガウス分布

$$
\mathcal{N}(x \mid \mu, \sigma^2) = \frac{1}{(2\pi\sigma^2)^{1/2}} \exp\left\{-\frac{1}{2\sigma^2}(x - \mu)^2\right\}
$$

**意味**:
- **最最重要の確率分布**の一つ
- $\mu$: **平均**（mean）- 分布の中心位置
- $\sigma^2$: **分散**（variance）- ばらつきの大きさ
- $\sigma$: **標準偏差**（standard deviation）
- $\beta = 1/\sigma^2$: **精度パラメータ**（precision parameter）
- 鐘型の対称な分布

---

### (1.47) ガウス分布の正値性

$$
\mathcal{N}(x \mid \mu, \sigma^2) > 0
$$

**意味**:
- ガウス分布は全ての $x$ に対して正の値を取る
- 確率密度関数の必要条件を満たす

---

### (1.48) ガウス分布の規格化条件

$$
\int_{-\infty}^{\infty} \mathcal{N}(x \mid \mu, \sigma^2) \, dx = 1
$$

**意味**:
- 全領域での積分が 1 になり、確率密度関数としての要件を満たす

---

### (1.49)-(1.51) ガウス分布のモーメント

$$
\mathbb{E}[x] = \int_{-\infty}^{\infty} \mathcal{N}(x \mid \mu, \sigma^2) x \, dx = \mu
$$

$$
\mathbb{E}[x^2] = \int_{-\infty}^{\infty} \mathcal{N}(x \mid \mu, \sigma^2) x^2 \, dx = \mu^2 + \sigma^2
$$

$$
\operatorname{var}[x] = \mathbb{E}[x^2] - \mathbb{E}[x]^2 = \sigma^2
$$

**意味**:
- $\mathbb{E}[x]$: $x$ の**期待値**（平均）は $\mu$ に一致
- $\mathbb{E}[x^2]$: **2 次のモーメント**
- $\operatorname{var}[x]$: **分散**はパラメータ $\sigma^2$ に一致

---

### (1.52) 多変量ガウス分布

$$
\mathcal{N}(\mathbf{x} \mid \boldsymbol{\mu}, \boldsymbol{\Sigma}) = \frac{1}{(2\pi)^{D/2}} \frac{1}{|\boldsymbol{\Sigma}|^{1/2}} \exp\left\{-\frac{1}{2}(\mathbf{x} - \boldsymbol{\mu})^\mathrm{T} \boldsymbol{\Sigma}^{-1} (\mathbf{x} - \boldsymbol{\mu})\right\}
$$

**意味**:
- $D$ 次元空間におけるガウス分布
- $\boldsymbol{\mu}$: $D$ 次元の平均ベクトル
- $\boldsymbol{\Sigma}$: $D × D$ の**共分散行列**（covariance matrix）
- $|\boldsymbol{\Sigma}|$: 共分散行列の**行列式**
- $(\mathbf{x} - \boldsymbol{\mu})^\mathrm{T} \boldsymbol{\Sigma}^{-1} (\mathbf{x} - \boldsymbol{\mu})$: **マハラノビス距離**の 2 乗（標準化された距離）

---

### (1.53) ガウス分布の尤度関数

$$
p(\mathbf{x} \mid \mu, \sigma^2) = \prod_{n=1}^{N} \mathcal{N}(x_n \mid \mu, \sigma^2)
$$

**意味**:
- 独立同分布（i.i.d.）な $N$ 個の観測値の**同時尤度**
- 各データ点は同じガウス分布から独立に生成されると仮定
- $\prod$（積）は、各観測値の確率密度の積

---

### (1.54) 対数尤度関数

$$
\ln p(\mathbf{x} \mid \mu, \sigma^2) = -\frac{1}{2\sigma^2} \sum_{n=1}^{N} (x_n - \mu)^2 - \frac{N}{2} \ln \sigma^2 - \frac{N}{2} \ln(2\pi)
$$

**意味**:
- 尤度関数の**対数**を取ったもの
- 対数を取る理由：
  1. 積を和に変える（計算が簡単）
  2. 小さな確率値の積によるアンダーフローを避ける
  3. 対数は単調増加関数なので最大化は等価
- 最大尤度推定（MLE）はこの関数を最大化することでパラメータを求める

---

### (1.55) 平均の最尤推定量

$$
\mu_{\mathrm{ML}} = \frac{1}{N} \sum_{n=1}^{N} x_n
$$

**意味**:
- ガウス分布の平均 $\mu$ の**最尤推定量**
- **標本平均**（サンプル平均）
- 観測値の単純な平均

---

### (1.56) 分散の最尤推定量

$$
\sigma_{\mathrm{ML}}^2 = \frac{1}{N} \sum_{n=1}^{N} (x_n - \mu_{\mathrm{ML}})^2
$$

**意味**:
- 分散 $\sigma^2$ の最尤推定量
- **標本分散**（サンプル分散）
- **バイアスがある**（後述）

---

### (1.57)-(1.58) 最尤推定バイアス

$$
\mathbb{E}[\mu_{\mathrm{ML}}] = \mu
$$

$$
\mathbb{E}[\sigma_{\mathrm{ML}}^2] = \left(\frac{N-1}{N}\right) \sigma^2
$$

**意味**:
- $\mu_{\mathrm{ML}}$ の期待値は真の平均 $\mu$ に等しい（不偏推定量）
- $\sigma_{\mathrm{ML}}^2$ の期待値は真の分散の $(N-1)/N$ 倍（**系統的に過小評価**）
- このバイアスは、データ点数 $N$ が小さいほど深刻

---

### (1.59) 不偏分散推定量

$$
\widetilde{\sigma}^2 = \frac{N}{N-1} \sigma_{\mathrm{ML}}^2 = \frac{1}{N-1} \sum_{n=1}^{N} (x_n - \mu_{\mathrm{ML}})^2
$$

**意味**:
- 不偏推定量（バイアスなし）の分散推定量
- 分母を $N$ から $N-1$ にすることでバイアスを補正

---

## 4. 確率モデルとしての曲線フィッティング

### (1.60) 条件付きガウス分布

$$
p(t \mid x, \mathbf{w}, \beta) = \mathcal{N}\left(t \mid y(x, \mathbf{w}), \beta^{-1}\right)
$$

**意味**:
- 回帰問題における**確率モデル**
- 入力 $x$ が与えられたとき、目標値 $t$ はガウス分布に従う
- 平均：多項式 $y(x, w)$
- 分散：$\beta^{-1}$（$\beta$ は精度パラメータ）
- **観測ノイズ**を確率的に表現

---

### (1.61) 回帰問題の尤度関数

$$
p(\mathbf{t} \mid \mathbf{x}, \mathbf{w}, \beta) = \prod_{n=1}^{N} \mathcal{N}\left(t_n \mid y(x_n, \mathbf{w}), \beta^{-1}\right)
$$

**意味**:
- 訓練データ $\{x, t\}$ 全体の尤度関数
- 各データ点は独立にガウス分布から生成されると仮定
- この尤度を最大化する $w$ を求めることで回帰問題が解ける

---

### (1.62) 対数尤度関数（回帰）

$$
\ln p(\mathbf{t} \mid \mathbf{x}, \mathbf{w}, \beta) = -\frac{\beta}{2} \sum_{n=1}^{N} \{y(x_n, \mathbf{w}) - t_n\}^2 + \frac{N}{2} \ln \beta - \frac{N}{2} \ln(2\pi)
$$

**意味**:
- 回帰問題における対数尤度関数
- **第 1 項**: 二乗和誤差项（$w$ によって制御）
- **第 2-3 項**: $w$ に依存しない項
- この式から、二乗誤差最小化は**ノイズがガウス分布という仮定の下での尤度最大化**と等価であることが導かれる

---

### (1.63) 精度パラメータの最尤推定

$$
\frac{1}{\beta_{\mathrm{ML}}} = \frac{1}{N} \sum_{n=1}^{N} \{y(x_n, \mathbf{w}_{\mathrm{ML}}) - t_n\}^2
$$

**意味**:
- 精度パラメータ $\beta$ の最尤推定量
- 分散 $\beta^{-1}$ は、残差（誤差）の二乗平均に等しい
- これもバイアスがある（1.2.4 節同様）

---

### (1.64) 予測分布（最尤）

$$
p(t \mid x, \mathbf{w}_{\mathrm{ML}}, \beta_{\mathrm{ML}}) = \mathcal{N}\left(t \mid y(x, \mathbf{w}_{\mathrm{ML}}), \beta_{\mathrm{ML}}^{-1}\right)
$$

**意味**:
- 最尤推定パラメータを用いた**予測分布**
- 新たな $x$ に対する $t$ の確率分布を返す
- 点予測だけでなく、**不確実性**も評価可能

---

## 5. ベイズ曲線フィッティング

### (1.65) パラメータの事前分布

$$
p(\mathbf{w} \mid \alpha) = \mathcal{N}(\mathbf{w} \mid \mathbf{0}, \alpha^{-1} \mathbf{I}) = \left(\frac{\alpha}{2\pi}\right)^{(M+1)/2} \exp\left\{-\frac{\alpha}{2} \mathbf{w}^\mathrm{T} \mathbf{w}\right\}
$$

**意味**:
- パラメータ $w$ に対する**事前分布**（ベイズ的アプローチ）
- 平均：ゼロベクトル $\mathbf{0}$
- 共分散：$\alpha^{-1} \mathbf{I}$（対角行列）
- $\alpha$: 事前分布の**精度パラメータ**
- **超パラメータ**（モデルパラメータを制御するパラメータ）
- 係数をゼロに近い値に引きずる事前信念

---

### (1.66) 事後分布

$$
p(\mathbf{w} \mid \mathbf{x}, \mathbf{t}, \alpha, \beta) \propto p(\mathbf{t} \mid \mathbf{x}, \mathbf{w}, \beta) p(\mathbf{w} \mid \alpha)
$$

**意味**:
- ベイズの定理から：事後確率 ∝ 尤度 × 事前確率
- データ $\{x, t\}$ を観測した後のパラメータ $w$ の分布

---

### (1.67) 最大事後確率（MAP）推定

$$
\frac{\beta}{2} \sum_{n=1}^{N} \{y(x_n, \mathbf{w}) - t_n\}^2 + \frac{\alpha}{2} \mathbf{w}^\mathrm{T} \mathbf{w}
$$

**意味**:
- 事後分布を最大化する $w$ を求める際の目的関数
- **第 1 項**: 二乗和誤差
- **第 2 項**: L2 正則化項
- $\lambda = \alpha/\beta$ の正則化項
- **MAP 推定は正則化された最小二乗法と等価**

---

### (1.68) 完全ベイズ予測分布

$$
p(t \mid x, \mathbf{x}, \mathbf{t}) = \int p(t \mid x, \mathbf{w}) p(\mathbf{w} \mid \mathbf{x}, \mathbf{t}) \, d\mathbf{w}
$$

**意味**:
- 完全なベイズ的アプローチ
- パラメータ $w$ に関する**すべての値を積分**（周辺化）
- 点推定ではなく、パラメータの不確実性を考慮
- ベイズ推論の根幹となる式

---

### (1.69) 予測分布の形

$$
p(t \mid x, \mathbf{x}, \mathbf{t}) = \mathcal{N}\left(t \mid m(x), s^2(x)\right)
$$

**意味**:
- 曲線フィッティングでは、予測分布もガウス分布になる
- 平均 $m(x)$ と分散 $s^2(x)$ を計算することで予測が可能

---

### (1.70)-(1.71) 予測分布の平均と分散

$$
m(x) = \beta \phi(x)^\mathrm{T} \mathbf{S} \sum_{n=1}^{N} \phi(x_n) t_n
$$

$$
s^2(x) = \beta^{-1} + \phi(x)^\mathrm{T} \mathbf{S} \phi(x)
$$

**意味**:
- **平均 $m(x)$**: データに基づく予測の中心
- **分散 $s^2(x)$** は 2 つの部分からなる：
  1. $\beta^{-1}$: **データノイズによる不確実性**（最尤予測と同じ）
  2. $\phi(x)^\mathrm{T} \mathbf{S} \phi(x)$: **パラメータ $w$ の不確実性**（ベイズ的な項）
- 学習データが少ない領域では、パラメータ不確実性が大きくなる

---

### (1.72) 共分散行列 $\mathbf{S}$

$$
\mathbf{S}^{-1} = \alpha \mathbf{I} + \beta \sum_{n=1}^{N} \phi(x_n) \phi(x_n)^\mathrm{T}
$$

**意味**:
- 事後分布の共分散行列の逆数
- **事前情報**（$\alpha \mathbf{I}$）と**データ情報**（和の項）のバランス
- $\phi(x)$ は基底関数ベクトル：$\phi_i(x) = x^i$（$i = 0, \dots, M$）

---

## 6. 決定理論

### (1.82) ベイズの定理（分類問題）

$$
p(\mathcal{C}_k \mid \mathbf{x}) = \frac{p(\mathbf{x} \mid \mathcal{C}_k) p(\mathcal{C}_k)}{p(\mathbf{x})}
$$

**意味**:
- クラス分類におけるベイズの定理
- $p(\mathcal{C}_k)$: **クラス事前確率**
- $p(\mathbf{x} \mid \mathcal{C}_k)$: **クラス条件付き密度**（尤度）
- $p(\mathbf{x})$: 規格化定数
- $p(\mathcal{C}_k \mid \mathbf{x})$: **クラス事後確率**

---

### (1.83) 規格化定数

$$
p(\mathbf{x}) = \sum_k p(\mathbf{x} \mid \mathcal{C}_k) p(\mathcal{C}_k)
$$

**意味**:
- 全てのクラスについて尤度×事前確率の和
- 確率分布として規格化されることを保証

---

### (1.78) 誤識別率

$$
p(\text{誤り}) = \int_{\mathcal{R}_1} p(\mathbf{x}, \mathcal{C}_2) \, d\mathbf{x} + \int_{\mathcal{R}_2} p(\mathbf{x}, \mathcal{C}_1) \, d\mathbf{x}
$$

**意味**:
- 誤って分類される確率
- $\mathcal{R}_k$: クラス $\mathcal{C}_k$ の**決定領域**
- 誤識別率を最小化する決定規則は**事後確率が最大**のクラスを選ぶこと

---

### (1.80) 期待損失

$$
\mathbb{E}[L] = \sum_k \sum_j \int_{\mathcal{R}_j} L_{kj} p(\mathbf{x}, \mathcal{C}_k) \, d\mathbf{x}
$$

**意味**:
- 異なる種類の誤りが異なる損失をもたらす場合の**期待損失**
- $L_{kj}$: 真のクラス $\mathcal{C}_k$ をクラス $\mathcal{C}_j$ と誤分類したときの**損失**
- 各 $x$ に対して**期待損失が最小**となるクラスを選択

---

### (1.81) 期待損失最小化の決定規則

$$
\sum_k L_{kj} p(\mathcal{C}_k \mid \mathbf{x})
$$

**意味**:
- 各 $x$ に対して、この値が最小となるクラス $\mathcal{C}_j$ を選ぶ
- 事後確率がわかれば自動的に決定できる

---

## 7. 回帰のための損失関数

### (1.87) 期待損失

$$
\mathbb{E}[L] = \iint \{y(\mathbf{x}) - t\}^2 p(\mathbf{x}, t) \, d\mathbf{x} \, dt
$$

**意味**:
- 回帰問題における二乗誤差の期待値
- 最適な関数 $y(x)$ を求めるための基準

---

### (1.88)-(1.89) 最適解

$$
\frac{\delta \mathbb{E}[L]}{\delta y(\mathbf{x})} = 2 \int \{y(\mathbf{x}) - t\} p(\mathbf{x}, t) \, dt = 0
$$

$$
y(\mathbf{x}) = \int t p(t \mid \mathbf{x}) \, dt = \mathbb{E}_t[t \mid \mathbf{x}]
$$

**意味**:
- 変分法による最適化
- **最適解は条件付き平均**（回帰関数）
- x が与えられた下での $t$ の期待値

---

### (1.90) 期待損失の分解

$$
\mathbb{E}[L] = \int \{y(\mathbf{x}) - \mathbb{E}[t \mid \mathbf{x}]\}^2 p(\mathbf{x}) \, d\mathbf{x} + \int \operatorname{var}[t \mid \mathbf{x}] p(\mathbf{x}) \, d\mathbf{x}
$$

**意味**:
- 期待損失を 2 つの項に分解
  1. **近似誤差**: $y(x)$ と条件付き平均の乖離
  2. **ノイズ項**: データの本質的な変動（避けられない損失）
- $y(x) = \mathbb{E}[t \mid x]$ のとき第 1 項が 0 になる

---

## 8. 情報理論

### (1.92) 情報量

$$
h(x) = -\log_2 p(x)
$$

**意味**:
- 事象 $x$ の**情報量**
- 起きにくい事象ほど情報量が多い
- 単位：**ビット**（底 2 の対数）

---

### (1.93) エントロピー

$$
\mathrm{H}[x] = -\sum_x p(x) \log_2 p(x)
$$

**意味**:
- 確率変数 $x$ の**エントロピー**
- 乱雑さ・不確実さの尺度
- 確率分布が一様に近いほどエントロピー大

---

### 微分エントロピー

$$
\mathrm{H}[x] = -\int p(x) \ln p(x) \, dx
$$

**意味**:
- 連続変数に対するエントロピー
- 単位：**ナット**（自然対数）

---

### (1.113) 相対エントロピー（KL ダイバージェンス）

$$
\mathrm{KL}(p \| q) = -\int p(\mathbf{x}) \ln q(\mathbf{x}) \, d\mathbf{x} - \left(-\int p(\mathbf{x}) \ln p(\mathbf{x}) \, d\mathbf{x}\right) = -\int p(\mathbf{x}) \ln \frac{q(\mathbf{x})}{p(\mathbf{x})} \, d\mathbf{x}
$$

**意味**:
- 2 つの確率分布 $p$ と $q$ の**違い**を測る尺度
- $\mathrm{KL}(p \| q) \geq 0$（等号は $p = q$ のとき）
- **対称ではない**（$p$ と $q$ を入れ替えると異なる値）

---

### (1.121) 相互情報量

$$
\mathrm{I}[\mathbf{x}, \mathbf{y}] = \mathrm{KL}(p(\mathbf{x}, \mathbf{y}) \| p(\mathbf{x})p(\mathbf{y})) = -\iint p(\mathbf{x}, \mathbf{y}) \ln \frac{p(\mathbf{x})p(\mathbf{y})}{p(\mathbf{x}, \mathbf{y})} \, d\mathbf{x} \, d\mathbf{y}
$$

**意味**:
- 2 つの変数 $\mathbf{x}$, $\mathbf{y}$ の**相互依存度**
- 独立なら 0、独立でないなら正
- **$\mathbf{y}$ の情報を知ることが $\mathbf{x}$ の不確実性をどれだけ減らすか**を表す

---

### (1.122) 相互情報量の別表現

$$
\mathrm{I}[\mathbf{x}, \mathbf{y}] = \mathrm{H}[\mathbf{x}] - \mathrm{H}[\mathbf{x} \mid \mathbf{y}] = \mathrm{H}[\mathbf{y}] - \mathrm{H}[\mathbf{y} \mid \mathbf{x}]
$$

**意味**:
- 相互情報量は、エントロピーの減少として解釈可能
- 情報の交換・共有の尺度

---

## まとめ

第 1 章ではパターン認識と機械学習の基礎となる重要な数学的概念を導入しました：

| セクション | 核心概念 | 重要な数式 |
|-----------|---------|-----------|
| 1.1 | 多項式曲線フィッティング | (1.1), (1.2), (1.4) |
| 1.2 | 確率論の基本 | (1.7), (1.11), (1.43) |
| 1.2.4 | ガウス分布 | (1.46), (1.52), (1.55) |
| 1.2.5 | 確率的曲線フィッティング | (1.60), (1.67) |
| 1.2.6 | ベイズ曲線フィッティング | (1.68), (1.70), (1.71) |
| 1.5 | 決定理論 | (1.78), (1.81) |
| 1.6 | 情報理論 | (1.93), (1.113), (1.121) |

これらの数学的基礎が、本書で扱われる高度な機械学習手法の理解へと繋がっていきます。
