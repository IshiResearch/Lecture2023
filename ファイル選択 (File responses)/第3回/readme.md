# 第3回 レビュー
* for文内でカウンタ変数iと同じ文字列を使用して、新たな変数を定義することはエラーの原因につながるため、カウンター変数と区別して定義しましょう。[[link](2023_04_18.ipynb)]

* 英大文字は定数扱い[[link](https://github.com/IshiResearch/Lecture2023/blob/main/%E3%83%95%E3%82%A1%E3%82%A4%E3%83%AB%E9%81%B8%E6%8A%9E%20(File%20responses)/%E7%AC%AC3%E5%9B%9E/2023_04_18_1.ipynb)]

* 英大文字は定数として扱うのが慣例です。定数は変更しないので、Dは小文字にして変数として扱うことが妥当です。[[link](kadai3.ipynb)]

* 何をしているコードなのかをコメントで説明しており、他人が読んでも理解しやすいです。[[link](ensyuu4.ipynb)]

* 英大文字は定数として扱うことが慣例となっているため、Sは英小文字の別の変数名にすることをお勧めします。[[link](2023_04_13.ipynb)]

> **命名規則**[[link](_exp3_1.ipynb)]  
英大文字は定数・英小文字は変数扱いです。その他のPythonの命名規則はこちらを参考にしてください  
[Python命名規則一覧
](https://qiita.com/naomi7325/items/4eb1d2a40277361e898b)

> **探索手法**[[link](_exp3_1.ipynb)]  
今回の推測ゲームでは、与えられた数値が基準値との大小関係を判定することで、探索範囲を縮小していき正解を求めます。この方法は二分探索法(バイナリサーチ)と呼ばれるアルゴリズムで、他にもどのような探索手法があるのか調べてみましょう。

