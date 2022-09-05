## 問題文

整数列 $A = (A_1, A_2, \dots, A_N)$ が与えられます。  
整数 $n, m\ (n≥m>0)$ に対して関数 $f(n, m)$ を

$f(n, m):=$ ( $n$ の約数のうち $m$ 以上で最小のもの)

と定義するとき、$\displaystyle \sum_{i=1}^{N} f(A_i, i)$ を求めてください。

## 制約

- $1 \le N \le 10^6$
- $i \le A_i \le 10^6$ ($1 ≤ i ≤ N$)
- 入力は全て整数

---

## 入力

入力は以下の形式で標準入力から与えられる。

> $N$  
> $A_1$ $A_2$ $\cdots$ $A_N$

## 出力

答えを出力せよ。答えは $32$ bit 整数に収まらないことがあるので注意せよ。

---

## 入力例 1

```
8
6 13 6 6 12 6 314159 265358
```

## 出力例 1

```
446873
```

$6$ の約数で $1$ 以上のものは $1, 2, 3, 6$ の $4$ 個であるので、$f(6, 1) = 1$ です。同様に、

- $f(13, 2) = 13$
- $f(6, 3) = 3$
- $f(6, 4) = 6$
- $f(12, 5) = 6$
- $f(6, 6) = 6$
- $f(314159, 7) = 314159$
- $f(265358, 8) = 132679$

で、合計は $446873$ になります。

---

## 入力例 2

```
2
1 2
```

## 出力例 2

```
3
```