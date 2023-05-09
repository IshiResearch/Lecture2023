# 第4回 レビュー
* ライブラリを使用しない場合も考えてみましょう。[[link](kadai4%20shimokawara.ipynb)]

> **raw文字列について**[[link](_exp4_1.ipynb)]  
パスを指定する際、raw文字列を使用するとエスケープシーケンスを無視して文字列をそのまま扱うことができます。raw文字列は文字列の前にrを付けて表現します。



e.g.

```python

path = r"C:\Users\user\Documents\test.txt"

``` 

> **複数ファイルのオープンについて** [[link](_exp4_1.ipynb)]  
with文ではカンマ区切りで複数のファイルをオープンすることができます。
e.g.

```python

with open("test1.txt", "r") as f1, open("test2.txt", "r") as f2:

    print(f1.read())

    print(f2.read())

```

> **ソートアルゴリズムについて**[[link](_exp4_1.ipynb)]  
今回、並べ替えにはsortメソッドを用いて、Timsortアルゴリズムによるソートを行っていますが、他にも様々なソートアルゴリズムがあります。以下に代表的なものが挙げられています。

[【Unity】ソートアルゴリズム12種を可視化してみた](https://qiita.com/r-ngtm/items/f4fa55c77459f63a5228)

[The Sound of Sorting - "Audibilization" and Visualization of Sorting Algorithms](https://panthema.net/2013/sound-of-sorting/)

