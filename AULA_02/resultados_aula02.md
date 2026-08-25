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

# 3 - Detalhe a função do Naive Bayes no algorítmo.



--- RESULTADOS DO LAB 03 ---
 # 1 - Qual foi a acurácia obtida pelo modelo no conjunto de teste e por que, em um dataset tão pequeno (9 exemplos), essa métrica pode ser enganosa?

A Acuaria foi de 33,33%, como o dataset tem apenas 9 exemplos, o resultado pode ser enganoso , pois foram usados poucos para teste. cade erro pode alterar bastante o resultado(porcentagem) da acuaria.

# 2 - Como o modelo de Árvore de Decisão (DecisionTreeClassifier) toma a decisão de separar as intenções do usuário?

A árvore da decisão analisa as palavras das mensagens e cria regras para separar as diferentes iintenções.

# 3 - Qual é o risco de utilizar uma Árvore de Decisão sem limite de profundidade (max_depth) em datasets de texto maiores?

O principal risco é o overfitting. ela fica complexa e aprende de mais os dados de treinamento, tendo dificuldades para classificar as mensagens novas.

--- RESULTADOS DO LAB 04 ---


