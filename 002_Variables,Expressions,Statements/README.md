# Variables,Expressions,Statements

## 値（value）,型（type）
値は1,2や'Hello World'などを指している<br>
型は値と紐づいており、1,2と"Hello World"は別の型となり、1,2は数値型（interger）となり"Hello World"は文字列型（String）となる<br>

型を調べたいときは以下のようにすることで確認ができる
~~~python
  type('Hello World')
  type(11)

  # 実行結果は以下の通り
  <class 'str'>
  <class 'int'>
~~~
strはString（文字列型）の略でintはInteger（数値型）の略となります<br>
少しややこしい点としては以下を見てみましょう
~~~python
  type('11')
  type(11.0)

  # 実行結果は以下の通り
  <class 'str'>
  <class 'float'>
~~~
11は数値ですが、今度はstr（文字列型）と表示されています。これは11が''（シングルクォーテーション）にて囲まれているため、strとして判断をされています<br>
11.0は一見数値に見えますが小数点以下が記載されています、結果としてintではなくfloat（浮動小数点数型）と表示されている<br>

## 変数（valiables）
変数はプログラム上で名前を使用して値を参照できるようにするためのもの<br>
以下のプログラムは変数に値を代入しています
~~~python
  text = 'This is a first message!'
  number = 100

  type(text)
  type(number)

  # 実行結果は以下の通り
  <class 'str'>
  <class 'int'>
~~~

また、紙上で変数を表現する方法として一般的なのは変数の値を指す矢印と名前を書くこと<br>
具体的には以下のような図を書きますが、このような図の事を状態図（state diagram）と呼ぶ<br>
![IMG_7792](https://github.com/tcydig/python_textBook/assets/53115840/977b9ffd-b93e-4102-86f6-2d90d11ca6e3)

## 変数名とキーワード
変数名は変数に入る値を論理的に表す変数名を設定する<br>
※自分が作成したコードを将来別の誰かが見た際に処理を想像しやすいように<br>
Pythonにはキーワードと呼ばれるものがあり、その文字列は変数名として使用する事が出来ない<br>
※キーワードを主にインタープリターが構文を解析する際に使用している<br>

Python3の場合は以下の35個の文字がキーワードとなる
| False | await | else | import | pass |
| --- | --- | --- | --- | --- |
| None | break | except | in | raise |
| True | class | finally | is | return |
| and | continue | for | lambda | try |
| as | def | from | nonlocal | while |
| assert | del | global | not | with |
| async | elif | if | or | yield |

## 演算子（Operator）と被演算子（Operands）
演算子は加算や減算などで使用する「+」「-」の事です<br>
被演算子は加算や減算で計算される値の事を指します<br>
※1 + 1 であれば + が演算子で1 1 が被演算子です<br>

## 式（Expressions）,文（Statements）
式は変数や値、演算子などを表しており、以下はすべて式と言える
~~~python
  11
  S
  s + 11
~~~
文はPythonのインタープリタが実行できるコードの単位でprintや代入などを指します<br>
基本的に式も文の一つだと認識して問題ない
## Interactive mode and script mode
Interactive modeはプログラムをすぐに実行できる利点があり、コマンドラインに以下のようにプログラムを入力すればすぐに実行がされる<br>
~~~python
  2 * 2
  # 実行結果は以下の通り
  4
~~~
script modeの場合は通常一連のステートメントを定義しており、実行されると一つ一つのステートメントの結果を表示する<br>

## 計算順序（Order of operations）
計算の順序はある優先度に基づき決定がされ、その優先度の定義は数学の式のルートと同一である<br>
※カッコ内 -> 累乗 -> 掛け算・割り算 -> 足し算 -> 引き算

## String operations
Stringでも使用できる演算子があり、それは加算と乗算である<br>
挙動としては以下の通りである
~~~python
  'Hello' + 'world'
  'Hello' * 2
  # 実行結果は以下の通り
  'Helloworld'
  'HelloHello'
~~~
## コメント
作成したプログラマを他人が見た際に挙動を想定しやすいようにコメントと呼ばれるものを残す事がある<br>
Pythonの場合は#記号を使用して、#より後ろの文字はコメントとしてインタープリターからは無視される
~~~python
  num = 5 * 10
  # 上記の場合だと5が何を表していて10が何を表しているのkが分からない
  # そのため、以下のようにコメントを残すとわかりやすい

  # 人数 * お菓子数 で必要なお菓子の数を求める
  num = 5 * 10
  'Hello' * 2
~~~
上記のようなコメントは少なすぎるのも問題だが、多すぎるのも可読性を下げるため避けたほうが良い<br>
そのため、分かりやすい変数名などをつけてソースコードのみで推測できるものはコメントを入れず、適宜コメントを残す事で綺麗なソースコードを作成する事が出来る

## 参考文献
Think Python: How to Think Like a Computer Scientist (2nd ed.). (2016). O’Reilly Media. https://www.greenteapress.com/thinkpython/html/index.html

