## Drug Classification

README translated into English/US [here](https://github.com/leticiaplang/drug_classification/blob/main/README.md)

### Estrutura do projeto
- README.md
- README_ptBR.md
- drug_classification.ipynb (notebook)
- drug_200.csv (dataset)


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

### Estrutura do Notebook (está em inglês)
* Preparando o ambiente
  - Instalações
  - Importações
  - Requisitos
  - Importação do dataset e transformação dele em dataframe
* Exploração do dataframe
  - Característica do dataframe
  - Transformações
  - Anaálise exploratória
  - Distribuição e balanceamento
  - análise de outlier
* Insights de negócio
* Modelagem
  - Engenharia de atributos
  - Definição de funções 
  - Criando cenários
  - Testando os cenários
* Conclusão e próximo passos
* Referências

### Ambiente
* Python
* Pandas
* Numpy
* Matplotlib
* Seaborn
* Warnings
* Sklearn
* Imbelarn
