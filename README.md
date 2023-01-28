# ChatGPTのプロンプト日英1対1対応集

## はじめに
ChatGPTは英語、日本語を含む様々な言語のテクストで学習しており、それらの言語で回答を生成することができます。ただし、質問の複雑さや特殊性、特定の言語での学習データの有無によって性能が異なる場合があります。

*-ChatGPT*

ChatGPTはインターネットに敬されている英語のコーパスで訓練された後、日本語のデータセットでファインチューニングされています。したがって、日本語より英語で質問(プロンプト)を書いた方が、より良い回答が得られると考えられます。ここではデータサイエンスにはじめ、様々なトピックで役立つChatGPTのプロンプトを集めています。

- [データサイエンス](#データサイエンス)
- [参考文献](#参考文献)

## データサイエンス
### Pythonコードを書く
#### 1. データ探索
|プロンプト|Prompt|
| --- | --- |
| データサイエンティストとして、私のためにコードを書いて欲しい。私は`[データセットの説明]`のデータセットを持っています。このデータの可視化と探索のためのコードを書いてください。| I want you to act as a data scientist and code for me. I have a dataset of `[describe dataset]`. Please write code for data visualisation and exploration.|

#### 2. 機械学習モデルの訓練
|プロンプト|Prompt|
| --- | --- |
| データサイエンティストとして、私のためにコードを書いて欲しい。私は`[データセットの説明]`のデータセットを持っています。`[ターゲット変数]`を予測する機械学習モデルを構築してください。| I want you to act as a data scientist and code for me. I have a dataset of `[describe dataset]`. Please build a machine learning model that predict `[target variable]`.

### コードの説明
#### 1. Pythonの場合
|プロンプト|Prompt|
| --- | --- |
| コードの説明役をしてほしい。このPythonのコードが何をしているのか、説明してもらえますか？`[Pythonコードを挿入]` | I want you to act as a code explainer. Can you explain to me what this Python code is doing? `[Insert Python code]`

#### 2. Rの場合
|プロンプト|Prompt|
| --- | --- |
| コードの説明役をしてほしい。このRのコードが何をしているのか、説明してもらえますか？`[Rコードを挿入]` | I want you to act as a code explainer. Can you explain to me what this R code is doing? `[Insert R code]`

#### 3. SQLの場合
|プロンプト|Prompt|
| --- | --- |
|コードの説明役をしてほしい。このSQLのコードが何をしているのか、説明してもらえますか？`[SQLコードを挿入]`| I want you to act as a code explainer. Can you explain to me what this SQL code is doing? `[Insert SQL code]`

### コードの最適化
#### 1. 実行速度の向上
|プロンプト|Prompt|
| --- | --- |
| ソフトウェア開発者の役をして欲しい。以下のPythonコードの時間的複雑さを改善するのを手伝って欲しい。`[コードを挿入]`| I want you to act as a software developer. Please help me improve the time complexity of the Python code below. `[Insert code]`

### コードの整理
#### 1. ドキュメンテーションの生成
|プロンプト|Prompt|
| --- | --- |
| ソフトウェア開発者の役をして欲しい。以下の`[関数名を挿入]`についてのドキュメントを提供してください。`[関数のコードを挿入]`| I want you to act as a software developer. Please provide documentation for the function `[Insert function name]` below. `[Insert function]`

#### 2. コードの読みやすさを向上
|プロンプト|Prompt|
| --- | --- |
| コード分析者の役をして欲しい。次のコードの可読性と保守性を改善できるだろうか。`[コードを挿入]` | I want you to act as a code analyzer. Can you improve the following code for readability and maintainability? `[Insert code]`

### コードの最適化

### コードの翻訳

## 参考文献
