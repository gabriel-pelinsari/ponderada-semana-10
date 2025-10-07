# Detecção de SPAM com LSTM e GloVe

Este projeto implementa um modelo de detecção de **SPAM em SMS** utilizando duas abordagens:
1. **LSTM** com vetores **GloVe** pré-treinados;
2. **MLP** com vetorização **TF-IDF** (baseline).

---

## Estrutura
- `spam.csv` — dataset com 5.572 mensagens rotuladas como *ham* (não spam) ou *spam*.
- `spam_detection_colab.ipynb` — notebook com todo o pipeline.
- `README.md` — este arquivo explicativo.

---

## Resultados

| Modelo | Vetorização | Acurácia | Observações |
|---------|--------------|-----------|--------------|
| **MLP** | TF-IDF | **0.975** | Converge rapidamente, ótimo baseline |
| **LSTM** | GloVe | **0.839** | Precisa de mais épocas/dados para melhorar |

---

## Gráficos
- Distribuição de classes (ham/spam)
- Comprimento médio das mensagens
- Palavras mais frequentes por classe
- Matrizes de confusão para ambos os modelos

---

## Como rodar no Google Colab
1. Suba o arquivo `spam.csv` no ambiente Colab.
2. Copie o conteúdo do notebook deste repositório.
3. Execute célula por célula.
4. Observe os resultados de acurácia e gráficos gerados.

---

## Conclusões
- O modelo **LSTM + GloVe** capta melhor a semântica das palavras, mas precisa de mais iterações.
- O **MLP + TF-IDF** é uma alternativa leve e eficiente, com excelente performance.
- Em cenários reais, a combinação de embeddings densos e maior tempo de treinamento pode superar o baseline.

---
