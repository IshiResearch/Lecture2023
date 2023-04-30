# 第2回 レビュー
* 全てのnに対して実行できるようにする方法を考えてみてください
* エラーの原因になるため、for文で使用する変数は、異なる変数名にしましょう。
* このようにすると、コードがすっきりすると思います。

```python
def radix2(decimal):
    binary = 0
    count = 0
    
    while decimal > 0:
        if decimal % 2 == 1:
            binary += 10**count
        count += 1
        decimal //= 2
    
    return binary
```
