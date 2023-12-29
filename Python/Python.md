# Pythonの基本情報まとめ

## 環境構築
- python
- Anaconda

## Anaconda
Anacondaは、Pythonプログラミング言語向けのオープンソースのディストリビューションおよびパッケージ管理システムです。以下はAnacondaの主な特徴と要点です。

### 1. パッケージ管理と環境管理
Anacondaは、科学計算やデータサイエンスのための豊富なパッケージを提供し、これらを簡単に管理できます。仮想環境を作成してプロジェクトごとに異なるバージョンのパッケージを使用できます。

### 2. Conda パッケージマネージャー
AnacondaはCondaと呼ばれるパッケージマネージャーを使用しており、これによりパッケージのインストール、アップデート、削除が容易になります。CondaはPythonだけでなく、他の言語やツールにも拡張されています。

### 3. 科学計算向けのパッケージ
AnacondaにはNumPy、SciPy、Pandas、Matplotlibなどの主要な科学計算ライブラリが含まれており、データ分析や機械学習のプロジェクトに便利です。

### 4. Jupyter ノートブック
AnacondaにはJupyterノートブックが含まれており、対話的なデータ分析や可視化を支援します。ノートブック形式でコードと結果を組み合わせてドキュメントを作成できます。

### 5. クロスプラットフォームサポート
AnacondaはWindows、macOS、Linuxなど、さまざまなプラットフォームで利用可能です。

### 6. 教育および研究
Anacondaは教育機関や研究機関で広く利用されており、データサイエンスや科学計算の教育および研究において、一般的な選択肢となっています。

Anacondaはデータサイエンスや科学技術計算の分野で広く利用され、開発者やデータサイエンティストにとって非常に重要なツールとなっています。

## Pythonの配列について
### 配列の定義
```
a = []
```

### 多次元配列の定義
```Python
a = [["hoge", "huga"], ["hage", "hega"]]

// 呼び出し方
print(a[0][0]) == hoge
print(a[0][1]) == huga
print(a[1][0]) == hage
print(a[1][1]) == hega
```

## Pythonの演算子
多言語と変わりなしだが、論理演算子のみPHPと記述が違う

### 論理演算子
- PHP: || python: or
- PHP: && python: and

## Pythonの代入演算子
他言語と変わりなし

## 条件分岐
基本構文
```Python
if文
if 条件：
　条件の内容
```
* 例文
```Python
age = 22
if age => 20:
  print("abult")
 elif age = 20:
  print("GOOD")
 else:
  print("child")
```

## Pythonのループ処理
- for文

### 基本構文
```Python
for カウンタ変数(i) in range(繰り返す回数):
    繰り返し中に実行する処理
```

### 例文
```Python
例①
for i in range(5):
    if i == 2:
        break:
    if i == 3:
        continue
    print(i)


例② for文の中に、for文を入れる場合
for i in range(5):
    for j in range(3):
        print(i, j, sep="-")
        ※　sep引数によって間にハイフンを代入している
```

## Pythonの関数定義
### 基本構文
```Python
def 関数名(引数):
    実行する処理

例文
def say_hello():
    print("hello world")

// 実行
say_hello()

例文２
def div(a, b, c):
    return (a + b + c)/3

result = div(1, 2, 3)
print(result)
```

## Pythonのクラスについて
### クラス（Class）
Pythonでは、
1. データのことをアトリビュート（attribute）と呼ぶ
   1. attributeとは、クラス内で定義される変数のこと
2. 処理のことをメソッドと呼ぶ
   1. メソッドは、クラス内で定義される処理のこと

### Pythonのクラスでの注意点
#### 関数（クラス定義なし）の場合、引数は定義しなくてもOK
```Python
def avg():
    print((80 + 70) / 2)
```

**メソッド（クラス内関数）については、渡したい引数が存在しない場合でも、引数を書かないと行けない**
```Python
def avg(self):
    print(80 + 10)
```

**※渡したい引数がない場合は、慣習的に```self```と記述しておく**

#### 引数を渡したい場合
- 引数1つの場合
```Python
def avg(self, hoge):
    print(hoge)
```

- 引数2つの場合
```Python
def avg(self, hoge, huga):
    print(hoge + huga)
```

## Pythonのコンストラクタについて
他言語と大幅に違いはない

### 基本構文
```Python
class Student:

    # コンストラクタ
    def __init__(self):
        self.name = ""

    def avg (self, math ,english):
        print((math + english) / 2)

# 実行文
# クラスのインスタンス作成
a001 = Student()

# nmae に "sato" を代入
a001.name = "sato"
print(a001.name)       # 実行結果 "sato"

# nmae に "taro" を代入
a002.name = "taro"
print(a002.name)       # 実行結果 "sato"
```

### インスタンス作成と同時に引数を渡す
```Python
class Student:

    # コンストラクタ
    def __init__(self):
        self.name = ""

    def avg (self, math ,english):
        print((math + english) / 2)

# 実行文
a001 = Student("sato")
print(a001.name)       # 実行結果 "sato"

a002 = Student("taro")
print(a002.name)       # 実行結果 "sato"
```

## 問題
① ~ ⑤の名称はなにか？
```Python
class Student:

    ③　def __init__(self):
        ④　self.name = ""

    ⑤　def avg (self, math ,english):
        print((math + english) / 2)

①　a001 = ②　Student("sato")
print(a001.name)
```

## 回答
①インスタンス
②クラス
③コンストラクタ
④アトリビュート
⑤メソッド
