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
