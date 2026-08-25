--- RESULTADOS DO LAB 01 (AULA 03) ---
Mensagem: 'Preciso urgente da segunda via da fatura'
Intenção Predita: [segunda_via]
Vocabulário Filtrado (sem stopwords): ['2a', '2a via', 'aberto', 'acordo', 'acordo pagar', 'alterar', 'alterar endereço', 'app', 'atrasada', 'atualizo', 'atualizo dados', 'boleto', 'cadastramento', 'dados', 'dados residenciais', 'débito', 'débito aberto', 'dívida', 'emitir', 'emitir segunda', 'endereço', 'endereço cadastramento', 'fatura', 'fatura atrasada', 'fazer', 'fazer um', 'gostaria', 'gostaria alterar', 'negociar', 'negociar pagamento', 'no', 'no app', 'onde', 'onde atualizo', 'pagamento', 'pagamento dívida', 'pagar', 'pagar débito', 'posso', 'posso emitir', 'residenciais', 'residenciais no', 'segunda', 'segunda via', 'um', 'um acordo', 'via', 'via boleto', 'via fatura']

#========== PRODUÇÃO DO RELATÓRIO:==============
# 1 - Qual o impacto da remoção de stopwords no tamanho do vocabulário do modelo?
A remoção de stopwords diminui o tamanho do vocabulário, eliminando palavras genéricas que têm pouca importância para a classificação.

# 2 - O que significa a configuração ngram_range=(1, 2) no TfidfVectorizer?
ngram_range=(1, 2) faz o modelo considerar palavras individuais unigramas e combinações de duas palavras bigramas.

# 3 - Como a remoção de palavras genéricas ajuda a evitar classificações incorretas?
A remoção de palavras genéricas reduz o ruído nos dados, fazendo o modelo dar mais importância às palavras relevantes e diminuindo a chance de classificações incorretas.


--- RESULTADOS DO LAB 02 (AULA 03) ---

--- Relatório de Classificação ---
                     precision    recall  f1-score   support

horario_atendimento       0.50      1.00      0.67         1
        localizacao       1.00      0.50      0.67         2
    troca_devolucao       1.00      1.00      1.00         2

           accuracy                           0.80         5
          macro avg       0.83      0.83      0.78         5
       weighted avg       0.90      0.80      0.80         5

--- Matriz de Confusão ---
[[1 0 0]
 [1 1 0]
 [0 0 2]]

--- Comparação entre valores reais e previstos ---
                         Mensagem       Intenção Real    Intenção Predita
      Preciso devolver meu pedido     troca_devolucao     troca_devolucao
    Qual é a localização da loja?         localizacao horario_atendimento
       A loja funciona no sábado? horario_atendimento horario_atendimento
Posso trocar um produto comprado?     troca_devolucao     troca_devolucao
         Onde fica a loja fisica?         localizacao         localizacao

#========== PRODUÇÃO DO RELATÓRIO:==============
# 1 - O que representam as métricas Precision, Recall e F1-Score no relatório?
# 2 - Como interpretar a diagonal principal da Matriz de Confusão?
# 3 - Por que a acurácia isolada pode ser enganosa quando temos classes desbalanceadas?

         
