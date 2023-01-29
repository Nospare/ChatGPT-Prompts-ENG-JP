---
layout: default
title: コーディング Coding
parent: データサイエンス Datascience
nav_order: 1
---

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

### データ探索 Explore Data

| プロンプト | Prompt |
|:--- |:--- |
| データサイエンティストとして、私のためにコードを書いて欲しい。私は`[データセットの説明]`のデータセットを持っています。このデータの可視化と探索のためのコードを書いてください。| I want you to act as a data scientist and code for me. I have a dataset of `[describe dataset]`. Please write code for data visualisation and exploration.|

### 機械学習モデルの訓練 Train a Machine Learning Model

| プロンプト | Prompt |
|:--- |:--- |
| データサイエンティストとして、私のためにコードを書いて欲しい。私は`[データセットの説明]`のデータセットを持っています。`[ターゲット変数]`を予測する機械学習モデルを構築してください。| I want you to act as a data scientist and code for me. I have a dataset of `[describe dataset]`. Please build a machine learning model that predict `[target variable]`.|

### データの生成 Generate Data

| プロンプト | Prompt |
| :--- | :--- |
| あなたにはプログラマーの役をしてもらいたい。`[データセットの説明]`の偽のデータセットを生成するためのPythonコードを書いてください。データはpandasのDataFrameに格納される。データには、`[変数]`が含まれます。 | I want you to act as a programmer. You will write the Python to generate a fake dataset of `[describe dataset]`. The data will be stored in a pandas DataFrame. The data will contain contain: `[variables in the dataset]`|

#### 具体例 Example

{: .user-title}
> User
> 
> I want you to act as a programmer. You will write the Python code to generate a fake dataset of McDonals sales in Japan. The data will be stored in a pandas DataFrame. The data will contain three columns: name of the product, price, and number of items sold in a month.
>
> **和訳**:
> あなたにはプログラマーの役をしてもらいたい。日本におけるマクドナルドの売上高の偽のデータセットを生成するためのPythonコードを書いてください。データはpandasのDataFrameに格納される。データには、商品名、価格、1ヶ月に売れた個数の3つの列が含まれます。

{: .chatgpt-title}
> ChatGPT
>
> Sure! Here's a code to generate a fake dataset of McDonalds sales in Japan: 
>
> **和訳**
> もちろん！日本のマクドナルドの売り上げに関する偽のデータセットを生成するコードはこちらです。
>
> ```python
> import pandas as pd
> import random
> 
> products = ['Big Mac', 'Quarter Pounder', 'McChicken', 'Filet-O-Fish', 'Happy Meal']
> prices = [450, 500, 400, 350, 400]
> sales = [random.randint(500, 5000) for i in range(5)]
> 
> df = pd.DataFrame({'Product': products, 'Price': prices, 'Sales': sales})
> ```
> 
> This code creates a list of 5 products, with corresponding prices, and generates random sales figures for each product using the random module. The resulting data is then stored in a Pandas DataFrame with the column names 'Product', 'Price', and 'Sales'.
> 
> **和訳**
> このコードでは、5つの商品とそれに対応する価格のリストを作成し、randomモジュールを使用して各商品のランダムな販売数を生成しています。生成されたデータは、'Product'、'Price'、'Sales'というカラム名を持つ Pandas DataFrame に格納されます。