# PyTorchの自動微分と誤差逆伝播を理解しよう

このリポジトリでは、**PyTorch** を使って、**自動微分（autograd）**と**誤差逆伝播**の基本的な流れを、1次関数モデルを例に解説します。  
Tensorの勾配計算と、`optimizer.step()` によるパラメータ更新の仕組みを、視覚的かつコードベースで学べる構成です。

詳細な解説は、以下のブログ記事をご覧ください。

📘 **[ブログ記事: PyTorchの「自動微分」と「誤差逆伝播」を徹底解説](https://www.ai-physics-lab.com/entry/pytorch-autograd-backpropagation)**

---

## 内容

本リポジトリでは、以下の内容を Jupyter Notebook (`tensor_autograd.ipynb`) に実装しています。

### 1 **Tensorとモデルの準備**
- 入力データ `x_train` と正解データ `y_train` の定義
- 単純な1次関数モデル `y = wx` の構築
- パラメータ `w` に `requires_grad=True` を設定

### 2 **順伝播と損失関数の定義**
- モデルの出力を計算
- 損失関数に2乗誤差を使用

### 3 **誤差逆伝播とパラメータ更新**
- `.backward()` による勾配計算
- `.grad` 属性による勾配確認
- `optimizer.step()` によるパラメータ更新
- `optimizer.zero_grad()` による勾配初期化

### 4 **結果の可視化**
- 学習前後のモデルとデータの比較プロット

---

## ノートブックの実行方法

### **1. Google Colab で開く**
Colab 上で開いてそのまま実行できます。

▶ **[Google Colab で開く](https://colab.research.google.com/github/ai-physics-lab/dl-beginner/blob/main/autograd_intro/tensor_autograd.ipynb)**

### **2. ローカル環境で実行**
#### **必要なライブラリをインストール**
以下のコマンドで必要なライブラリをインストールしてください：

```sh
pip install torch matplotlib

