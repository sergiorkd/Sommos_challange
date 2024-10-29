# Sommos_challange

Neste desafio você deverá apresentar o domínio de um case e o conjunto de dados relacionado. 
Contextualização - Correção Automática de Redações

Em Processamento de Língua Natural (PLN), uma solução completa de Correção Automática de Redação deve contemplar pelo menos três etapas básicas:

1. A detecção de desvios no texto;
2. A atribuição da nota, seja ela global ou por critério de avaliação; e
3. A elaboração de um feedback para o aluno.

O Exame Nacional do Ensino Médio (Enem) é uma prova do Governo Federal que avalia o desempenho escolar dos estudantes ao término do Ensino Médio. Essa prova avalia várias áreas do conhecimento e, também, a produção de uma redação. Com mais de 3,9 milhões de inscritos em 2023, o Enem pode ser considerado o principal modelo de correção de redação no Brasil.
No modelo de correção do Enem, o aluno deve produzir um texto do tipo dissertativo-argumentativo para um tema específico. A avaliação é dividida em 5 competências, cada uma no intervalo de notas de 0 a 200: (i) Língua Portuguesa, (ii) Tema e Gênero, (iii) Coerência, (iv) Coesão e (v) Proposta de Intervenção (sugestão de ação ou medida interventiva para solucionar ou minimizar o problema associado ao tema proposto). A soma direta das notas das competências leva à nota total, que fica no intervalo de 0 a 1000.

Escopo e entrega
Para o desafio, você deve:

1. Ler e entender a contextualização. Sinta-se à vontade para pesquisar mais sobre o assunto também;
2. Trabalhar na análise descritiva do conjunto público de redações Essay-br;
3. Fazer anotações de suas suposições e dúvidas quanto às etapas básicas da correção automática de redações;
4. Esboçar um plano de solução: por onde você começaria? Qual a stack tecnológica? Técnicas, features, algoritmos etc.

Caso você queira tentar modelar o plano de solução, total ou parcialmente, você pode fazer isso. No entanto, o foco de avaliação será, principalmente, para os itens enumerados acima. 
Você deverá compartilhar conosco (repositório Git) os códigos produzidos e registro de esboço do plano de solução. Caso você tenha elaborado o esboço em papel, pode enviar uma foto anexa ao e-mail com indicação do repositório Git. 
______________________________________________________________________________________________________________________

1.	Principais dúvidas e questionamentos:

•	Quais bibliotecas utilizar? Utilizar modelos pré treinados?
•	Fazer um modelo capaz de verificar redações apenas do Enem ou generalizar para outros vestibulares/provas?
•	Um modelo pode funcionar bem para diferentes temas e gêneros de redação ou precisa ser ajustado por tipo?
•	Modelo será capaz de se adaptar ou ideal fazer um modelo para cada tipo de texto e prova?
•	Tokenização, utilizar lematização ou stemming?
•	Como lidar com erros gramaticais específicos do português, modelos em outras línguas ajudariam?
•	Quais tipos de métricas de avaliação de desempenho são mais importantes para modelos de correção de redação?
•	Como dar feedback para o aluno sem simplesmente apontar erros? Algum algoritmo pode sugerir melhorias no texto?

2.	Plano de solução

Plano de solução utilizando Processamento de Língua Natural (PLN) para a correção de provas de redação do Exame Nacional do Ensino Médio (ENEM). O processo proposto será feito pensando em atender 3 critérios: detecção de desvios nos textos, atribuição de notas, global ou por critérios de avaliação e elaboração de um feedback para o aluno.
As etapas para o desenvolvimento do projeto são descritas a seguir:

Definição do Escopo e Objetivos
Identificar as três etapas principais: detecção de desvios, atribuição de nota e feedback ao aluno, seguindo o modelo completo de Correção Automática de Redação (CAR).

Coleta e Preparação dos Dados
Reunir redações do ENEM já corrigidas e anotadas. Limpar e padronizar o texto, removendo ruídos e formatando para uma análise eficiente.
Entender o conjunto de redações, identificando a estrutura dos textos e critérios de avaliação do ENEM, incluindo a análise descritiva e estatísticas iniciais de cada competência para melhor entendimento do comportamento dos dados.

Pré-processamento dos Textos
Simplificar o texto utilizando técnicas como tokenização, lematização e remoção stopwords, visando uma estrutura adequada para extração de features e treinamento do modelo. Extrair métricas básicas, como contagem de palavras e frases, e identificar desvios ortográficos e gramaticais usando ferramentas como CoGroo e LanguageTool. Ferramentas como SpaCy e NLTK poderiam ser utilizadas para realizar o pré-processamento, tokenização, lematização, e extração de padrões no texto.

Detecção de Desvios
Implementar uma abordagem simbólica baseada em regras para identificar desvios ortográficos, gramaticais e de uso de vocabulário. Extrair features como contagem de palavras, frases, média de conectivos, entre outras. Ferramentas como LanguageTool e BERT poderiam ser utilizadas para detecção de erros ortográficos e gramaticais e verificações contextuais.

Extração de Features e Engenharia de Atributos
Criar features que representem as competências específicas do ENEM: Língua Portuguesa, Tema e Gênero, Coerência, Coesão e Proposta de Intervenção. Adicionar contagem de conectivos e variedade no uso de vocabulário para avaliar a construção textual.

Treinamento e Avaliação do Modelo de Atribuição de Nota
Utilizar modelos de redes neurais para prever as notas de cada competência. Implementar um modelo separado ou multitarefa para atribuição de nota com avaliação de acurácia. Bibliotecas como Scikit-learn e Pytorch poderiam ser utilizadas para modelagem de algoritmos de regressão e para o desenvolvimento de redes neurais para análise semântica e atribuição de notas.

Feedback Construtivo Automatizado
Desenvolver um sistema que devolva feedbacks específicos baseados nos desvios identificados, incluindo sugestões de melhoria na estrutura e gramática.

Validação e Testes
Realizar validação cruzada e testes em conjunto com corretores humanos para refinar o sistema. Coletar feedback dos usuários para melhorias.
