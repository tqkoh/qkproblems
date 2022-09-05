## 問題文

長さ $N$ の整数列 $A = (A_1, A_2, \dots, A_N)$ が与えられます。$A$ から $K$ 個の整数を取り出す方法は $\binom NK$ 通りありますが、$\binom NK$ 個の取り出し方それぞれについて取り出した整数の最大値を求め、その総和を $998244353$ で割った余りを出力してください。(取り出した $K$ 個の整数が同じでも、取り出した位置が一つでも違えば、別の組として数えます。)

すなわち、

$$
\left(\sum_{1\le i_1<i_2<\dots<i_K\le N} \max\{A_{i_1}, A_{i_2}, \dots, A_{i_K}\} \right)\bmod 998244353
$$

を出力してください。

## 制約

- $1 \le N \le 2 \times 10^5$
- $1 \le K \le N$
- $1 \le A_i \le 10^9$ ($1≤i≤N$)
- 入力は全て整数

---

## 入力

入力は以下の形式で標準入力から与えられる。

> $N$ $K$  
> $A_1$ $A_2$ $\cdots$ $A_N$

## 出力

答えを出力せよ。

---

## 入力例 1

```
3 2
2 3 2
```

## 出力例 1

```
8
```
数列 $A = (2, 3, 2)$ から整数を $2$ つ取り出す方法は $3$ 通りあります。$2$ と $3$ の組が二つありますが、$2$ を選んだ位置が違うため別で数えることに注意してください。

$\max\{2, 3\} = 3,\ \max\{2, 2\} = 2,\ \max\{3, 2\} = 3$ の和である $8$ を出力します。


## 入力例 2

```
1 1
1
```

## 出力例 2

```
1
```

## 入力例 3

```
6 3
123456789 987654321 314159265 998244352 998244353 998244354
```

## 出力例 3

```
987654328
```

$998244353$ で割った余りを出力することに注意してください。