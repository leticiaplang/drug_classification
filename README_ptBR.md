## Drug Classification

README translated into English/US [here](https://github.com/leticiaplang/drug_classification/blob/main/README.md)

### Conteúdo & acesso
* Um projeto elaborado para fins educacionais de aplicação de modelos de classificação
* O dataset original retirado do Kaggle
* Para ter acesso ao notebook na íntegra:
  * Após abrí-lo no GitHub, clique em 'abrir com o colab'
  * Realizar a cópia por meio do Raw, salvando com formato .ipynb
  * Realizar acesso pelo link web

### Problema de Negócio
Uma das grandes dores dos serviços de saúde são os erros relacionados a medicamentos. De acordo com o [artigo](https://www.ncbi.nlm.nih.gov/books/NBK519065/) de Rayhan A. e colegas, os erros de pescrição e solicitação englobam 50% dos erros totais relacionamentos a medicamentos. O dano não ocorre apesas ao paciente, familiar ou aos profissionais, mas também à própria empresa, uma vez que são estimados gastos maiores a 40 bilhões de dólares por ano para o cuidado desses pacientes.
Este algoritmo é o primeiro passo para a construção de um MVP (produto mínimo viável) visando auxílio para prescrição de medicamentos segura. Após, será realizada análise de dose, juntamente com a análise em uma amostra de tamanho maior.

### Objetivo
* Buscar insigths sobre os fatores que auxiliam na escolha da droga a partir da análise exploratória dos dados (associação e correlação)
* Construir um modelo classifcatório que utilize as features e consiga prever adequadamente a recomendação do tipo de droga para tratamento

### Características do dataframe

* Ele possui 200 linhas e 6 colunas
* Não foram identificados dados inconsistentes
* As variáveis numéricas são: 
   - Age | idade: 15 to 74 anos
   - Na to Potassium Ratio | razão sódio e potássio: 6.269 - 38.247mEq/24 horas | Exame de urina | Altas razão significa consumo elevado de Sodio e menor de Potássio.
* As variáveis categóricas são:
   - Sex | sexo: F(feminino), M(masculino)
   - Blood Pressure Levels (BP) | pressão arterial: normal, baixa, alta
   - Cholesterol Levels | colesterol: normal, alto | exame de sangue
   - Drug | droga: a, b, c, x, y

### Método exploratório
* Uso de histograma, boxplot, IQR, countplot e scatterplot

### Método Modelagem
Alvo: 
* Drug | droga

Atributos contínuos: 
* Age|idade 
* Na_to_K|razão Na e K

Atributos categóricos: 
* Sex | sexo
* BP | pressão arterial
* Cholesterol | colesterol

* Utilizado label encoder nas features categóricas
* Criada três funções: criação de cenários de modelagem, rodar modelos conforme os cenários e outra para gerar gráficos das métricas de performance
* Métricas de performance: acurácia (principal), precisão, recall, F1-score
* Modelos analisados: dummy classifier, regressão logística, KNN, árvore de decisão, random forest


### Conclusões
1) Modelo
* Baseline foi Dummy Classifier: acurácia de 0.5
* Melhor performance foi com regressão logística: acurácia de 0.89
* Árvore de decisão e random forest provavelmente com overfitting
* Podemos mostrar um MVP com regressão logística

2) Insights
Age | idade: 
* Droga A utilizada para menores de 50 anos
* Droga B utilizada para maiores de 50 anos

BP | pressão arterial: 
* Droga A e droga B para pessoa com pressão alta
* Droga C para pessoas com pressão normal
* Droga X para pessoas com pressão normal ou baixa 

Cholesterol | colesterol:
* Uso de C para pessoas com colesterol elevado

Na to K:
* Droga Y utilizada se razão for maior que 15mEq/24 horas

Sexo: Feature não relevante? 

### Próximos passos:
* Tunnig da árvore de decisão e random forest, incluindo análise de overfitting.
* Calcular ANOVA para ver quais features são mais relevantes para o modelo.
* Aplicar balanceamento dos dados, exemplo SMOTE.
* Assim que possível, inserir análise das doses para buscarmos maior granularidade dos dados e segurança no apoio à precrição dos medicamentos.
