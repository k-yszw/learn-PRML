# PRML2 数式一覧（tag付き）

抽出元: PRML2.md

## 式1 (tag: 2.1)

$$

p ( x = 1 | \mu ) = \mu\tag{2.1}

$$

## 式2 (tag: 2.2)

$$

\operatorname { B e r n } ( x | \mu ) = \mu _ { \cdot } ^ { x } ( 1 - \mu ) ^ { 1 - x }\tag{2.2}

$$

## 式3 (tag: 2.3)

$$

\mathbb { E } [ x ] = \mu\tag{2.3}

$$

## 式4 (tag: 2.4)

$$

\operatorname { v a r } [ x ] = \mu ( 1 - \mu )\tag{2.4}

$$

## 式5 (tag: 2.5)

$$

p ( \mathcal { D } | \mu ) = \prod _ { n = 1 } ^ { N } p ( x _ { n } | \mu ) = \prod _ { n = 1 } ^ { N } \mu ^ { x _ { n } } ( 1 - \mu ) ^ { 1 - x _ { n } } .\tag{2.5}

$$

## 式6 (tag: 2.6)

$$

\ln p ( \mathcal { D } | \mu ) = \sum _ { n = 1 } ^ { N } \ln p ( x _ { n } | \mu ) = \sum _ { n = 1 } ^ { N } \left\{ x _ { n } \ln \mu + ( 1 - x _ { n } ) \ln ( 1 - \mu ) \right\} .\tag{2.6}

$$

## 式7 (tag: 2.7)

$$

\mu _ { \mathrm { M L } } = \frac { 1 } { N } \sum _ { n = 1 } ^ { N } x _ { n }\tag{2.7}

$$

## 式8 (tag: 2.8)

$$

\mu _ { \mathrm { M L } } = { \frac { m } { N } }\tag{2.8}

$$

## 式9 (tag: 2.9)

$$

\mathrm { B i n } ( m | N , \mu ) = \binom { N } { m } \mu ^ { m } ( 1 - \mu ) ^ { N - m } .\tag{2.9}

$$

## 式10 (tag: 2.10)

$$

{ \binom { N } { m } } \equiv \frac { N ! } { ( N - m ) ! m ! }\tag{2.10}

$$

## 式11 (tag: 2.11)

$$

\mathbb { E } [ m ] \equiv \sum _ { m = 0 } ^ { N } m \mathrm { B i n } ( m | N , \mu ) = N \mu\tag{2.11}

$$

## 式12 (tag: 2.12)

$$

\operatorname { v a r } [ m ] \equiv \sum _ { m = 0 } ^ { N } { \big ( } m - \mathbb { E } [ m ] { \big ) } ^ { 2 } \operatorname { B i n } ( m | N , \mu ) = N \mu ( 1 - \mu )\tag{2.12}

$$

## 式13 (tag: 2.13)

$$

\mathrm { B e t a } ( \mu | a , b ) = { \frac { \Gamma ( a + b ) } { \Gamma ( a ) \Gamma ( b ) } } \mu ^ { a - 1 } ( 1 - \mu ) ^ { b - 1 } .\tag{2.13}

$$

## 式14 (tag: 2.14)

$$

\int _ { 0 } ^ { 1 } \mathrm { B e t a } ( \mu | a , b ) \mathrm { d } \mu = 1\tag{2.14}

$$

## 式15 (tag: 2.15)

$$

 \mathbb { E } [ \mu ] = \frac { a } { a + b }\tag{2.15}

$$

## 式16 (tag: 2.16)

$$

\operatorname { v a r } [ \mu ] = { \frac { a b } { ( a + b ) ^ { 2 } ( a + b + 1 ) } }\tag{2.16}

$$

## 式17 (tag: 2.17)

$$

p ( \mu | m , l , a , b ) \propto \mu ^ { m + a - 1 } ( 1 - \mu ) ^ { l + b - 1 }\tag{2.17}

$$

## 式18 (tag: 2.18)

$$

p ( \mu | m , l , a , b ) = \frac { \Gamma ( m + a + l + b ) } { \Gamma ( m + a ) \Gamma ( l + b ) } \mu ^ { m + a - 1 } ( 1 - \mu ) ^ { l + b - 1 }\tag{2.18}

$$

## 式19 (tag: 2.19)

$$

p ( x = 1 | \mathcal { D } ) = \int _ { 0 } ^ { 1 } p ( x = 1 | \mu ) p ( \mu | \mathcal { D } ) \mathrm { d } \mu = \int _ { 0 } ^ { 1 } \mu p ( \mu | \mathcal { D } ) \mathrm { d } \mu = \mathbb { E } [ \mu | \mathcal { D } ]\tag{2.19}

$$

## 式20 (tag: 2.20)

$$

p ( x = 1 | \mathcal { D } ) = \frac { m + a } { m + a + l + b }\tag{2.20}

$$

## 式21 (tag: 2.21)

$$

\mathbb { E } _ { \pmb { \theta } } [ \pmb { \theta } ] = \mathbb { E } _ { \mathcal { D } } \left[ \mathbb { E } _ { \pmb { \theta } } [ \pmb { \theta } | \mathcal { D } ] \right]\tag{2.21}

$$

## 式22 (tag: 2.22)

$$

\mathbb { E } _ { \theta } [ \theta ] \equiv \int p ( \theta ) \theta \mathrm { d } \theta\tag{2.22}

$$

## 式23 (tag: 2.23)

$$

\mathbb { E } _ { \mathcal { D } } [ \mathbb { E } _ { \boldsymbol { \theta } } [ \boldsymbol { \theta } | \mathcal { D } ] ] \equiv \int \left\{ \int \theta p ( \boldsymbol { \theta } | \mathcal { D } ) \mathrm { d } \boldsymbol { \theta } \right\} p ( \mathcal { D } ) \mathrm { d } \mathcal { D }\tag{2.23}

$$

## 式24 (tag: 2.24)

$$

\begin{array} { r } { \operatorname { v a r } _ { \theta } [ \theta ] = \mathbb { E } _ { \mathcal { D } } \left[ \operatorname { v a r } _ { \theta } [ \theta | \mathcal { D } ] \right] + \operatorname { v a r } _ { \mathcal { D } } \left[ \mathbb { E } _ { \theta } [ \theta | \mathcal { D } ] \right] . } \end{array}\tag{2.24}

$$

## 式25 (tag: 2.25)

$$

\mathbf { x } = ( 0 , 0 , 1 , 0 , 0 , 0 ) ^ { \mathrm { T } }\tag{2.25}

$$

## 式26 (tag: 2.26)

$$

p ( \mathbf { x } | \mu ) = \prod _ { k = 1 } ^ { K } \mu _ { k } ^ { x _ { k } }\tag{2.26}

$$

## 式27 (tag: 2.27)

$$

\sum _ { \mathbf { x } } p ( \mathbf { x } | \mu ) = \sum _ { k = 1 } ^ { K } \mu _ { k } = 1\tag{2.27}

$$

## 式28 (tag: 2.28)

$$

\mathbb { E } [ \mathbf { x } | \mu ] = \sum _ { \mathbf { x } } p ( \mathbf { x } | \mu ) \mathbf { x } = ( \mu _ { 1 } , \dots , \mu _ { K } ) ^ { \mathrm { T } } = \mu\tag{2.28}

$$

## 式29 (tag: 2.29)

$$

p ( \mathcal { D } | \boldsymbol { \mu } ) = \prod _ { n = 1 } ^ { N } \prod _ { k = 1 } ^ { K } \mu _ { k } ^ { x _ { n k } } = \prod _ { k = 1 } ^ { K } \mu _ { k } ^ { \left( \sum _ { n } x _ { n k } \right) } = \prod _ { k = 1 } ^ { K } \mu _ { k } ^ { m _ { k } }\tag{2.29}

$$

## 式30 (tag: 2.30)

$$

m _ { k } = \sum _ { n } x _ { n k } .\tag{2.30}

$$

## 式31 (tag: 2.31)

$$

\sum _ { k = 1 } ^ { K } m _ { k } \ln \mu _ { k } + \lambda \left( \sum _ { k = 1 } ^ { K } \mu _ { k } - 1 \right)\tag{2.31}

$$

## 式32 (tag: 2.32)

$$

\mu _ { k } = - m _ { k } / \lambda\tag{2.32}

$$

## 式33 (tag: 2.33)

$$

\mu _ { k } ^ { \mathrm { M L } } = \frac { m _ { k } } { N }\tag{2.33}

$$

## 式34 (tag: 2.34)

$$

\mathrm { M u l t } ( m _ { 1 } , m _ { 2 } , . . . , m _ { K } | \pmb { \mu } , N ) = \binom { N } { m _ { 1 } m _ { 2 } . . . m _ { K } } \prod _ { k = 1 } ^ { K } \mu _ { k } ^ { m _ { k } }\tag{2.34}

$$

## 式35 (tag: 2.35)

$$

{ \binom { N } { m _ { 1 } m _ { 2 } \ldots . . m _ { K } } } = { \frac { N ! } { m _ { 1 } ! m _ { 2 } ! \ldots . m _ { K } ! } }\tag{2.35}

$$

## 式36 (tag: 2.36)

$$

\sum _ { k = 1 } ^ { K } m _ { k } = N .\tag{2.36}

$$

## 式37 (tag: 2.37)

$$

p ( \mu | \alpha ) \propto \prod _ { k = 1 } ^ { K } \mu _ { k } ^ { \alpha _ { k } - 1 }\tag{2.37}

$$

## 式38 (tag: 2.38)

$$

\operatorname { D i r } ( \mu | \alpha ) = { \frac { \Gamma ( \alpha _ { 0 } ) } { \Gamma ( \alpha _ { 1 } ) \cdots \Gamma ( \alpha _ { K } ) } } \prod _ { k = 1 } ^ { K } \mu _ { k } ^ { \alpha _ { k } - 1 }\tag{2.38}

$$

## 式39 (tag: 2.39)

$$

\alpha _ { 0 } = \sum _ { k = 1 } ^ { K } \alpha _ { k }\tag{2.39}

$$

## 式40 (tag: 2.40)

$$

p ( \pmb { \mu } | \mathcal { D } , \pmb { \alpha } ) \propto p ( \mathcal { D } | \pmb { \mu } ) p ( \pmb { \mu } | \pmb { \alpha } ) \propto \prod _ { k = 1 } ^ { K } \mu _ { k } ^ { \alpha _ { k } + m _ { k } - 1 }\tag{2.40}

$$

## 式41 (tag: 2.41)

$$

\begin{array} { l } { { \displaystyle p ( { \boldsymbol { \mu } } | \mathcal { D } , { \boldsymbol { \alpha } } ) = \mathrm { D i r } ( { \boldsymbol { \mu } } | { \boldsymbol { \alpha } } + \mathbf { m } ) } \ ~ } \\ { { \displaystyle ~ = \frac { \Gamma ( \alpha _ { 0 } + N ) } { \Gamma ( \alpha _ { 1 } + m _ { 1 } ) \cdots \Gamma ( \alpha _ { K } + m _ { K } ) } \prod _ { k = 1 } ^ { K } \mu _ { k } ^ { \alpha _ { k } + m _ { k } - 1 } } } \end{array}\tag{2.41}

$$

## 式42 (tag: 2.42)

$$

\mathcal { N } ( x | \mu , \sigma ^ { 2 } ) = \frac { 1 } { \left( 2 \pi \sigma ^ { 2 } \right) ^ { 1 / 2 } } \exp \left\{ - \frac { 1 } { 2 \sigma ^ { 2 } } ( x - \mu ) ^ { 2 } \right\}\tag{2.42}

$$

## 式43 (tag: 2.43)

$$

{ \mathcal { N } } ( \mathbf { x } | { \boldsymbol { \mu } } , { \boldsymbol { \Sigma } } ) = { \frac { 1 } { ( 2 \pi ) ^ { D / 2 } } } { \frac { 1 } { | { \boldsymbol { \Sigma } } | ^ { 1 / 2 } } } \exp \left\{ - { \frac { 1 } { 2 } } ( \mathbf { x } - { \boldsymbol { \mu } } ) ^ { \mathrm { { T } } } { \boldsymbol { \Sigma } } ^ { - 1 } ( \mathbf { x } - { \boldsymbol { \mu } } ) \right\}\tag{2.43}

$$

## 式44 (tag: 2.44)

$$

\Delta ^ { 2 } = ( { \bf x } - { \boldsymbol \mu } ) ^ { \mathrm { T } } \Sigma ^ { - 1 } ( { \bf x } - { \boldsymbol \mu } )\tag{2.44}

$$

## 式45 (tag: 2.45)

$$

\begin{array} { r } { \Sigma { \mathbf { u } } _ { i } = \lambda _ { i } \mathbf { u } _ { i } . } \end{array}\tag{2.45}

$$

## 式46 (tag: 2.46)

$$

\begin{array} { r } { { \bf u } _ { i } ^ { \mathrm { T } } { \bf u } _ { j } = I _ { i j } . } \end{array}\tag{2.46}

$$

## 式47 (tag: 2.47)

$$

I _ { i j } = \left\{ \begin{array} { l l } { 1 , } & { i = j \mathrm { ~ } \boldsymbol { \sigma } ) \boldsymbol { \xi } \stackrel { \ast } { \mathrm { ~ } } } \\ { 0 , } & { \boldsymbol { \Xi } \hslash \mathcal { D } \boldsymbol { \perp } \boldsymbol { \mathcal { N } } \mathrm { ~ } } \end{array} \right.\tag{2.47}

$$

## 式48 (tag: 2.48)

$$

\boldsymbol \Sigma = \sum _ { i = 1 } ^ { D } \lambda _ { i } \mathbf { u } _ { i } \mathbf { u } _ { i } ^ { \mathrm { T } }\tag{2.48}

$$

## 式49 (tag: 2.49)

$$

\boldsymbol { \Sigma } ^ { - 1 } = \sum _ { i = 1 } ^ { D } \frac { 1 } { \lambda _ { i } } \mathbf { u } _ { i } \mathbf { u } _ { i } ^ { \mathrm { T } }\tag{2.49}

$$

## 式50 (tag: 2.50)

$$

\Delta ^ { 2 } = \sum _ { i = 1 } ^ { D } \frac { y _ { i } ^ { 2 } } { \lambda _ { i } }\tag{2.50}

$$

## 式51 (tag: 2.51)

$$

y _ { i } = \mathbf { u } _ { i } ^ { \mathrm { T } } ( \mathbf { x } - \mu ) .\tag{2.51}

$$

## 式52 (tag: 2.52)

$$

\mathbf { y } = \mathbf { U } ( \mathbf { x } - \boldsymbol { \mu } )\tag{2.52}

$$

## 式53 (tag: 2.53)

$$

J _ { i j } = { \frac { \partial x _ { i } } { \partial y _ { j } } } = U _ { j i }\tag{2.53}

$$

## 式54 (tag: 2.54)

$$

\mathbf { \left| J \right| ^ { 2 } } = \left| \mathbf { U ^ { \mathrm { T } } } \right| ^ { 2 } = \left| \mathbf { U ^ { \mathrm { T } } } \right| \left| \mathbf { U } \right| = \left| \mathbf { U ^ { \mathrm { T } } } \mathbf { U } \right| = \left| \mathbf { I } \right| = 1\tag{2.54}

$$

## 式55 (tag: 2.55)

$$

| \Sigma | ^ { 1 / 2 } = \prod _ { j = 1 } ^ { D } \lambda _ { j } ^ { 1 / 2 }\tag{2.55}

$$

## 式56 (tag: 2.56)

$$

p ( \mathbf { y } ) = p ( \mathbf { x } ) | \mathbf { J } | = \prod _ { j = 1 } ^ { D } \frac { 1 } { ( 2 \pi \lambda _ { j } ) ^ { 1 / 2 } } \exp \left\{ - \frac { y _ { j } ^ { 2 } } { 2 \lambda _ { j } } \right\}\tag{2.56}

$$

## 式57 (tag: 2.57)

$$

\int p ( \mathbf { y } ) \mathrm { d } \mathbf { y } = \prod _ { j = 1 } ^ { D } \int _ { - \infty } ^ { \infty } { \frac { 1 } { ( 2 \pi \lambda _ { j } ) ^ { 1 / 2 } } } \exp \left\{ - { \frac { y _ { j } ^ { 2 } } { 2 \lambda _ { j } } } \right\} \mathrm { d } y _ { j } = 1\tag{2.57}

$$

## 式58 (tag: 2.58)

$$

{ \begin{array} { r l } & { \mathbb { E } [ { \mathbf { x } } ] = { \frac { 1 } { ( 2 \pi ) ^ { D / 2 } } } { \frac { 1 } { | { \boldsymbol { \Sigma } } | ^ { 1 / 2 } } } \int \exp \left\{ - { \frac { 1 } { 2 } } ( { \mathbf { x } } - { \boldsymbol { \mu } } ) ^ { \mathrm { { T } } } { \boldsymbol { \Sigma } } ^ { - 1 } ( { \mathbf { x } } - { \boldsymbol { \mu } } ) \right\} { \mathbf { x } } \mathrm { d } { \mathbf { x } } } \\ & { \quad = { \frac { 1 } { ( 2 \pi ) ^ { D / 2 } } } { \frac { 1 } { | { \boldsymbol { \Sigma } } | ^ { 1 / 2 } } } \int \exp \left\{ - { \frac { 1 } { 2 } } { \mathbf { z } } ^ { \mathrm { { T } } } { \boldsymbol { \Sigma } } ^ { - 1 } { \mathbf { z } } \right\} ( { \mathbf { z } } + { \boldsymbol { \mu } } ) \mathrm { d } { \mathbf { z } } } \end{array} }\tag{2.58}

$$

## 式59 (tag: 2.59)

$$

\mathbb { E } [ \mathbf { x } ] = \mu\tag{2.59}

$$

## 式60 (tag: 2.60)

$$

\mathbf { z } = \sum _ { j = 1 } ^ { D } y _ { j } \mathbf { u } _ { j }\tag{2.60}

$$

## 式61 (tag: 2.61)

$$

{ \begin{array} { r l } { \displaystyle \frac { 1 } { ( 2 \pi ) ^ { D / 2 } } \frac { 1 } { | \mathbf { \boldsymbol { \Sigma } } | ^ { 1 / 2 } } \int \exp \left\{ - \frac { 1 } { 2 } \mathbf { \boldsymbol { \Sigma } } ^ { \mathrm { { T } } } \mathbf { \boldsymbol { \Sigma } } ^ { - 1 } \mathbf { z } \right\} \mathbf { z } \mathbf { z } ^ { \mathrm { T } } \mathrm { ~ d } \mathbf { z } } \\ { = } & { \displaystyle \frac { 1 } { ( 2 \pi ) ^ { D / 2 } } \frac { 1 } { | \mathbf { \boldsymbol { \Sigma } } | ^ { 1 / 2 } } \sum _ { i = 1 } ^ { D } \sum _ { j = 1 } ^ { D } \mathbf { u } _ { i } \mathbf { u } _ { j } ^ { \mathrm { T } } \int \exp \left\{ - \sum _ { k = 1 } ^ { D } \frac { y _ { k } ^ { 2 } } { 2 \lambda _ { k } } \right\} y _ { i } y _ { j } \mathrm { ~ d } \mathbf { y } } \\ { = } & { \displaystyle \sum _ { i = 1 } ^ { D } \mathbf { u } _ { i } \mathbf { u } _ { i } ^ { \mathrm { { T } } } \lambda _ { i } = \Sigma } \end{array} }\tag{2.61}

$$

## 式62 (tag: 2.62)

$$

\mathbb { E } [ { \bf x } { \bf x } ^ { \mathrm { T } } ] = \mu \mu ^ { \mathrm { T } } + \Sigma\tag{2.62}

$$

## 式63 (tag: 2.63)

$$

\operatorname { c o v } [ \mathbf { x } ] = \mathbb { E } \left[ ( \mathbf { x } - \mathbb { E } [ \mathbf { x } ] ) ( \mathbf { x } - \mathbb { E } [ \mathbf { x } ] ) ^ { \mathrm { T } } \right] .\tag{2.63}

$$

## 式64 (tag: 2.64)

$$

\operatorname { c o v } [ \mathbf { x } ] = \Sigma\tag{2.64}

$$

## 式65 (tag: 2.65)

$$

\begin{array} { r } { \mathbf { x } = \left( \begin{array} { l } { \mathbf { x } _ { a } } \\ { \mathbf { x } _ { b } } \end{array} \right) . } \end{array}\tag{2.65}

$$

## 式66 (tag: 2.66)

$$

\begin{array} { r } { \boldsymbol { \mu } = \left( \begin{array} { l } { \mu _ { a } } \\ { \mu _ { b } } \end{array} \right) . } \end{array}\tag{2.66}

$$

## 式67 (tag: 2.67)

$$

\Sigma = \left( \begin{array} { l l } { { \Sigma _ { a a } } } & { { \Sigma _ { a b } } } \\ { { \Sigma _ { b a } } } & { { \Sigma _ { b b } } } \end{array} \right) .\tag{2.67}

$$

## 式68 (tag: 2.68)

$$

\begin{array} { r } { \pmb { \Lambda } \equiv \pmb { \Sigma } ^ { - 1 } . } \end{array}\tag{2.68}

$$

## 式69 (tag: 2.69)

$$

\Lambda = \left( \begin{array} { l l } { { \Lambda _ { a a } } } & { { \Lambda _ { a b } } } \\ { { \Lambda _ { b a } } } & { { \Lambda _ { b b } } } \end{array} \right) .\tag{2.69}

$$

## 式70 (tag: 2.70)

$$

\begin{array} { l } { { \displaystyle - \frac 1 2 ( { \bf x } - { \boldsymbol { \mu } } ) ^ { \mathrm { T } } { \boldsymbol { \Sigma } } ^ { - 1 } ( { \bf x } - { \boldsymbol { \mu } } ) = } \ } \\ { { \displaystyle ~ - \frac 1 2 ( { \bf x } _ { a } - { \boldsymbol { \mu } } _ { a } ) ^ { \mathrm { T } } \Lambda _ { a a } ( { \bf x } _ { a } - { \boldsymbol { \mu } } _ { a } ) - \frac 1 2 ( { \bf x } _ { a } - { \boldsymbol { \mu } } _ { a } ) ^ { \mathrm { T } } \Lambda _ { a b } ( { \bf x } _ { b } - { \boldsymbol { \mu } } _ { b } ) } } \\ { { \displaystyle ~ - \frac 1 2 ( { \bf x } _ { b } - { \boldsymbol { \mu } } _ { b } ) ^ { \mathrm { T } } \Lambda _ { b a } ( { \bf x } _ { a } - { \boldsymbol { \mu } } _ { a } ) - \frac 1 2 ( { \bf x } _ { b } - { \boldsymbol { \mu } } _ { b } ) ^ { \mathrm { T } } \Lambda _ { b b } ( { \bf x } _ { b } - { \boldsymbol { \mu } } _ { b } ) } } \end{array}\tag{2.70}

$$

## 式71 (tag: 2.71)

$$

- { \frac { 1 } { 2 } } ( \mathbf { x } - { \boldsymbol { \mu } } ) ^ { \mathrm { { T } } } { \boldsymbol { \Sigma } } ^ { - 1 } ( \mathbf { x } - { \boldsymbol { \mu } } ) = - { \frac { 1 } { 2 } } \mathbf { x } ^ { \mathrm { { T } } } { \boldsymbol { \Sigma } } ^ { - 1 } \mathbf { x } + \mathbf { x } ^ { \mathrm { { T } } } { \boldsymbol { \Sigma } } ^ { - 1 } { \boldsymbol { \mu } } + { \mathrm { c o n s t . } }\tag{2.71}

$$

## 式72 (tag: 2.72)

$$

- \frac { 1 } { 2 } \mathbf { x } _ { a } ^ { \mathrm { { T } } } \mathbf { \Lambda } \mathbf { 1 } _ { a a } \mathbf { x } _ { a }\tag{2.72}

$$

## 式73 (tag: 2.73)

$$

\Sigma _ { a | b } = \Lambda _ { a a } ^ { - 1 }\tag{2.73}

$$

## 式74 (tag: 2.74)

$$

{ \bf x } _ { a } ^ { \mathrm { T } } \left\{ \pmb { \Lambda } _ { a a } \pmb { \mu } _ { a } - \pmb { \Lambda } _ { a b } \left( \mathbf { x } _ { b } - \pmb { \mu } _ { b } \right) \right\}\tag{2.74}

$$

## 式75 (tag: 2.75)

$$

\begin{array} { c } { { \pmb { \mu } _ { a | b } = \pmb { \Sigma } _ { a | b } \left\{ \pmb { \Lambda } _ { a a } \pmb { \mu } _ { a } - \pmb { \Lambda } _ { a b } ( \mathbf { x } _ { b } - \pmb { \mu } _ { b } ) \right\} } } \\ { { = \pmb { \mu } _ { a } - \pmb { \Lambda } _ { a a } ^ { - 1 } \pmb { \Lambda } _ { a b } ( \mathbf { x } _ { b } - \pmb { \mu } _ { b } ) } } \end{array}\tag{2.75}

$$

## 式76 (tag: 2.76)

$$

\left( \mathbf { A } \quad \mathbf { B } \right) ^ { - 1 } = \left( \begin{array} { c c } { \mathbf { M } } & { - \mathbf { M } \mathbf { B } \mathbf { D } ^ { - 1 } } \\ { - \mathbf { D } ^ { - 1 } \mathbf { C } \mathbf { M } } & { \mathbf { D } ^ { - 1 } + \mathbf { D } ^ { - 1 } \mathbf { C } \mathbf { M } \mathbf { B } \mathbf { D } ^ { - 1 } } \end{array} \right) .\tag{2.76}

$$

## 式77 (tag: 2.77)

$$

\mathbf { M } = ( \mathbf { A } - \mathbf { B } \mathbf { D } ^ { - 1 } \mathbf { C } ) ^ { - 1 } .\tag{2.77}

$$

## 式78 (tag: 2.78)

$$

\left( \begin{array} { c c } { { \sum _ { a a } } } & { { \sum _ { a b } } } \\ { { \sum _ { b a } } } & { { \sum _ { b b } } } \end{array} \right) ^ { - 1 } = \left( \begin{array} { c c } { { \Lambda _ { a a } } } & { { \Lambda _ { a b } } } \\ { { \Lambda _ { b a } } } & { { \Lambda _ { b b } } } \end{array} \right)\tag{2.78}

$$

## 式79 (tag: 2.79)

$$

\mathbf { \Lambda } _ { a a } = ( \Sigma _ { a a } - \Sigma _ { a b } \Sigma _ { b b } ^ { - 1 } \Sigma _ { b a } ) ^ { - 1 }\tag{2.79}

$$

## 式80 (tag: 2.80)

$$

\begin{array} { r } { \mathbf { \Lambda } _ { a b } = - ( \Sigma _ { a a } - \Sigma _ { a b } \Sigma _ { b b } ^ { - 1 } \Sigma _ { b a } ) ^ { - 1 } \Sigma _ { a b } \Sigma _ { b b } ^ { - 1 } } \end{array}\tag{2.80}

$$

## 式81 (tag: 2.81)

$$

\pmb { \mu } _ { a | b } = \pmb { \mu } _ { a } + \pmb { \Sigma } _ { a b } \pmb { \Sigma } _ { b b } ^ { - 1 } ( \mathbf { x } _ { b } - \pmb { \mu } _ { b } )\tag{2.81}

$$

## 式82 (tag: 2.82)

$$

\begin{array} { r } { \Sigma _ { a | b } = \Sigma _ { a a } - \Sigma _ { a b } \Sigma _ { b b } ^ { - 1 } \Sigma _ { b a } } \end{array}\tag{2.82}

$$

## 式83 (tag: 2.83)

$$

p ( \mathbf { x } _ { a } ) = \int p ( \mathbf { x } _ { a } , \mathbf { x } _ { b } ) \mathrm { d } \mathbf { x } _ { b }\tag{2.83}

$$

## 式84 (tag: 2.84)

$$

- \frac 1 2 \mathbf { x } _ { b } ^ { \mathrm { T } } \mathbf { A } _ { b b } \mathbf { x } _ { b } + \mathbf { x } _ { b } ^ { \mathrm { T } } \mathbf { m } = - \frac 1 2 ( \mathbf { x } _ { b } - \mathbf { A } _ { b b } ^ { - 1 } \mathbf { m } ) ^ { \mathrm { T } } \mathbf { A } _ { b b } ( \mathbf { x } _ { b } - \mathbf { A } _ { b b } ^ { - 1 } \mathbf { m } ) + \frac 1 2 \mathbf { m } ^ { \mathrm { T } } \mathbf { A } _ { b b } ^ { - 1 } \mathbf { m }\tag{2.84}

$$

## 式85 (tag: 2.85)

$$

\mathbf { m } = \Lambda _ { b b } \pmb { \mu } _ { b } - \pmb { \Lambda } _ { b a } ( \mathbf { x } _ { a } - \pmb { \mu } _ { a } )\tag{2.85}

$$

## 式86 (tag: 2.86)

$$

\int \exp \left\{ - \frac { 1 } { 2 } ( \mathbf { x } _ { b } - \mathbf { A } _ { b b } ^ { - 1 } \mathbf { m } ) ^ { \mathrm { T } } \mathbf { A } _ { b b } ( \mathbf { x } _ { b } - \mathbf { A } _ { b b } ^ { - 1 } \mathbf { m } ) \right\} \mathrm { d } \mathbf { x } _ { b } .\tag{2.86}

$$

## 式87 (tag: 2.87)

$$

\begin{array} { r l } {  { \frac { 1 } { 2 } [ \Lambda _ { b b } \mu _ { b } - \Lambda _ { b a } ( \mathbf { x } _ { a } - \mu _ { a } ) ] ^ { \mathrm { T } } \mathbf { \Lambda } _ { b b } ^ { - 1 } [ \Lambda _ { b b } \mu _ { b } - \Lambda _ { b a } ( \mathbf { x } _ { a } - \mu _ { a } ) ] } } \\ & { ~ - \frac { 1 } { 2 } \mathbf { x } _ { a } ^ { \mathrm { T } } \mathbf { \Lambda } _ { a a } \mathbf { x } _ { a } + \mathbf { x } _ { a } ^ { \mathrm { T } } ( \mathbf { \Lambda } _ { a a } \mu _ { a } + \Lambda _ { a b } \mu _ { b } ) + \mathrm { c o n s t } } \\ & { = ~ - \frac { 1 } { 2 } \mathbf { x } _ { a } ^ { \mathrm { T } } ( \mathbf { \Lambda } _ { a a } - \Lambda _ { a b } \mathbf { \Lambda } _ { b b } ^ { - 1 } \mathbf { \Lambda } _ { b a } ) \mathbf { x } _ { a } } \\ & { + \mathbf { x } _ { a } ^ { \mathrm { T } } ( \mathbf { \Lambda } _ { a a } - \mathbf { \Lambda } _ { a b } \mathbf { \Lambda } _ { b b } ^ { - 1 } \mathbf { \Lambda } _ { b a } ) \mu _ { a } + \mathrm { c o n s t } } \end{array}\tag{2.87}

$$

## 式88 (tag: 2.88)

$$

\pmb { \Sigma } _ { a } = ( \pmb { \Lambda } _ { a a } - \pmb { \Lambda } _ { a b } \pmb { \Lambda } _ { b b } ^ { - 1 } \pmb { \Lambda } _ { b a } ) ^ { - 1 }\tag{2.88}

$$

## 式89 (tag: 2.89)

$$

\Sigma _ { a } ( \Lambda _ { a a } - \Lambda _ { a b } \Lambda _ { b b } ^ { - 1 } \Lambda _ { b a } ) \pmb { \mu } _ { a } = \pmb { \mu } _ { a }\tag{2.89}

$$

## 式90 (tag: 2.90)

$$

\left( \Lambda _ { a a } \Lambda _ { a b } \right) ^ { - 1 } = \left( \begin{array} { l l } { { { \Sigma } _ { a a } } } & { { { \Sigma } _ { a b } } } \\ { { { \Sigma } _ { b a } } } & { { { \Lambda } _ { b b } } } \end{array} \right) ^ { - 1 } = \left( \begin{array} { l l } { { { \Sigma } _ { a a } } } & { { { \Sigma } _ { a b } } } \\ { { { \Sigma } _ { b a } } } & { { { \Sigma } _ { b b } } } \end{array} \right) .\tag{2.90}

$$

## 式91 (tag: 2.91)

$$

\left( \pmb { \Lambda } _ { a a } - \pmb { \Lambda } _ { a b } \pmb { \Lambda } _ { b b } ^ { - 1 } \pmb { \Lambda } _ { b a } \right) ^ { - 1 } = \pmb { \Sigma } _ { a a }\tag{2.91}

$$

## 式92 (tag: 2.92)

$$

\mathbb { E } [ { \bf x } _ { a } ] ~ = ~ \mu _ { a }\tag{2.92}

$$

## 式93 (tag: 2.93)

$$

\mathrm { c o v } [ { \bf x } _ { a } ] = \Sigma _ { a a }\tag{2.93}

$$

## 式94 (tag: 2.94)

$$

\mathbf { x } = { \binom { \mathbf { x } _ { a } } { \mathbf { x } _ { b } } } , \quad \mu = { \binom { \mu _ { a } } { \mu _ { b } } }\tag{2.94}

$$

## 式95 (tag: 2.95)

$$

\Sigma = \left( \begin{array} { l l } { \Sigma _ { a a } } & { \Sigma _ { a b } } \\ { \Sigma _ { b a } } & { \Sigma _ { b b } } \end{array} \right) , \quad \Lambda = \left( \begin{array} { l l } { \Lambda _ { a a } } & { \Lambda _ { a b } } \\ { \Lambda _ { b a } } & { \Lambda _ { b b } } \end{array} \right)\tag{2.95}

$$

## 式96 (tag: 2.96)

$$

p ( \mathbf { x } _ { a } | \mathbf { x } _ { b } ) = \mathcal { N } ( \mathbf { x } _ { a } | \boldsymbol { \mu } _ { a | b } , \boldsymbol { \Lambda } _ { a a } ^ { - 1 } )\tag{2.96}

$$

## 式97 (tag: 2.97)

$$

\mu _ { a | b } = \mu _ { a } - \Lambda _ { a a } ^ { - 1 } \Lambda _ { a b } ( { \bf x } _ { b } - \mu _ { b } )\tag{2.97}

$$

## 式98 (tag: 2.98)

$$

p ( \mathbf { x } _ { a } ) = \mathcal { N } ( \mathbf { x } _ { a } | \boldsymbol { \mu } _ { a } , \boldsymbol { \Sigma } _ { a a } )\tag{2.98}

$$

## 式99 (tag: 2.99)

$$

p ( \mathbf { x } ) = \mathcal { N } \left( \mathbf { x } | \boldsymbol { \mu } , \boldsymbol { \Lambda } ^ { - 1 } \right)\tag{2.99}

$$

## 式100 (tag: 2.100)

$$

p ( \mathbf { y } \vert \mathbf { x } ) = \mathcal { N } \left( \mathbf { y } \vert \mathbf { A } \mathbf { x } + \mathbf { b } , \mathbf { L } ^ { - 1 } \right)\tag{2.100}

$$

## 式101 (tag: 2.101)

$$

\mathbf { z } = { \binom { \mathbf { x } } { \mathbf { y } } } \cdot\tag{2.101}

$$

## 式102 (tag: 2.102)

$$

\begin{array} { l } { { \displaystyle \ln p ( { \bf z } ) = \ln p ( { \bf x } ) + \ln p ( { \bf y } \vert { \bf x } ) } \ ~ } \\ { { \displaystyle ~ = - \frac { 1 } { 2 } ( { \bf x } - { \boldsymbol \mu } ) ^ { \mathrm { T } } { \pmb \Lambda } ( { \bf x } - { \boldsymbol \mu } ) } \ ~ } \\ { { \displaystyle ~ - \frac { 1 } { 2 } ( { \bf y } - { \bf A } { \bf x } - { \bf b } ) ^ { \mathrm { T } } { \bf L } ( { \bf y } - { \bf A } { \bf x } - { \bf b } ) + \mathrm { c o n s t } } } \end{array}\tag{2.102}

$$

## 式103 (tag: 2.103)

$$

\begin{array} { r l r } {  { - \frac { 1 } { 2 } \mathbf { x } ^ { \mathrm { T } } ( \mathbf { A } + \mathbf { A } ^ { \mathrm { T } } \mathbf { L } \mathbf { A } ) \mathbf { x } - \frac { 1 } { 2 } \mathbf { y } ^ { \mathrm { T } } \mathbf { L } \mathbf { y } + \frac { 1 } { 2 } \mathbf { y } ^ { \mathrm { T } } \mathbf { L } \mathbf { A } \mathbf { x } + \frac { 1 } { 2 } \mathbf { x } ^ { \mathrm { T } } \mathbf { A } ^ { \mathrm { T } } \mathbf { L } \mathbf { y } } } \\ & { = } & { - \frac { 1 } { 2 } ( \begin{array} { c } { \mathbf { x } } \\ { \mathbf { y } } \end{array} ) ^ { \mathrm { T } } ( \begin{array} { c c } { \mathbf { A } + \mathbf { A } ^ { \mathrm { T } } \mathbf { L } \mathbf { A } } & { - \mathbf { A } ^ { \mathrm { T } } \mathbf { L } } \\ { - \mathbf { L } \mathbf { A } } & { \mathbf { L } } \end{array} ) ( \begin{array} { c } { \mathbf { x } } \\ { \mathbf { y } } \end{array} ) = - \frac { 1 } { 2 } \mathbf { z } ^ { \mathrm { T } } \mathbf { R } \mathbf { z } . } \end{array}\tag{2.103}

$$

## 式104 (tag: 2.104)

$$

\mathbf { R } = \left( \begin{array} { c c } { \mathbf { \Lambda } \mathbf { 1 } + \mathbf { A } ^ { \mathrm { T } } \mathbf { L } \mathbf { A } } & { - \mathbf { A } ^ { \mathrm { T } } \mathbf { L } } \\ { - \mathbf { L } \mathbf { A } } & { \mathbf { L } } \end{array} \right)\tag{2.104}

$$

## 式105 (tag: 2.105)

$$

\mathrm { c o v } [ \mathbf { z } ] = \mathbf { R } ^ { - 1 } = \left( \begin{array} { c c } { \mathbf { \mathbf { \boldsymbol { \Lambda } } \mathbf { \boldsymbol { \Lambda } } ^ { - 1 } } } & { \mathbf { \boldsymbol { \Lambda } } ^ { - 1 } \mathbf { \boldsymbol { \mathbf { A } } } ^ { \mathrm { T } } } \\ { \mathbf { \boldsymbol { \mathbf { A } } } \mathbf { \boldsymbol { \Lambda } } ^ { - 1 } } & { \mathbf { \boldsymbol { \mathbf { L } } } ^ { - 1 } + \mathbf { \boldsymbol { \mathbf { A } } } \mathbf { \boldsymbol { \Lambda } } ^ { - 1 } \mathbf { \boldsymbol { \mathbf { A } } } ^ { \mathrm { T } } } \end{array} \right) .\tag{2.105}

$$

## 式106 (tag: 2.106)

$$

\mathbf { x } ^ { \mathrm { T } } \mathbf { A } \mu - \mathbf { x } ^ { \mathrm { T } } \mathbf { A } ^ { \mathrm { T } } \mathbf { L } \mathbf { b } + \mathbf { y } ^ { \mathrm { T } } \mathbf { L } \mathbf { b } = { \binom { \mathbf { x } } { \mathbf { y } } } ^ { \mathrm { T } } \left( { \begin{array} { c } { \mathbf { A } \mu - \mathbf { A } ^ { \mathrm { T } } \mathbf { L } \mathbf { b } } \\ { \mathbf { L } \mathbf { b } } \end{array} } \right)\tag{2.106}

$$

## 式107 (tag: 2.107)

$$

\mathbb { E } [ \mathbf { z } ] = \mathbf { R } ^ { - 1 } \left( \begin{array} { c } { { \mathbf { \Lambda } \mathbf { \Lambda } \mathbf { \Lambda } \mathbf { \Lambda } \mathbf { \Lambda } \mathbf { \Lambda } } } \\ { { \mathbf { \Lambda } \mathbf { \Lambda } \mathbf { L } \mathbf { b } } } \end{array} \right)\tag{2.107}

$$

## 式108 (tag: 2.108)

$$

\mathbb { E } [ \mathbf { z } ] = \binom { \mu } { \mathbf { A } \mu + \mathbf { b } }\tag{2.108}

$$

## 式109 (tag: 2.109)

$$

\mathbb { E } [ { \bf y } ] = { \bf A } \mu + { \bf b }\tag{2.109}

$$

## 式110 (tag: 2.110)

$$

\mathrm { c o v } [ \mathbf { y } ] = \mathbf { L } ^ { - 1 } + \mathbf { A } \mathbf { A } ^ { - 1 } \mathbf { A } ^ { \mathrm { T } }\tag{2.110}

$$

## 式111 (tag: 2.111)

$$

\mathbb { E } [ \mathbf { x } | \mathbf { y } ] = ( \mathbf { A } + \mathbf { A } ^ { \mathrm { T } } \mathbf { L A } ) ^ { - 1 } \left\{ \mathbf { A } ^ { \mathrm { T } } \mathbf { L } ( \mathbf { y } - \mathbf { b } ) + \mathbf { A } \mu \right\}\tag{2.111}

$$

## 式112 (tag: 2.112)

$$

\operatorname { c o v } [ \mathbf { x } | \mathbf { y } ] = ( \mathbf { \mathbf { \mathbf { \Lambda } } } \mathbf { \mathbf { \mathbf { \Lambda } } } \mathbf { \mathbf { \mathbf { \Lambda } } } \mathbf { \mathbf { \Lambda } } \mathbf { \mathbf { \Lambda } } \mathbf { \Lambda } ) ^ { - 1 }\tag{2.112}

$$

## 式113 (tag: 2.113)

$$

p ( { \bf x } ) = \mathcal { N } ( { \bf x } | \boldsymbol { \mu } , \Lambda ^ { - 1 } )\tag{2.113}

$$

## 式114 (tag: 2.114)

$$

p ( \mathbf { y } | \mathbf { x } ) = \mathcal { N } ( \mathbf { y } | \mathbf { A } \mathbf { x } + \mathbf { b } , \mathbf { L } ^ { - 1 } )\tag{2.114}

$$

## 式115 (tag: 2.115)

$$

p ( \mathbf { y } ) = { \mathcal { N } } ( \mathbf { y } | \mathbf { A } \mu + \mathbf { b } , \mathbf { L } ^ { - 1 } + \mathbf { A } \mathbf { A } ^ { - 1 } \mathbf { A } ^ { \mathrm { T } } )\tag{2.115}

$$

## 式116 (tag: 2.116)

$$

p ( \mathbf { x } | \mathbf { y } ) = { \mathcal { N } } ( \mathbf { x } | \Sigma \{ \mathbf { A } ^ { \mathrm { T } } \mathbf { L } ( \mathbf { y } - \mathbf { b } ) + \Delta \mu \} , \Sigma )\tag{2.116}

$$

## 式117 (tag: 2.117)

$$

\pmb { \Sigma } = ( \pmb { \Lambda } + \mathbf { A } ^ { \mathrm { T } } \mathbf { L } \mathbf { A } ) ^ { - 1 }\tag{2.117}

$$

## 式118 (tag: 2.118)

$$

\ln p ( { \bf X } | { \boldsymbol \mu } , { \boldsymbol \Sigma } ) = - { \frac { N D } { 2 } } \ln ( 2 \pi ) - { \frac { N } { 2 } } \ln | { \boldsymbol \Sigma } | - { \frac { 1 } { 2 } } \sum _ { n = 1 } ^ { N } ( { \bf x } _ { n } - { \boldsymbol \mu } ) ^ { \mathrm { { T } } } { \boldsymbol \Sigma } ^ { - 1 } ( { \bf x } _ { n } - { \boldsymbol \mu } )\tag{2.118}

$$

## 式119 (tag: 2.119)

$$

\sum _ { n = 1 } ^ { N } \mathbf { x } _ { n } , \qquad \sum _ { n = 1 } ^ { N } \mathbf { x } _ { n } \mathbf { x } _ { n } ^ { \mathrm { { T } } } .\tag{2.119}

$$

## 式120 (tag: 2.120)

$$

\frac { \partial } { \partial \pmb { \mu } } \ln p ( \mathbf { X } | \pmb { \mu } , \pmb { \Sigma } ) = \sum _ { n = 1 } ^ { N } \pmb { \Sigma } ^ { - 1 } ( \mathbf { x } _ { n } - \pmb { \mu } )\tag{2.120}

$$

## 式121 (tag: 2.121)

$$

\mu _ { \mathrm { M L } } = \frac { 1 } { N } \sum _ { n = 1 } ^ { N } \mathbf { x } _ { n } .\tag{2.121}

$$

## 式122 (tag: 2.122)

$$

\Sigma _ { \mathrm { M L } } = \frac { 1 } { N } \sum _ { n = 1 } ^ { N } ( \mathbf { x } _ { n } - \pmb { \mu } _ { \mathrm { M L } } ) ( \mathbf { x } _ { n } - \pmb { \mu } _ { \mathrm { M L } } ) ^ { \mathrm { T } } .\tag{2.122}

$$

## 式123 (tag: 2.123)

$$

\mathbb { E } [ \mu _ { \mathrm { M L } } ] = \mu\tag{2.123}

$$

## 式124 (tag: 2.124)

$$

\mathbb { E } [ \Sigma _ { \mathrm { M L } } ] = \frac { N - 1 } { N } \Sigma\tag{2.124}

$$

## 式125 (tag: 2.125)

$$

\widetilde \Sigma = \frac { 1 } { N - 1 } \sum _ { n = 1 } ^ { N } ( \mathbf { x } _ { n } - \pmb { \mu } _ { \mathrm { M L } } ) ( \mathbf { x } _ { n } - \pmb { \mu } _ { \mathrm { M L } } ) ^ { \mathrm { T } } .\tag{2.125}

$$

## 式126 (tag: 2.126)

$$

\begin{array} { l } { \displaystyle \mu _ { \mathrm { M L } } ^ { ( N ) } = \frac { 1 } { N } \sum _ { n = 1 } ^ { N } \mathbf { x } _ { n } } \\ { \displaystyle \quad = \frac { 1 } { N } \mathbf { x } _ { N } + \frac { 1 } { N } \sum _ { n = 1 } ^ { N - 1 } \mathbf { x } _ { n } } \\ { \displaystyle \quad = \frac { 1 } { N } \mathbf { x } _ { N } + \frac { N - 1 } { N } \mu _ { \mathrm { M L } } ^ { ( N - 1 ) } } \\ { \displaystyle \quad = \mu _ { \mathrm { M L } } ^ { ( N - 1 ) } + \frac { 1 } { N } ( \mathbf { x } _ { N } - \mu _ { \mathrm { M L } } ^ { ( N - 1 ) } ) } \end{array}\tag{2.126}

$$

## 式127 (tag: 2.127)

$$

f ( \theta ) \equiv \mathbb { E } [ z | \theta ] = \int z p ( z | \theta ) \mathrm { d } z .\tag{2.127}

$$

## 式128 (tag: 2.128)

$$

\mathbb { E } \left[ \left( z - f \right) ^ { 2 } \bigm | \theta \right] < \infty .\tag{2.128}

$$

## 式129 (tag: 2.129)

$$

\theta ^ { ( N ) } = \theta ^ { ( N - 1 ) } - a _ { N - 1 } z ( \theta ^ { ( N - 1 ) } ) .\tag{2.129}

$$

## 式130 (tag: 2.130)

$$

\operatorname* { l i m } _ { N  \infty } a _ { N } = 0\tag{2.130}

$$

## 式131 (tag: 2.131)

$$

\sum _ { N = 1 } ^ { \infty } a _ { N } = \infty\tag{2.131}

$$

## 式132 (tag: 2.132)

$$

\sum _ { N = 1 } ^ { \infty } a _ { N } ^ { 2 } < \infty\tag{2.132}

$$

## 式133 (tag: 2.133)

$$

- \frac { \partial } { \partial \theta } \left. \left\{ \frac { 1 } { N } \sum _ { n = 1 } ^ { N } \ln p ( x _ { n } | \theta ) \right\} \right| _ { \theta _ { \mathrm { M L } } } = 0\tag{2.133}

$$

## 式134 (tag: 2.134)

$$

- \operatorname* { l i m } _ { N \to \infty } \frac { 1 } { N } \sum _ { n = 1 } ^ { N } \frac { \partial } { \partial \theta } \ln p ( x _ { n } | \theta ) = \mathbb { E } _ { x } \left[ - \frac { \partial } { \partial \theta } \ln p ( x | \theta ) \right]\tag{2.134}

$$

## 式135 (tag: 2.135)

$$

\theta ^ { ( N ) } = \theta ^ { ( N - 1 ) } - a _ { N - 1 } { \frac { \partial } { \partial \theta ^ { ( N - 1 ) } } } \left[ - \ln p ( x _ { N } | \theta ^ { ( N - 1 ) } ) \right] .\tag{2.135}

$$

## 式136 (tag: 2.136)

$$

z = - \frac { \partial } { \partial \mu _ { \mathrm { M L } } } \ln p ( x | \mu _ { \mathrm { M L } } , \sigma ^ { 2 } ) = - \frac { 1 } { \sigma ^ { 2 } } ( x - \mu _ { \mathrm { M L } } )\tag{2.136}

$$

## 式137 (tag: 2.137)

$$

p ( \mathbf { x } | \mu ) = \prod _ { n = 1 } ^ { N } p ( x _ { n } | \mu ) = \frac { 1 } { ( 2 \pi \sigma ^ { 2 } ) ^ { N / 2 } } \exp \left. - \frac { 1 } { 2 \sigma ^ { 2 } } \sum _ { n = 1 } ^ { N } ( x _ { n } - \mu ) ^ { 2 } \right.\tag{2.137}

$$

## 式138 (tag: 2.138)

$$

p ( \mu ) = \mathcal { N } \left( \mu | \mu _ { 0 } , \sigma _ { 0 } ^ { 2 } \right) .\tag{2.138}

$$

## 式139 (tag: 2.139)

$$

p ( \mu | \mathbf { x } ) \propto p ( \mathbf { x } | \mu ) p ( \mu )\tag{2.139}

$$

## 式140 (tag: 2.140)

$$

p ( \mu | \mathbf { x } ) = \mathcal { N } \left( \mu | \mu _ { N } , \sigma _ { N } ^ { 2 } \right) .\tag{2.140}

$$

## 式141 (tag: 2.141)

$$

\mu _ { N } = \frac { \sigma ^ { 2 } } { N \sigma _ { 0 } ^ { 2 } + \sigma ^ { 2 } } \mu _ { 0 } + \frac { N \sigma _ { 0 } ^ { 2 } } { N \sigma _ { 0 } ^ { 2 } + \sigma ^ { 2 } } \mu _ { \mathrm { M L } }\tag{2.141}

$$

## 式142 (tag: 2.142)

$$

\frac { 1 } { \sigma _ { N } ^ { 2 } } = \frac { 1 } { \sigma _ { 0 } ^ { 2 } } + \frac { N } { \sigma ^ { 2 } }\tag{2.142}

$$

## 式143 (tag: 2.143)

$$

\mu _ { \mathrm { M L } } = \frac { 1 } { N } \sum ^ { N } x _ { n }\tag{2.143}

$$

## 式144 (tag: 2.144)

$$

p ( \mu | \pmb { x } ) \propto \left[ p ( \mu ) \prod _ { n = 1 } ^ { N - 1 } p ( x _ { n } | \mu ) \right] p ( x _ { N } | \mu ) .\tag{2.144}

$$

## 式145 (tag: 2.145)

$$

p ( { \pmb x } | \lambda ) = \prod _ { n = 1 } ^ { N } { \mathcal N } ( x _ { n } | \mu , \lambda ^ { - 1 } ) \propto \lambda ^ { N / 2 } \exp \left\{ - \frac { \lambda } { 2 } \sum _ { n = 1 } ^ { N } ( x _ { n } - \mu ) ^ { 2 } \right\} .\tag{2.145}

$$

## 式146 (tag: 2.146)

$$

\mathrm { G a m } ( \lambda | a , b ) = \frac { 1 } { \Gamma ( a ) } b ^ { a } \lambda ^ { a - 1 } \exp ( - b \lambda ) .\tag{2.146}

$$

## 式147 (tag: 2.147)

$$

\mathbb { E } [ \lambda ] = { \frac { a } { b } }\tag{2.147}

$$

## 式148 (tag: 2.148)

$$

\operatorname { v a r } [ \lambda ] = { \frac { a } { b ^ { 2 } } }\tag{2.148}

$$

## 式149 (tag: 2.149)

$$

p ( \lambda | \mathbf { x } ) \propto \lambda ^ { a _ { 0 } - 1 } \lambda ^ { N / 2 } \exp \left\{ - b _ { 0 } \lambda - { \frac { \lambda } { 2 } } \sum _ { n = 1 } ^ { N } ( x _ { n } - \mu ) ^ { 2 } \right\}\tag{2.149}

$$

## 式150 (tag: 2.150)

$$

a _ { N } = a _ { 0 } + { \frac { N } { 2 } }\tag{2.150}

$$

## 式151 (tag: 2.151)

$$

b _ { N } = b _ { 0 } + { \frac { 1 } { 2 } } \sum _ { n = 1 } ^ { N } ( x _ { n } - \mu ) ^ { 2 } = b _ { 0 } + { \frac { N } { 2 } } \sigma _ { \mathrm { M L } } ^ { 2 }\tag{2.151}

$$

## 式152 (tag: 2.152)

$$

\begin{array} { r l r } {  { p ( { \boldsymbol { \mathbf { x } } } | \mu , \lambda ) = \prod _ { n = 1 } ^ { N } ( \frac { \lambda } { 2 \pi } ) ^ { 1 / 2 } \exp \{ - \frac { \lambda } { 2 } ( x _ { n } - \mu ) ^ { 2 } \} } } \\ & { \propto } & { [ \lambda ^ { 1 / 2 } \exp ( - \frac { \lambda \mu ^ { 2 } } { 2 } ) ] ^ { N } \exp \{ \lambda \mu \sum _ { n = 1 } ^ { N } x _ { n } - \frac { \lambda } { 2 } \sum _ { n = 1 } ^ { N } x _ { n } ^ { 2 } \} . } \end{array}\tag{2.152}

$$

## 式153 (tag: 2.153)

$$

\begin{array} { r l r } {  { p ( \mu , \lambda ) \propto [ \lambda ^ { 1 / 2 } \exp ( - \frac { \lambda \mu ^ { 2 } } { 2 } ) ] ^ { \beta } \exp \{ c \lambda \mu - d \lambda \} } } \\ & { = } & { \exp \{ - \frac { \beta \lambda } { 2 } ( \mu - c / \beta ) ^ { 2 } \} \lambda ^ { \beta / 2 } \exp \{ - ( d - \frac { c ^ { 2 } } { 2 \beta } ) \lambda \} . } \end{array}\tag{2.153}

$$

## 式154 (tag: 2.154)

$$

p ( \mu , \lambda ) = { \mathcal { N } } ( \mu | \mu _ { 0 } , ( \beta \lambda ) ^ { - 1 } ) { \mathrm { G a m } } ( \lambda | a , b ) .\tag{2.154}

$$

## 式155 (tag: 2.155)

$$

\mathcal { W } ( \mathbf { A } | \mathbf { W } , \nu ) = B | \mathbf { A } | ^ { ( \nu - D - 1 ) / 2 } \exp \left( - \frac { 1 } { 2 } \mathrm { T r } ( \mathbf { W } ^ { - 1 } \pmb { \Lambda } ) \right) .\tag{2.155}

$$

## 式156 (tag: 2.156)

$$

B ( { \bf W } , \nu ) = | { \bf W } | ^ { - \nu / 2 } \left( 2 ^ { \nu D / 2 } \pi ^ { D ( D - 1 ) / 4 } \prod _ { i = 1 } ^ { D } \Gamma \left( \frac { \nu + 1 - i } { 2 } \right) \right) ^ { - 1 } ,\tag{2.156}

$$

## 式157 (tag: 2.157)

$$

p ( \pmb { \mu } , \pmb { \Lambda } | \pmb { \mu } _ { 0 } , \beta , \mathbf { W } , \nu ) = \mathcal { N } ( \pmb { \mu } | \pmb { \mu } _ { 0 } , ( \beta \pmb { \Lambda } ) ^ { - 1 } ) \mathcal { W } ( \pmb { \Lambda } | \mathbf { W } , \nu ) .\tag{2.157}

$$

## 式158 (tag: 2.158)

$$

\begin{array} { l } { \displaystyle p ( x | \mu , a , b ) = \int _ { 0 } ^ { \infty } \mathcal { N } ( x | \mu , \tau ^ { - 1 } ) \mathrm { G a m } ( \tau | a , b ) \mathrm { d } \tau } \\ { \displaystyle \qquad = \int _ { 0 } ^ { \infty } \frac { b ^ { a } e ^ { ( - b \tau ) } \tau ^ { a - 1 } } { \Gamma ( a ) } \left( \frac { \tau } { 2 \pi } \right) ^ { 1 / 2 } \exp \left\{ - \frac { \tau } { 2 } ( x - \mu ) ^ { 2 } \right\} \mathrm { d } \tau } \\ { \displaystyle \qquad = \frac { b ^ { a } } { \Gamma ( a ) } \left( \frac { 1 } { 2 \pi } \right) ^ { 1 / 2 } \left[ b + \frac { ( x - \mu ) ^ { 2 } } { 2 } \right] ^ { - a - 1 / 2 } \Gamma ( a + 1 / 2 ) . } \end{array}\tag{2.158}

$$

## 式159 (tag: 2.159)

$$

\mathrm { S t } ( x | \mu , \lambda , \nu ) = { \frac { \Gamma ( \nu / 2 + 1 / 2 ) } { \Gamma ( \nu / 2 ) } } \left( { \frac { \lambda } { \pi \nu } } \right) ^ { 1 / 2 } \left[ 1 + { \frac { \lambda ( x - \mu ) ^ { 2 } } { \nu } } \right] ^ { - \nu / 2 - 1 / 2 } .\tag{2.159}

$$

## 式160 (tag: 2.160)

$$

\operatorname { S t } ( x | \mu , \lambda , \nu ) = \int _ { 0 } ^ { \infty } \mathcal { N } \left( x | \mu , ( \eta \lambda ) ^ { - 1 } \right) \operatorname { G a m } ( \eta | \nu / 2 , \nu / 2 ) \mathrm { d } \eta .\tag{2.160}

$$

## 式161 (tag: 2.161)

$$

\operatorname { S t } ( \mathbf { x } | \mu , \Lambda , \nu ) = \int _ { 0 } ^ { \infty } \mathcal { N } ( \mathbf { x } | \mu , ( \eta \Lambda ) ^ { - 1 } ) \mathrm { G a m } ( \eta | \nu / 2 , \nu / 2 ) \mathrm { d } \eta .\tag{2.161}

$$

## 式162 (tag: 2.162)

$$

\operatorname { S t } ( { \bf x } | \mu , \Lambda , \nu ) = { \frac { \Gamma ( D / 2 + \nu / 2 ) } { \Gamma ( \nu / 2 ) } } { \frac { | \Lambda | ^ { 1 / 2 } } { ( \pi \nu ) ^ { D / 2 } } } \bigg [ 1 + { \frac { \Delta ^ { 2 } } { \nu } } \bigg ] ^ { - D / 2 - \nu / 2 }\tag{2.162}

$$

## 式163 (tag: 2.163)

$$

\Delta ^ { 2 } = ( { \bf x } - { \pmb \mu } ) ^ { \mathrm { T } } { \pmb \Lambda } ( { \bf x } - { \pmb \mu } ) .\tag{2.163}

$$

## 式164 (tag: 2.164)

$$

\nu > 1 0 ) \in \eth\tag{2.164}

$$

## 式165 (tag: 2.165)

$$

{ \mathrm { m o d e } } [ \mathbf { x } ] = \mu\tag{2.165}

$$

## 式166 (tag: 2.167)

$$

\overline { { \mathbf { x } } } = \frac { 1 } { N } \sum _ { n = 1 } ^ { N } \mathbf { x } _ { n }\tag{2.167}

$$

## 式167 (tag: 2.168)

$$

{ \overline { { x } } } _ { 1 } = { \overline { { r } } } \cos { \overline { { \theta } } } = { \frac { 1 } { N } } \sum _ { n = 1 } ^ { N } \cos \theta _ { n } , { \overline { { x } } } _ { 2 } = { \overline { { r } } } \sin { \overline { { \theta } } } = { \frac { 1 } { N } } \sum _ { n = 1 } ^ { N } \sin \theta _ { n }\tag{2.168}

$$

## 式168 (tag: 2.169)

$$

\overline { { \theta } } = \tan ^ { - 1 } \left\{ \frac { \sum _ { n } \sin \theta _ { n } } { \sum _ { n } \cos \theta _ { n } } \right\}\tag{2.169}

$$

## 式169 (tag: 2.170)

$$

p ( \theta ) \geqslant 0\tag{2.170}

$$

## 式170 (tag: 2.171)

$$

\int _ { 0 } ^ { 2 \pi } p ( \theta ) \mathrm { d } \theta = 1\tag{2.171}

$$

## 式171 (tag: 2.172)

$$

p ( \theta + 2 \pi ) = p ( \theta )\tag{2.172}

$$

## 式172 (tag: 2.173)

$$

p ( x _ { 1 } , x _ { 2 } ) = \frac { 1 } { 2 \pi \sigma ^ { 2 } } \exp \left\{ - \frac { ( x _ { 1 } - \mu _ { 1 } ) ^ { 2 } + ( x _ { 2 } - \mu _ { 2 } ) ^ { 2 } } { 2 \sigma ^ { 2 } } \right\} .\tag{2.173}

$$

## 式173 (tag: 2.174)

$$

x _ { 1 } = r \cos \theta , \qquad x _ { 2 } = r \sin \theta .\tag{2.174}

$$

## 式174 (tag: 2.175)

$$

\mu _ { 1 } = r _ { 0 } \cos \theta _ { 0 } , \qquad \mu _ { 2 } = r _ { 0 } \sin \theta _ { 0 } .\tag{2.175}

$$

## 式175 (tag: 2.176)

$$

\begin{array} { r l r } {  { - \frac { 1 } { 2 \sigma ^ { 2 } } \{ ( r \cos \theta - r _ { 0 } \cos \theta _ { 0 } ) ^ { 2 } + ( r \sin \theta - r _ { 0 } \sin \theta _ { 0 } ) ^ { 2 } \} } } \\ & { = } & { - \frac { 1 } { 2 \sigma ^ { 2 } } \{ 1 + r _ { 0 } ^ { 2 } - 2 r _ { 0 } \cos \theta \cos \theta _ { 0 } - 2 r _ { 0 } \sin \theta \sin \theta _ { 0 } \} } \\ & { = } & { \frac { r _ { 0 } } { \sigma ^ { 2 } } \cos ( \theta - \theta _ { 0 } ) + \mathrm { c o n s t } } \end{array}\tag{2.176}

$$

## 式176 (tag: 2.177)

$$

\cos ^ { 2 } A + \sin ^ { 2 } A = 1\tag{2.177}

$$

## 式177 (tag: 2.178)

$$

\cos A \cos B + \sin A \sin B = \cos ( A - B )\tag{2.178}

$$

## 式178 (tag: 2.179)

$$

p ( \theta | \theta _ { 0 } , m ) = \frac { 1 } { 2 \pi I _ { 0 } ( m ) } \exp \left\{ m \cos ( \theta - \theta _ { 0 } ) \right\} .\tag{2.179}

$$

## 式179 (tag: 2.180)

$$

I _ { 0 } ( m ) = \frac { 1 } { 2 \pi } \int _ { 0 } ^ { 2 \pi } \exp \left\{ m \cos \theta \right\} \mathrm { d } \theta .\tag{2.180}

$$

## 式180 (tag: 2.181)

$$

\ln p ( \mathcal { D } | \theta _ { 0 } , m ) = - N \ln ( 2 \pi ) - N \ln I _ { 0 } ( m ) + m \sum _ { n = 1 } ^ { N } \cos ( \theta _ { n } - \theta _ { 0 } )\tag{2.181}

$$

## 式181 (tag: 2.182)

$$

\sum _ { n = 1 } ^ { N } \sin ( \theta _ { n } - \theta _ { 0 } ) = 0\tag{2.182}

$$

## 式182 (tag: 2.183)

$$

\sin ( A - B ) = \sin A \cos B - \cos A \sin B\tag{2.183}

$$

## 式183 (tag: 2.184)

$$

\theta _ { 0 } ^ { \mathrm { M L } } = \tan ^ { - 1 } \left\{ \frac { \sum _ { n } \sin \theta _ { n } } { \sum _ { n } \cos \theta _ { n } } \right\}\tag{2.184}

$$

## 式184 (tag: 2.185)

$$

A ( m _ { \mathrm { M L } } ) = \frac { 1 } { N } \sum _ { n = 1 } ^ { N } \cos ( \theta _ { n } - \theta _ { 0 } ^ { \mathrm { M L } } )\tag{2.185}

$$

## 式185 (tag: 2.186)

$$

A ( m ) = \frac { I _ { 1 } ( m ) } { I _ { 0 } ( m ) } .\tag{2.186}

$$

## 式186 (tag: 2.187)

$$

A ( m _ { \mathrm { M L } } ) = \left( \frac { 1 } { N } \sum _ { n = 1 } ^ { N } \cos \theta _ { n } \right) \cos \theta _ { 0 } ^ { \mathrm { M L } } + \left( \frac { 1 } { N } \sum _ { n = 1 } ^ { N } \sin \theta _ { n } \right) \sin \theta _ { 0 } ^ { \mathrm { M L } } .\tag{2.187}

$$

## 式187 (tag: 2.188)

$$

p ( { \mathbf x } ) = \sum _ { k = 1 } ^ { K } \pi _ { k } { \mathcal N } ( { \mathbf x } | \mu _ { k } , \Sigma _ { k } ) .\tag{2.188}

$$

## 式188 (tag: 2.189)

$$

\sum _ { k = 1 } ^ { K } \pi _ { k } = 1\tag{2.189}

$$

## 式189 (tag: 2.190)

$$

0 \leqslant \pi _ { k } \leqslant 1 .\tag{2.190}

$$

## 式190 (tag: 2.191)

$$

p ( \mathbf { x } ) = \sum _ { k = 1 } ^ { K } p ( k ) p ( \mathbf { x } | k )\tag{2.191}

$$

## 式191 (tag: 2.192)

$$

\begin{array} { l } { \gamma _ { k } ( { \bf x } ) \equiv p ( k | { \bf x } ) } \\ { = \frac { p ( k ) p ( { \bf x } | k ) } { \sum _ { l } p ( l ) p ( { \bf x } | l ) } } \\ { = \frac { \pi _ { k } \mathcal { N } ( { \bf x } | \mu _ { k } , \Sigma _ { k } ) } { \sum _ { l } \pi _ { l } \mathcal { N } ( { \bf x } | \mu _ { l } , \Sigma _ { l } ) } } \end{array}\tag{2.192}

$$

## 式192 (tag: 2.193)

$$

\ln p ( { \mathbf X } | { \boldsymbol \pi } , { \boldsymbol \mu } , { \boldsymbol \Sigma } ) = \sum _ { n = 1 } ^ { N } \ln \left\{ \sum _ { k = 1 } ^ { K } \pi _ { k } { \mathcal N } ( { \mathbf x } _ { n } | { \boldsymbol \mu } _ { k } , { \boldsymbol \Sigma } _ { k } ) \right\}\tag{2.193}

$$

## 式193 (tag: 2.194)

$$

p ( \mathbf x | \boldsymbol \eta ) = h ( \mathbf x ) g ( \boldsymbol \eta ) \exp \left\{ \boldsymbol \eta ^ { \mathrm { T } } \mathbf u ( \mathbf x ) \right\} .\tag{2.194}

$$

## 式194 (tag: 2.195)

$$

g ( \pmb { \eta } ) \int h ( \mathbf x ) \exp \left\{ \pmb { \eta } ^ { \mathrm { T } } \mathbf { u } ( \mathbf x ) \right\} \ \mathrm d \mathbf x = 1\tag{2.195}

$$

## 式195 (tag: 2.196)

$$

p ( x | \mu ) = \mathrm { B e r n } ( x | \mu ) = \mu ^ { x } ( 1 - \mu ) ^ { 1 - x }\tag{2.196}

$$

## 式196 (tag: 2.197)

$$

\begin{array} { c } { { p ( x | \mu ) = \exp \left\{ x \ln \mu + ( 1 - x ) \ln ( 1 - \mu ) \right\} } } \\ { { = ( 1 - \mu ) \exp \left\{ \ln \left( \displaystyle \frac { \mu } { 1 - \mu } \right) x \right\} . } } \end{array}\tag{2.197}

$$

## 式197 (tag: 2.198)

$$

\eta = \ln \left( \frac { \mu } { 1 - \mu } \right) .\tag{2.198}

$$

## 式198 (tag: 2.199)

$$

\sigma ( \eta ) = \frac { 1 } { 1 + \exp ( - \eta ) } .\tag{2.199}

$$

## 式199 (tag: 2.200)

$$

p ( x | \eta ) = \sigma ( - \eta ) \exp ( \eta x ) .\tag{2.200}

$$

## 式200 (tag: 2.201)

$$

u ( x ) = x\tag{2.201}

$$

## 式201 (tag: 2.202)

$$

h ( x ) = 1\tag{2.202}

$$

## 式202 (tag: 2.203)

$$

g ( \eta ) = \sigma ( - \eta )\tag{2.203}

$$

## 式203 (tag: 2.204)

$$

p ( \mathbf x | \mu ) = \prod _ { k = 1 } ^ { M } \mu _ { k } ^ { x _ { k } } = \exp \left\{ \sum _ { k = 1 } ^ { M } x _ { k } \ln \mu _ { k } \right\} .\tag{2.204}

$$

## 式204 (tag: 2.205)

$$

p ( \mathbf { x } | \boldsymbol { \eta } ) = \exp ( \boldsymbol { \eta } ^ { \mathrm { T } } \mathbf { x } )\tag{2.205}

$$

## 式205 (tag: 2.206)

$$

\mathbf { u } ( \mathbf { x } ) = \mathbf { x }\tag{2.206}

$$

## 式206 (tag: 2.207)

$$

h ( \mathbf { x } ) = 1\tag{2.207}

$$

## 式207 (tag: 2.208)

$$

g ( \eta ) = 1\tag{2.208}

$$

## 式208 (tag: 2.209)

$$

\sum _ { k = 1 } ^ { M } \mu _ { k } = 1 .\tag{2.209}

$$

## 式209 (tag: 2.210)

$$

0 \leqslant \mu _ { k } \leqslant 1 , \qquad \sum _ { k = 1 } ^ { M - 1 } \mu _ { k } \leqslant 1 .\tag{2.210}

$$

## 式210 (tag: 2.211)

$$

\begin{array} { l } { \displaystyle \exp \left\{ \sum _ { k = 1 } ^ { M } x _ { k } \ln \mu _ { k } \right\} } \\ { \displaystyle = \exp \left\{ \sum _ { k = 1 } ^ { M - 1 } x _ { k } \ln \mu _ { k } + \left( 1 - \sum _ { k = 1 } ^ { M - 1 } x _ { k } \right) \ln \left( 1 - \sum _ { k = 1 } ^ { M - 1 } \mu _ { k } \right) \right\} } \\ { \displaystyle = \exp \left\{ \sum _ { k = 1 } ^ { M - 1 } x _ { k } \ln \left( \frac { \mu _ { k } } { 1 - \sum _ { j = 1 } ^ { M - 1 } \mu _ { j } } \right) + \ln \left( 1 - \sum _ { k = 1 } ^ { M - 1 } \mu _ { k } \right) \right\} . } \end{array}\tag{2.211}

$$

## 式211 (tag: 2.212)

$$

\ln \left( { \frac { \mu _ { k } } { 1 - \sum _ { j } \mu _ { j } } } \right) = \eta _ { k } .\tag{2.212}

$$

## 式212 (tag: 2.213)

$$

\mu _ { k } = \frac { \exp ( \eta _ { k } ) } { 1 + \sum _ { j } \exp ( \eta _ { j } ) }\tag{2.213}

$$

## 式213 (tag: 2.214)

$$

\underline { { p ( \mathbf { x } | \boldsymbol { \eta } ) } } = \left( 1 + \sum _ { k = 1 } ^ { M - 1 } \exp ( \eta _ { k } ) \right) ^ { - 1 } \exp ( \eta ^ { \mathrm { T } } \mathbf { x } ) .\tag{2.214}

$$

## 式214 (tag: 2.215)

$$

\mathbf { u } ( \mathbf { x } ) = \mathbf { x }\tag{2.215}

$$

## 式215 (tag: 2.216)

$$

h ( \mathbf { x } ) = 1\tag{2.216}

$$

## 式216 (tag: 2.217)

$$

g ( \eta ) = \left( 1 + \sum _ { k = 1 } ^ { M - 1 } \exp ( \eta _ { k } ) \right) ^ { - 1 }\tag{2.217}

$$

## 式217 (tag: 2.218)

$$

\begin{array} { c } { { p ( x | \mu , \sigma ^ { 2 } ) = \displaystyle \frac { 1 } { ( 2 \pi \sigma ^ { 2 } ) ^ { 1 / 2 } } \exp \left. - \frac { 1 } { 2 \sigma ^ { 2 } } ( x - \mu ) ^ { 2 } \right. } } \\ { { = \displaystyle \frac { 1 } { ( 2 \pi \sigma ^ { 2 } ) ^ { 1 / 2 } } \exp \left. - \frac { 1 } { 2 \sigma ^ { 2 } } x ^ { 2 } + \frac { \mu } { \sigma ^ { 2 } } x - \frac { 1 } { 2 \sigma ^ { 2 } } \mu ^ { 2 } \right. } } \end{array}\tag{2.218}

$$

## 式218 (tag: 2.220)

$$

\eta = { \binom { \mu / \sigma ^ { 2 } } { - 1 / 2 \sigma ^ { 2 } } }\tag{2.220}

$$

## 式219 (tag: 2.221)

$$

{ \mathbf u } ( x ) = \binom { x } { x ^ { 2 } }\tag{2.221}

$$

## 式220 (tag: 2.222)

$$

g ( \eta ) = ( - 2 \eta _ { 2 } ) ^ { 1 / 2 } \exp \left( \frac { \eta _ { 1 } ^ { 2 } } { 4 \eta _ { 2 } } \right)\tag{2.222}

$$

## 式221 (tag: 2.224)

$$

\begin{array} { l } { { \displaystyle \nabla g ( { \boldsymbol \eta } ) \int h ( { \bf x } ) \exp \{ { \boldsymbol \eta } ^ { \mathrm { T } } { \bf u } ( { \bf x } ) \} \ \mathrm { d } { \bf x } } \ ~ } \\ { { \displaystyle +  g ( { \boldsymbol \eta } ) \int h ( { \bf x } ) \exp \{ { \boldsymbol \eta } ^ { \mathrm { T } } { \bf u } ( { \bf x } ) \} { \bf u } ( { \bf x } ) \mathrm { d } { \bf x } = 0 } } \end{array}\tag{2.224}

$$

## 式222 (tag: 2.225)

$$

- \frac { 1 } { g ( \eta ) } \nabla g ( \eta ) = g ( \eta ) \int h ( \mathbf { x } ) \exp \left\{ \eta ^ { \mathrm { T } } \mathbf { u } ( \mathbf { x } ) \right\} \mathbf { u } ( \mathbf { x } ) \mathrm { d } \mathbf { x } = \mathbb { E } [ \mathbf { u } ( \mathbf { x } ) ]\tag{2.225}

$$

## 式223 (tag: 2.226)

$$

- \nabla \ln g ( \pmb { \eta } ) = \mathbb { E } [ \mathbf { u } ( \mathbf { x } ) ] .\tag{2.226}

$$

## 式224 (tag: 2.227)

$$

p ( \mathbf { X } | \boldsymbol { \eta } ) = \left( \prod _ { n = 1 } ^ { N } h ( \mathbf { x } _ { n } ) \right) g ( \boldsymbol { \eta } ) ^ { N } \exp \left\{ \boldsymbol { \eta } ^ { \mathrm { T } } \sum _ { n = 1 } ^ { N } \mathbf { u } ( \mathbf { x } _ { n } ) \right\}\tag{2.227}

$$

## 式225 (tag: 2.228)

$$

- \nabla \ln g ( \pmb { \eta } _ { \mathrm { M L } } ) = \frac { 1 } { N } \sum _ { n = 1 } ^ { N } \mathbf { u } ( \mathbf { x } _ { n } ) .\tag{2.228}

$$

## 式226 (tag: 2.229)

$$

p ( \eta | \chi , \nu ) = f ( \chi , \nu ) g ( \eta ) ^ { \nu } \exp \left\{ \nu \eta ^ { \mathrm { T } } \chi \right\} .\tag{2.229}

$$

## 式227 (tag: 2.230)

$$

p ( \eta | \mathbf { X } , \chi , \nu ) \propto g ( \eta ) ^ { \nu + N } \exp \left\{ \eta ^ { \mathrm { T } } \left( \sum _ { n = 1 } ^ { N } \mathbf { u } ( \mathbf { x } _ { n } ) + \nu \chi \right) \right\} .\tag{2.230}

$$

## 式228 (tag: 2.231)

$$

p _ { \eta } ( \eta ) = p _ { \lambda } ( \lambda ) \left| \frac { \mathrm { d } \lambda } { \mathrm { d } \eta } \right| = p _ { \lambda } ( \eta ^ { 2 } ) 2 \eta \propto \eta\tag{2.231}

$$

## 式229 (tag: 2.232)

$$

p ( x | \mu ) = f ( x - \mu ) .\tag{2.232}

$$

## 式230 (tag: 2.233)

$$

p ( \widehat { x } | \widehat { \mu } ) = f ( \widehat { x } - \widehat { \mu } )\tag{2.233}

$$

## 式231 (tag: 2.234)

$$

\int _ { A } ^ { B } p ( \mu ) \mathrm { d } \mu = \int _ { A - c } ^ { B - c } p ( \mu ) \mathrm { d } \mu = \int _ { A } ^ { B } p ( \mu - c ) \mathrm { d } \mu .\tag{2.234}

$$

## 式232 (tag: 2.235)

$$

p ( \mu - c ) = p ( \mu )\tag{2.235}

$$

## 式233 (tag: 2.236)

$$

p ( x | \sigma ) = { \frac { 1 } { \sigma } } f \left( { \frac { x } { \sigma } } \right) .\tag{2.236}

$$

## 式234 (tag: 2.237)

$$

p ( \widehat { x } | \widehat { \sigma } ) = \frac { 1 } { \widehat { \sigma } } f \left( \frac { \widehat { x } } { \widehat { \sigma } } \right) .\tag{2.237}

$$

## 式235 (tag: 2.238)

$$

\int _ { A } ^ { B } p ( \sigma ) \mathrm { d } \sigma = \int _ { A / c } ^ { B / c } p ( \sigma ) \mathrm { d } \sigma = \int _ { A } ^ { B } p \left( { \frac { 1 } { c } } \sigma \right) { \frac { 1 } { c } } \mathrm { d } \sigma\tag{2.238}

$$

## 式236 (tag: 2.239)

$$

p ( \sigma ) = p \left( { \frac { 1 } { c } } \sigma \right) { \frac { 1 } { c } }\tag{2.239}

$$

## 式237 (tag: 2.240)

$$

\mathcal { N } ( x | \mu , \sigma ^ { 2 } ) \propto \sigma ^ { - 1 } \exp \left\{ - ( \widetilde { x } / \sigma ) ^ { 2 } \right\}\tag{2.240}

$$

## 式238 (tag: 2.241)

$$

p _ { i } = \frac { n _ { i } } { N \Delta _ { i } }\tag{2.241}

$$

## 式239 (tag: 2.242)

$$

P = \int _ { \mathcal R } p ( \mathbf x ) \mathrm d \mathbf x\tag{2.242}

$$

## 式240 (tag: 2.243)

$$

\mathrm { B i n } ( K | N , P ) = \frac { N ! } { K ! ( N - K ) ! } P ^ { K } ( 1 - P ) ^ { N - K } .\tag{2.243}

$$

## 式241 (tag: 2.244)

$$

K \simeq N P\tag{2.244}

$$

## 式242 (tag: 2.245)

$$

P \simeq p ( \mathbf { x } ) V\tag{2.245}

$$

## 式243 (tag: 2.246)

$$

p ( \mathbf { x } ) = \frac { K } { N V } .\tag{2.246}

$$

## 式244 (tag: 2.247)

$$

k ( \mathbf { u } ) = \left\{ \begin{array} { l l } { 1 , } & { | u _ { i } | \leqslant 1 / 2 , \qquad i = 1 , \ldots , D \oslash \xi \stackrel { * } { \leqslant } } \\ { 0 , } & { \ z \nmid \land \bot \xi \rrangle , } \end{array} \right.\tag{2.247}

$$

## 式245 (tag: 2.248)

$$

K = \sum _ { n = 1 } ^ { N } k \left( { \frac { \mathbf { x } - \mathbf { x } _ { n } } { h } } \right)\tag{2.248}

$$

## 式246 (tag: 2.249)

$$

p ( \mathbf { x } ) = \frac { 1 } { N } \sum _ { n = 1 } ^ { N } \frac { 1 } { h ^ { D } } k \left( \frac { \mathbf { x } - \mathbf { x } _ { n } } { h } \right) .\tag{2.249}

$$

## 式247 (tag: 2.250)

$$

p ( { \bf x } ) = \frac { 1 } { N } \sum _ { n = 1 } ^ { N } \frac { 1 } { ( 2 \pi h ^ { 2 } ) ^ { D / 2 } } \exp \left\{ - \frac { \| { \bf x } - { \bf x } _ { n } \| ^ { 2 } } { 2 h ^ { 2 } } \right\} .\tag{2.250}

$$

## 式248 (tag: 2.251)

$$

k ( { \mathbf { u } } ) \geqslant 0 ,\tag{2.251}

$$

## 式249 (tag: 2.252)

$$

\int k ( { \mathbf { u } } ) \mathrm { d } { \mathbf { u } } = 1\tag{2.252}

$$

## 式250 (tag: 2.253)

$$

p ( \mathbf { x } | \mathcal { C } _ { k } ) = \frac { K _ { k } } { N _ { k } V } .\tag{2.253}

$$

## 式251 (tag: 2.254)

$$

p ( \mathbf { x } ) = \frac { K } { N V }\tag{2.254}

$$

## 式252 (tag: 2.255)

$$

p ( \mathcal { C } _ { k } ) = \frac { N _ { k } } { N }\tag{2.255}

$$

## 式253 (tag: 2.256)

$$

p ( \mathcal { C } _ { k } | \mathbf { x } ) = \frac { p ( \mathbf { x } | \mathcal { C } _ { k } ) p ( \mathcal { C } _ { k } ) } { p ( \mathbf { x } ) } = \frac { K _ { k } } { K } .\tag{2.256}

$$

## 式254 (tag: 2.257)

$$

\sum _ { x = 0 } ^ { 1 } p ( x | \mu ) = 1\tag{2.257}

$$

## 式255 (tag: 2.258)

$$

\mathbb { E } [ x ] = \mu\tag{2.258}

$$

## 式256 (tag: 2.259)

$$

\operatorname { v a r } [ x ] = \mu ( 1 - \mu )\tag{2.259}

$$

## 式257 (tag: 2.260)

$$

\operatorname { H } [ x ] = - \mu \ln \mu - ( 1 - \mu ) \ln ( 1 - \mu )\tag{2.260}

$$

## 式258 (tag: 2.261)

$$

p ( x | \mu ) = \left( \frac { 1 - \mu } { 2 } \right) ^ { ( 1 - x ) / 2 } \left( \frac { 1 + \mu } { 2 } \right) ^ { ( 1 + x ) / 2 }\tag{2.261}

$$

## 式259 (tag: 2.262)

$$

{ \binom { N } { m } } + { \binom { N } { m - 1 } } = { \binom { N + 1 } { m } }\tag{2.262}

$$

## 式260 (tag: 2.263)

$$

( 1 + x ) ^ { N } = \sum _ { m = 0 } ^ { N } { \binom { N } { m } } x ^ { m } .\tag{2.263}

$$

## 式261 (tag: 2.264)

$$

\sum _ { m = 0 } ^ { N } \binom { N } { m } \mu ^ { m } ( 1 - \mu ) ^ { N - m } = 1 .\tag{2.264}

$$

## 式262 (tag: 2.265)

$$

\int _ { 0 } ^ { 1 } \mu ^ { a - 1 } ( 1 - \mu ) ^ { b - 1 } \mathrm { d } \mu = { \frac { \Gamma ( a ) \Gamma ( b ) } { \Gamma ( a + b ) } }\tag{2.265}

$$

## 式263 (tag: 2.266)

$$

\Gamma ( a ) \Gamma ( b ) = \int _ { 0 } ^ { \infty } \exp ( - x ) x ^ { a - 1 } \mathrm { d } x \int _ { 0 } ^ { \infty } \exp ( - y ) y ^ { b - 1 } \mathrm { d } y\tag{2.266}

$$

## 式264 (tag: 2.267)

$$

\mathbb { E } [ \mu ] = \frac { a } { a + b }\tag{2.267}

$$

## 式265 (tag: 2.268)

$$

\operatorname { v a r } [ \mu ] = { \frac { a b } { ( a + b ) ^ { 2 } ( a + b + 1 ) } }\tag{2.268}

$$

## 式266 (tag: 2.269)

$$

{ \mathrm { m o d e } } [ \mu ] = { \frac { a - 1 } { a + b - 2 } }\tag{2.269}

$$

## 式267 (tag: 2.270)

$$

\mathbb { E } [ x ] = \mathbb { E } _ { y } \left[ \mathbb { E } _ { x } [ x | y ] \right]\tag{2.270}

$$

## 式268 (tag: 2.271)

$$

\operatorname { v a r } [ x ] = \mathbb { E } _ { y } \left[ \operatorname { v a r } _ { x } [ x | y ] \right] + \operatorname { v a r } _ { y } \left[ \mathbb { E } _ { x } [ x | y ] \right]\tag{2.271}

$$

## 式269 (tag: 2.272)

$$

p _ { M } ( \mu _ { 1 } , \dots , \mu _ { M - 1 } ) = C _ { M } \prod _ { k = 1 } ^ { M - 1 } \mu _ { k } ^ { \alpha _ { k } - 1 } \left( 1 - \sum _ { j = 1 } ^ { M - 1 } \mu _ { j } \right) ^ { \alpha _ { M } - 1 }\tag{2.272}

$$

## 式270 (tag: 2.273)

$$

\mathbb { E } [ \mu _ { j } ] = \frac { \alpha _ { j } } { \alpha _ { 0 } }\tag{2.273}

$$

## 式271 (tag: 2.274)

$$

\mathrm { v a r } [ \mu _ { j } ] = \frac { \alpha _ { j } ( \alpha _ { 0 } - \alpha _ { j } ) } { \alpha _ { 0 } ^ { 2 } ( \alpha _ { 0 } + 1 ) }\tag{2.274}

$$

## 式272 (tag: 2.275)

$$

j \neq l\tag{2.275}

$$

## 式273 (tag: 2.276)

$$

\mathbb { E } [ \ln \mu _ { j } ] = \psi ( \alpha _ { j } ) - \psi ( \alpha _ { 0 } )\tag{2.276}

$$

## 式274 (tag: 2.278)

$$

\mathrm { U } ( x | a , b ) = \frac { 1 } { b - a } , \qquad a \leqslant x \leqslant b\tag{2.278}

$$

## 式275 (tag: 2.279)

$$

\mathrm { H } [ \mathbf { x } ] = - \int p ( \mathbf { x } ) \ln p ( \mathbf { x } ) \mathrm { d } \mathbf { x }\tag{2.279}

$$

## 式276 (tag: 2.280)

$$

\int { p ( \mathbf { x } ) \mathrm { d } \mathbf { x } } = 1\tag{2.280}

$$

## 式277 (tag: 2.281)

$$

\int p ( \mathbf { x } ) \mathbf { x } \mathrm { d } \mathbf { x } = \boldsymbol { \mu }\tag{2.281}

$$

## 式278 (tag: 2.282)

$$

\int p ( \mathbf { x } ) ( \mathbf { x } - { \boldsymbol { \mu } } ) ( \mathbf { x } - { \boldsymbol { \mu } } ) ^ { \mathrm { { T } } } \mathrm { { d } } \mathbf { x } = \Sigma\tag{2.282}

$$

## 式279 (tag: 2.283)

$$

\mathrm { H } [ \mathbf { x } ] = \frac { 1 } { 2 } \ln \left| \pmb { \Sigma } \right| + \frac { D } { 2 } \left( 1 + \ln ( 2 \pi ) \right)\tag{2.283}

$$

## 式280 (tag: 2.284)

$$

p ( x ) = \int _ { - \infty } ^ { \infty } p ( x | x _ { 2 } ) p ( x _ { 2 } ) \mathrm { d } x _ { 2 } .\tag{2.284}

$$

## 式281 (tag: 2.285)

$$

\mathbf { a } ^ { \mathrm { T } } \mathbf { \Sigma } \mathbf { \mathbf { \bar { z } } } \mathbf { a } .\tag{2.285}

$$

## 式282 (tag: 2.286)

$$

V _ { D } | \Sigma | ^ { 1 / 2 } \Delta ^ { D }\tag{2.286}

$$

## 式283 (tag: 2.287)

$$

\left( \begin{array} { c c } { \mathbf { A } } & { \mathbf { B } } \\ { \mathbf { C } } & { \mathbf { D } } \end{array} \right) .\tag{2.287}

$$

## 式284 (tag: 2.288)

$$

\mu = \left( \begin{array} { l } { \mu _ { a } } \\ { \mu _ { b } } \\ { \mu _ { c } } \end{array} \right) , \qquad \Sigma = \left( \begin{array} { l l l } { \Sigma _ { a a } } & { \Sigma _ { a b } } & { \Sigma _ { a c } } \\ { \Sigma _ { b a } } & { \Sigma _ { b b } } & { \Sigma _ { b c } } \\ { \Sigma _ { c a } } & { \Sigma _ { c b } } & { \Sigma _ { c c } } \end{array} \right)\tag{2.288}

$$

## 式285 (tag: 2.289)

$$

\mathbf { ( A + B C D ) } ^ { - 1 } = \mathbf { A } ^ { - 1 } - \mathbf { A } ^ { - 1 } \mathbf { B } ( \mathbf { C } ^ { - 1 } + \mathbf { D A } ^ { - 1 } \mathbf { B } ) ^ { - 1 } \mathbf { D A } ^ { - 1 }\tag{2.289}

$$

## 式286 (tag: 2.290)

$$

\mathbf { z } = { \binom { \mathbf { x } } { \mathbf { y } } } \cdot\tag{2.290}

$$

## 式287 (tag: 2.291)

$$

\mathbb { E } [ { \mathbf { x } } _ { n } { \mathbf { x } } _ { m } ^ { \mathrm { T } } ] = { \mu \mu } ^ { \mathrm { T } } + I _ { n m } \boldsymbol { \Sigma }\tag{2.291}

$$

## 式288 (tag: 2.292)

$$

\sigma _ { \mathrm { M L } } ^ { 2 } = \frac { 1 } { N } \sum _ { n = 1 } ^ { N } ( x _ { n } - \mu ) ^ { 2 } .\tag{2.292}

$$

## 式289 (tag: 2.293)

$$

p ( x | \sigma ^ { 2 } , q ) = \frac { q } { 2 ( 2 \sigma ^ { 2 } ) ^ { 1 / q } \Gamma ( 1 / q ) } \exp \left( - \frac { | x | ^ { q } } { 2 \sigma ^ { 2 } } \right) ,\tag{2.293}

$$

## 式290 (tag: 2.294)

$$

\int _ { - \infty } ^ { \infty } p ( x | \sigma ^ { 2 } , q ) \mathrm { d } x = 1 .\tag{2.294}

$$

## 式291 (tag: 2.295)

$$

\mathbf { w } , \sigma ^ { 2 } ) = - \frac { 1 } { 2 \sigma ^ { 2 } } \sum _ { n = 1 } ^ { N } | y ( \mathbf { x } _ { n } , \mathbf { w } ) - t _ { n } | ^ { q } - \frac { N } { q } \ln ( 2 \sigma ^ { 2 } ) + \mathrm { c o n s t }\tag{2.295}

$$

## 式292 (tag: 2.296)

$$

\exp ( i A ) = \cos A + i \sin A .\tag{2.296}

$$

## 式293 (tag: 2.297)

$$

\exp ( i A ) \exp ( - i A ) = 1\tag{2.297}

$$

## 式294 (tag: 2.298)

$$

\cos ( A - B ) = \Re \exp \{ i ( A - B ) \}\tag{2.298}

$$

## 式295 (tag: 2.2)

$$

\cos \alpha = 1 - \frac { \alpha ^ { 2 } } { 2 } + O ( \alpha ^ { 4 } )\tag{2.2}

$$

## 式296 (tag: 2.300)

$$

- \nabla \nabla \ln g ( \boldsymbol { \eta } ) = \mathbb { E } [ \mathbf { u } ( \mathbf { x } ) \mathbf { u } ( \mathbf { x } ) ^ { \mathrm { T } } ] - \mathbb { E } [ \mathbf { u } ( \mathbf { x } ) ] \mathbb { E } [ \mathbf { u } ( \mathbf { x } ) ^ { \mathrm { T } } ] = \operatorname { c o v } [ \mathbf { u } ( \mathbf { x } ) ]\tag{2.300}

$$

