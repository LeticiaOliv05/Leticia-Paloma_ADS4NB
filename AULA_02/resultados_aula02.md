--- RESULTADOS DO LAB 01 ---

# 1 - Avaliem os resultados e verifiquem se os resultados foram corretos ou incorretos. Coloque a resposta no arquivo do relatório do laboratório

Mensagem: 'Quero consultar quanto dinheiro tenho' ==> Intenção Predita: [consultar_saldo]
Mensagem: 'Pode me ajudar a fazer um pix?' ==> Intenção Predita: [fazer_pix]
Mensagem: 'Gostaria de cancelar meu cartão de crédito' ==> Intenção Predita: [cancelar_conta]

# 2 - Detectado algum erro, qual seria a maneira mais correta de melhorar o resultado do algoritmo?
O erro aconteceu por que a frase foi classificada  com uma intenção diferente da esperada, alterando e acrescentando  exemplos diversificados fazemos com que o LogisticRegression  consiga identificar corretamente cada intenção.

# 3 - Detalhe a função do LogisticRegression no algorítmo.
Classificar as frases de acordo com sua intenção, com dados de entrada para saídas desejadas, a partir de exemplos rotulados.


--- RESULTADOS DO LAB 02 ---

# 1 - Avaliem os resultados e verifiquem se os resultados foram corretos ou incorretos. Coloque a resposta no arquivo do relatório do laboratório
Mensagem de Teste: 'Gostaria de devolver o produto que comprei'
Intenção Predita: troca_devolucao

--- Distribuição de Probabilidades por Classe ---
Classe [duvida_frete]: 18.68%
Classe [rastrear_pedido]: 17.79%
Classe [troca_devolucao]: 63.53%

# 2 - Detectado algum erro, qual seria a maneira mais correta de melhorar o resultado do algoritmo?
Não houve erro na classificação. Para melhorar o algoritmo, seria importante aumentar e diversificar o dataset, adicionando mais exemplos para cada intenção.
# 3 - Detalhe a função do Naive Bayes no algorítmo.
O Naive Bayes classifica a mensagem calculando a probabilidade de ela pertencer a cada intenção. Ele escolhe a classe com maior probabilidade. Neste caso, classificou a mensagem como troca_devolucao.


--- RESULTADOS DO LAB 03 ---
 # 1 - Qual foi a acurácia obtida pelo modelo no conjunto de teste e por que, em um dataset tão pequeno (9 exemplos), essa métrica pode ser enganosa?

A Acuaria foi de 33,33%, como o dataset tem apenas 9 exemplos, o resultado pode ser enganoso , pois foram usados poucos para teste. cade erro pode alterar bastante o resultado(porcentagem) da acuaria.

# 2 - Como o modelo de Árvore de Decisão (DecisionTreeClassifier) toma a decisão de separar as intenções do usuário?

A árvore da decisão analisa as palavras das mensagens e cria regras para separar as diferentes iintenções.

# 3 - Qual é o risco de utilizar uma Árvore de Decisão sem limite de profundidade (max_depth) em datasets de texto maiores?

O principal risco é o overfitting. ela fica complexa e aprende de mais os dados de treinamento, tendo dificuldades para classificar as mensagens novas.


--- RESULTADOS DO LAB 04 ---

DATASET COMPLETO:
                                                frase          intencao
0           Quero comprar uma passagem para São Paulo  comprar_passagem
1       Preciso reservar um voo para o Rio de Janeiro  comprar_passagem
2              Gostaria de comprar uma passagem aérea  comprar_passagem
3   Quero viajar para Salvador e preciso de uma pa...  comprar_passagem
4                Como faço para comprar uma passagem?  comprar_passagem
5                        Quero cancelar minha reserva  cancelar_reserva
6                            Preciso cancelar meu voo  cancelar_reserva
7     Não vou mais viajar e quero cancelar a passagem  cancelar_reserva
8                  Como posso cancelar minha reserva?  cancelar_reserva
9                Gostaria de desistir da minha viagem  cancelar_reserva
10                       Quero falar com um atendente   falar_atendente
11                     Preciso de ajuda de uma pessoa   falar_atendente
12               Posso falar com um atendente humano?   falar_atendente
13              Quero conversar com alguém da agência   falar_atendente
14                        Preciso falar com o suporte   falar_atendente

==================================================
QUANTIDADE DE FRASES POR INTENÇÃO:
intencao
comprar_passagem    5
cancelar_reserva    5
falar_atendente     5
Name: count, dtype: int64

==================================================
DIVISÃO DOS DADOS
==================================================
Quantidade de frases para treino: 11
Quantidade de frases para teste: 4

==================================================
VETORIZAÇÃO
==================================================
Formato dos dados de treino: (11, 36)
Formato dos dados de teste: (4, 36)

==================================================
MODELO TREINADO COM SUCESSO!
==================================================

==================================================
RESULTADOS DO CONJUNTO DE TESTE
==================================================

Frase: Posso falar com um atendente humano?
Intenção real: falar_atendente
Intenção prevista: falar_atendente
----------------------------------------

Frase: Preciso falar com o suporte
Intenção real: falar_atendente
Intenção prevista: falar_atendente
----------------------------------------

Frase: Gostaria de desistir da minha viagem
Intenção real: cancelar_reserva
Intenção prevista: comprar_passagem
----------------------------------------

Frase: Como faço para comprar uma passagem?
Intenção real: comprar_passagem
Intenção prevista: comprar_passagem
----------------------------------------

==================================================
ACURÁCIA DO MODELO
==================================================
Acurácia: 75.00%

==================================================
RELATÓRIO DE CLASSIFICAÇÃO
==================================================
                  precision    recall  f1-score   support

cancelar_reserva       0.00      0.00      0.00         1
comprar_passagem       0.50      1.00      0.67         1
 falar_atendente       1.00      1.00      1.00         2

        accuracy                           0.75         4
       macro avg       0.50      0.67      0.56         4
    weighted avg       0.62      0.75      0.67         4


==================================================
PREDIÇÕES COM FRASES INÉDITAS
==================================================

Frase: Gostaria de comprar um voo para Recife
Intenção prevista: comprar_passagem
----------------------------------------

Frase: Preciso desistir da reserva da minha viagem
Intenção prevista: cancelar_reserva
----------------------------------------

Frase: Quero conversar com uma pessoa da agência
Intenção prevista: falar_atendente
----------------------------------------

==================================================
FIM DO DESAFIO NLU
==================================================


Neste laboratório, foi desenvolvido um protótipo de NLU (Natural Language Understanding) para uma agência de viagens. Foi criado um dataset próprio com 15 frases, distribuídas em três intenções: comprar_passagem, cancelar_reserva e falar_atendente.

Os dados foram divididos em conjuntos de treino e teste utilizando o train_test_split. Para transformar os textos em dados numéricos, foi utilizado o TfidfVectorizer, e o algoritmo escolhido para a classificação foi o LogisticRegression.

Após o treinamento, o modelo foi testado com frases inéditas e conseguiu identificar as intenções relacionadas à compra de passagens, cancelamento de reservas e atendimento humano.

O desafio demonstrou como técnicas de Machine Learning e Processamento de Linguagem Natural podem ser utilizadas para criar um chatbot capaz de compreender a intenção do usuário.
