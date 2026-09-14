**Resultados Exercício 1**
Ambiente preparado com sucesso.

Frase original:
Olá!!! EU gostaria de saber se vocês estão DEVOLVENDO as mesas que foram compradas ontem.

Frase processada:
olá gostar saber devolver mesa comprar ontem
============================================================
DIAGNÓSTICO DO PRÉ-PROCESSAMENTO
============================================================

Texto original:
MEU sofá!!! chegou quebrado e quero DEVOLVER!!!

Texto normalizado:
sofá chegar quebrar querer devolver

Quantidade de caracteres:
47

Quantidade de tokens antes:
7

Quantidade de tokens depois:
5

Tokens removidos:
['meu', 'chegou', 'quebrado', 'e', 'quero']

Tokens finais:
['sofá', 'chegar', 'quebrar', 'querer', 'devolver']
============================================================


**Resultados Exercício 2**
Dataset carregado com sucesso!

Dimensões do dataset:
(80, 2)

Colunas disponíveis:
['mensagem', 'intencao']

Primeiras mensagens:
                                            mensagem            intencao
0                           Meu pedido está atrasado  logistica_entregas
1      Quero devolver este sofá que chegou com rasgo   trocas_devolucoes
2       Qual o prazo de entrega do sofá que comprei?  logistica_entregas
3                Quero consultar o status da entrega  logistica_entregas
4  Recebi um armário com peças quebradas e quero ...   trocas_devolucoes

Mensagens normalizadas:
                                            mensagem  \
0                           Meu pedido está atrasado   
1      Quero devolver este sofá que chegou com rasgo   
2       Qual o prazo de entrega do sofá que comprei?   
3                Quero consultar o status da entrega   
4  Recebi um armário com peças quebradas e quero ...   

                          mensagem_normalizada  
0                              pedido atrasado  
1            querer devolver sofá chegar rasgo  
2                   prazo entrega sofá comprei  
3              querer consultar status entrega  
4  recebi armário peça quebrar querer devolver  

Corpus tokenizado:
[['pedido', 'atrasado'], ['querer', 'devolver', 'sofá', 'chegar', 'rasgo'], ['prazo', 'entrega', 'sofá', 'comprei']]

Modelo FastText treinado com sucesso!
Tamanho do vocabulário: 126
Dimensão dos vetores: 50

============================================================
TESTE DO MEAN POOLING
============================================================

Frase original:
quero devolver meu sofá

Frase processada:
querer devolver sofá

Vetor da frase:
[-1.1444055e-03  3.8392479e-03 -2.1939666e-03 -7.9391472e-04
 -1.4140267e-03  8.9081826e-05  4.1476716e-04  3.0109684e-03
  1.0967570e-03 -7.6226890e-04  3.0127533e-03  1.0160076e-03
 -8.5002044e-04  9.0500439e-04  1.9247766e-03  1.2719772e-03
  2.0829651e-03 -9.5745240e-04 -2.6341403e-04 -8.0457382e-04
 -6.1296619e-04 -3.3252973e-03  3.4528822e-03 -2.2243378e-03
  2.8998780e-04  8.1541244e-04 -1.5951727e-03 -6.4407213e-04
  4.4661476e-03 -2.4794692e-03 -1.9865241e-03 -5.3886889e-04
  1.0192011e-03  4.2558536e-03 -4.6039640e-05  1.5072023e-03
 -1.3652485e-04 -7.1902253e-04  1.1253973e-03 -2.9362978e-03
 -7.5033261e-04 -1.9030712e-03 -3.0656112e-05  2.5657561e-04
  3.4153965e-04 -3.4380525e-03  7.1787671e-04  2.2113265e-03
 -2.0023379e-03  1.6102478e-03]

Dimensão do vetor:
(50,)

Vetores gerados para todas as mensagens!

============================================================
MATRIZ DE EMBEDDINGS
============================================================

Formato da matriz:
(80, 50)

Dimensão de cada vetor:
50

============================================================
RESUMO DO EXERCÍCIO 2
============================================================

Quantidade de mensagens:
80

Tamanho do vocabulário:
126

Dimensão dos embeddings:
50

Formato da matriz final:
(80, 50)

Exercício 2 concluído com sucesso!


**Resultados Exercício 3**

============================================================
DIVISÃO DOS DADOS
============================================================

Dados de treinamento:
(64, 50)

Dados de teste:
(16, 50)

Treinamento:
64

Teste:
16

============================================================
MODELO TREINADO
============================================================

Regressão Logística treinada com sucesso!

============================================================
AVALIAÇÃO DO MODELO
============================================================

Accuracy:
0.75

Relatório de classificação:
                    precision    recall  f1-score   support

logistica_entregas       1.00      0.75      0.86         4
   suporte_tecnico       1.00      0.75      0.86         4
 trocas_devolucoes       0.67      1.00      0.80         4
  vendas_orcamento       0.50      0.50      0.50         4

          accuracy                           0.75        16
         macro avg       0.79      0.75      0.75        16
      weighted avg       0.79      0.75      0.75        16


============================================================
MATRIZ DE CONFUSÃO
============================================================
[[3 0 0 1]
 [0 3 0 1]
 [0 0 4 0]
 [0 0 2 2]]

============================================================
TESTE DO CHATBOT
============================================================

Mensagem:
quero devolver meu sofá
Intenção:
FALLBACK_HUMANO
Confiança:
25.00%
------------------------------------------------------------

Mensagem:
como faço para realizar a devolução?
Intenção:
FALLBACK_HUMANO
Confiança:
25.00%
------------------------------------------------------------

Mensagem:
cadê meu pedido?
Intenção:
FALLBACK_HUMANO
Confiança:
25.01%
------------------------------------------------------------

Mensagem:
meu pedido nao chego
Intenção:
FALLBACK_HUMANO
Confiança:
25.01%
------------------------------------------------------------

Mensagem:
qual é a previsão do tempo?
Intenção:
FALLBACK_HUMANO
Confiança:
25.00%
------------------------------------------------------------



**Resultados Exercício 4**
============================================================
MODELOS TREINADOS
============================================================

Regressão Logística: OK
KNN: OK

============================================================
COMPARAÇÃO DOS MODELOS
============================================================
             Modelo Accuracy Precision Recall     F1
Regressão Logística    75.0%    79.17%  75.0% 75.36%
                KNN   56.25%     52.5% 56.25% 52.14%

============================================================
RECOMENDAÇÃO TÉCNICA
============================================================

Modelo recomendado: Regressão Logística
F1-Score: 75.36%


**Questão 1 - Qual modelo apresentou melhor desempenho?**
A Regressão Logística apresentou o melhor resultado. Ela teve 75% de Accuracy e 75,36% de F1, enquanto o KNN teve 56,25% de Accuracy e 52,14% de F1.

**Questão 2 - Por que os resultados podem ser diferentes mesmo utilizando os mesmos embeddings?**
Porque cada modelo trabalha de uma forma diferente. A Regressão Logística aprende com os dados de treinamento, enquanto o KNN compara a distância entre os exemplos. Por isso, mesmo usando os mesmos embeddings, os resultados podem ser diferentes.

**Questão 3 - O KNN utiliza distância. Por que a qualidade dos embeddings é particularmente importante para esse algoritmo?**
Porque o KNN usa a distância entre os vetores para decidir qual é a classe da mensagem. Se os embeddings representarem bem o significado das frases, mensagens parecidas ficarão mais próximas e o resultado será melhor.

**Questão 4 - Se o sistema tivesse 100 mil mensagens e centenas de intenções, você escolheria KNN? Justifique.**
Não. Eu escolheria a Regressão Logística, porque ela apresentou um resultado melhor neste teste e seria mais adequada para trabalhar com uma quantidade muito grande de mensagens.

**Questão 5 - Qual modelo você escolheria para colocar em produção neste cenário?**
Eu escolheria a Regressão Logística, pois ela apresentou melhores resultados em todas as métricas. Além disso, teve 75,36% de F1-Score, contra 52,14% do KNN.

