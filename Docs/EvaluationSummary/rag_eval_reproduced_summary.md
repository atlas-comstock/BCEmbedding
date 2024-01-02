<!--
 * @Description: 
 * @Author: shenlei
 * @Date: 2023-12-31 23:44:03
 * @LastEditTime: 2024-01-01 00:51:40
 * @LastEditors: shenlei
-->
# RAG Evaluations in LlamaIndex  

## Reproduce [LlamaIndex Blog](https://blog.llamaindex.ai/boosting-rag-picking-the-best-embedding-reranker-models-42d079022e83)

| Embedding Models | WithoutReranker <br> [*hit_rate/mrr*] | CohereRerank <br> [*hit_rate/mrr*] | bge-reranker-base <br> [*hit_rate/mrr*] | bge-reranker-large <br> [*hit_rate/mrr*] | ***bce-reranker-base_v1*** <br> [*hit_rate/mrr*] | 
|:-------------------------------|:--------:|:--------:|:--------:|:--------:|:--------:| 
| OpenAI-ada-2 | 88.18/64.95 | 90.45/75.29 | 91.36/75.74 | 91.36/76.72 | **92.27/78.33** |  
| bge-large-en | 81.36/59.84 | 86.36/71.61 | 87.27/73.93 | 86.82/75.23 | **88.18/77.36** |  
| bge-base-en-v1.5 | 81.36/57.43 | 88.64/73.73 | 89.55/75.23 | 88.18/74.89 | **89.09/76.89** |  
| bge-large-en-v1.5 | 83.18/64.34 | 92.27/76.45 | 93.18/78.57 | 92.73/79.59 | **94.09/81.74** |  
| llm-embedder | 75.91/54.50 | 80.91/67.70 | 81.82/70.05 | 81.36/69.86 | **82.73/71.38** |  
| CohereV2 | 74.09/51.30 | 80.91/68.38 | 82.73/69.86 | 82.27/69.33 | **83.18/72.58** |  
| CohereV3 | 81.36/58.88 | 87.73/72.08 | 88.18/75.29 | 88.64/75.28 | **89.09/76.82** |  
| JinaAI-Small | 80.45/57.85 | 87.73/73.28 | 88.64/73.72 | 88.64/74.39 | **90.00/76.98** |  
| JinaAI-Base | 85.00/61.55 | 89.55/73.64 | 90.00/75.52 | 89.09/75.75 | **90.91/78.18** |  
| ***bce-embedding-base_v1*** | **91.36/71.20** | **92.73/77.65** | **95.00/79.01** | **95.00/79.95** | ***96.36/82.20*** |  