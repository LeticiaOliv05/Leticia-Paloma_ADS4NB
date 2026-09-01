# Relatório de Avaliação NLU - SAC Móveis Residenciais

## 1. Tabela Comparativa de Métricas (Dados de Teste)

| Modelo | Acurácia Geral | F1-Score (Weighted) | Principais Erros na Matriz |
| :--- | :--- | :--- | :--- |
| **KNN (K=3)** | 100,00% | 100,00% |
Não apresentou erros de classificação. Todas as 30 amostras foram classificadas corretamente. |
| **Decision Tree** | 80,00% | 80,00% |
Houve confusão principalmente entre Logística/Entregas e Vendas, Reclamações e Suporte, além de Trocas/Devoluções e Suporte. |

## 2. Análise dos Testes de Entrada (`input()`)

- **Comportamento do KNN (10 testes):**
 - O KNN apresentou bom desempenho nas frases relacionadas diretamente ao domínio do SAC. A frase "tem cupom para compra?" foi classificada como `vendas` com 100% de probabilidade. Frases sem relação clara com o atendimento, como "vou tomar refrigerante", "banana" e "Gustavo só inventa desculpa", foram encaminhadas para o fallback. Porém, algumas frases novas ou fora dos exemplos do treinamento, como "quero uma beliche", "quero dormir" e "gosto de verde", foram classificadas incorretamente, mostrando que o fallback não consegue identificar todos os casos fora do domínio.

- **Comportamento da Decision Tree (8 testes):**
- A Decision Tree apresentou algumas classificações corretas, como "onde esta o meu pedido", classificada como `logistica_entregas`, e "como montar o rack da sala", classificada como `suporte`. Entretanto, apresentou erros em frases relacionadas a compras. Por exemplo, "quero comprar uma beliche" e "quero comprar sofa retratil 3 lugares" foram classificadas como `trocas_devolucoes`, quando o esperado seria `vendas`. A frase "como rastreio o codigo de rastreamento" também foi classificada como `suporte`, apesar de estar relacionada à logística/entrega. Além disso, algumas classificações apresentaram 100% de probabilidade mesmo estando incorretas.

## 3. Veredito Final

- **Melhor modelo para este projeto:** **KNN (K=3)**

- **Justificativa técnica:**
- O KNN apresentou desempenho superior nos dados de teste, alcançando 100,00% de acurácia e 100,00% de F1-Score Weighted. Sua matriz de confusão não apresentou nenhum erro nas 30 amostras avaliadas. Já a Decision Tree apresentou 80,00% de acurácia e 80,00% de F1-Score Weighted, com algumas confusões entre as classes. Nos testes de entrada, os dois modelos apresentaram algumas classificações incorretas para frases novas, porém o KNN apresentou melhor desempenho geral. Portanto, o KNN é o modelo mais adequado para este projeto.
