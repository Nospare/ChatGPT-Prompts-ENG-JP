---
layout: default
title: 翻訳 Translate
parent: データサイエンス Datascience
nav_order: 5
---

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

### RからPythonへの翻訳

| プロンプト | Prompt |
| :--- | :--- |
| コード翻訳者の役をして欲しい。次のコードをRからPythonに変換してください。`[Rコードを挿入]` | I want you to act as a code translator. Can you please convert the following code from R to Python? `[Rコードを挿入]` |

#### 具体例 Example

{: .user-title}
> User
>
> I want you to act as a code translator. Can you please convert the following code from R to Python?
> 
> ```r
> library(dplyr)
> library(stringr)
> 
> data %>% 
>   mutate(
>     temperature = case_when(
>       temperature < 10 ~ "Cold",
>       temperature < 25 ~ "Mild",
>       temperature >= 25 ~ "Hot"
>     )
>   ) %>%
>   group_by(temperature) %>% 
>   summarise(N = n()) %>% 
>   ungroup() %>% 
>   mutate(percentage = N/sum(N) * 100)
> ```

{: .chatgpt-title}
> ChatGPT
> 
> ```python
> import pandas as pd
> 
> data = data.assign(
>     temperature=pd.cut(
>         data["temperature"],
>         bins=[-float("inf"), 10, 25, float("inf")],
>         labels=["Cold", "Mild", "Hot"]
>     )
> )
> 
> data = data.groupby("temperature").agg(N=("temperature", "count"))
> data["percentage"] = data["N"] / data["N"].sum() * 100
> data = data.reset_index()
> ```

### PythonからRへの翻訳

| プロンプト | Prompt |
| :--- | :--- |
| コード翻訳者の役をして欲しい。次のコードをPythonからRに変換してください。`[Pythonコードを挿入]` | I want you to act as a code translator. Can you please convert the following code from Python to R? `[Insert Python code]` |

### RからSQLへの翻訳

| プロンプト | Prompt |
| :--- | :--- |
| コード翻訳者の役をして欲しい。次のコードをRからSQLに変換してください。`[Rコードを挿入]` | I want you to act as a code translator. Can you please convert the following code from R to SQL? `[Insert R code]` |

#### 具体例 Example

{: .user-title}
> User
>
> I want you to act as a code translator. Can you please convert the following code from R to SQL?
> 
> ```r
> library(dplyr)
> library(stringr)
> 
> data %>% 
>   mutate(
>     temperature = case_when(
>       temperature < 10 ~ "Cold",
>       temperature < 25 ~ "Mild",
>       temperature >= 25 ~ "Hot"
>     )
>   ) %>%
>   group_by(temperature) %>% 
>   summarise(N = n()) %>% 
>   ungroup() %>% 
>   mutate(percentage = N/sum(N) * 100)
> ```

{: .chatgpt-title }
> ChatGPT
>
> ```sql
> SELECT 
>   temperature, 
>   COUNT(*) as N,
>   COUNT(*)/SUM(COUNT(*)) over() * 100 as percentage
> FROM (
>   SELECT 
>     CASE 
>       WHEN temperature < 10 THEN 'Cold'
>       WHEN temperature < 25 THEN 'Mild'
>       ELSE 'Hot'
>     END AS temperature
>   FROM data
> ) subquery
> GROUP BY temperature
> ```