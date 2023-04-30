# 第1回 レビュー
* if文を多く使用することは望ましくありません。if文を多く使用することは、プログラムの可読性を下げることにもなります。また、if文のネストが深くなると、プログラムのバグを見つけるのが難しくなります。and や or を使用して、if文を簡潔に書いてください。

(example)

```python
# 例
# 5つの数字を入力する
num1 = float(input("1つ目の数字を入力してください： "))
num2 = float(input("2つ目の数字を入力してください： "))
num3 = float(input("3つ目の数字を入力してください： "))
num4 = float(input("4つ目の数字を入力してください： "))
num5 = float(input("5つ目の数字を入力してください： "))

# 一番小さい値を見つける
min_num = num1

if num2 < min_num:
    min_num = num2

if num3 < min_num:
    min_num = num3

if num4 < min_num:
    min_num = num4

if num5 < min_num:
    min_num = num5

# 結果を表示する
print("一番小さい値は：", min_num)
```
* 以下のようにすると、可読性が上がります。
```python
jap = int(input("国語の点数："))
```
* while文1つで実行する方法も考えてみましょう。
* **for文は内部で最適化されているため、While文より高速に処理を実行できます。**
```python
import time

# forループの速度測定
start = time.time()
for i in range(10**7):
    pass
end = time.time()
print(f"forループ: {end - start}秒")

# whileループの速度測定
start = time.time()
i = 0
while i < 10**7:
    i += 1
end = time.time()
print(f"whileループ: {end - start}秒")
```

```
Output:
forループ: 0.24001169204711914秒
whileループ: 0.7509949207305908秒
```

* **同一直線上にあるかどうかを判定するプログラムでは、一つの座標を基準とした傾きから以下のようにif文一つで効率良く判定できます。**

```python
# 3つの点の座標を入力
x1, y1 = map(int, input("P1の座標を入力してください（x,y）：").split(','))
x2, y2 = map(int, input("P2の座標を入力してください（x,y）：").split(','))
x3, y3 = map(int, input("P3の座標を入力してください（x,y）：").split(','))

# 3つの点が同一線上にあるかどうかを判定
if (y2-y1)*(x3-x2) == (y3-y2)*(x2-x1):
    print("同一線上にあります")
else:
    print("同一線上にありません")

```
