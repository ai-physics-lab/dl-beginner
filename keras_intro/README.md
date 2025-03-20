# Keras + MNIST でモデルを構築・訓練しよう

このリポジトリでは、**Keras** を使って **MNIST データセット** でディープラーニングモデルを構築・訓練する方法を紹介します。  
詳細な解説は、以下のブログ記事をご覧ください。

 **[ブログ記事: Keras+MNISTでモデルを構築・訓練しよう](https://www.ai-physics-lab.com/entry/keras-mnist-tutorial)**

---

##  内容

本リポジトリでは、以下の内容を Jupyter Notebook (`keras_mnist.ipynb`) で実装しています。

### 1 **データの準備**
- MNIST データセットのロード
- データの前処理（ベクトル化・正規化）
- ラベルの one-hot encoding

### 2 **Keras で FCN（全結合ニューラルネットワーク）を構築**
- `Sequential()` を使ったモデルの定義
- `Dense()` レイヤーと `ReLU` 活性化関数
- `softmax` による分類出力

### 3 **モデルの学習と評価**
- `model.fit()` によるトレーニング
- 学習曲線（loss & accuracy）の可視化
- `model.evaluate()` によるテストデータでの評価
- 手書き数字の分類結果を可視化

---

## ノートブックの実行方法

### **1. Google Colab で開く**
Google Colab 上で Jupyter Notebook を開いて、すぐに実行できます。

▶ **[Google Colab で開く](https://colab.research.google.com/github/ai-physics-lab/dl-beginner/blob/main/keras_intro/keras_mnist.ipynb)**

### **2. ローカル環境で実行**
#### ** 必要なライブラリをインストール**
Python 3.x 環境で、以下のライブラリをインストールしてください。

```sh
pip install tensorflow numpy matplotlib

