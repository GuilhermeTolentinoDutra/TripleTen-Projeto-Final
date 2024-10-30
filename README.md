Projeto final apresentado no Bootcamp de Data Science da TripleTen.

Tarefa:
A operadora de comunicações Interconnect gostaria de ser capaz de predizer a rotatividade de seus clientes. Se for descoberto que um usuário está planejando trocar de operadora, a empresa oferecerá-lhe códigos promocionais e opções de plano especiais. A equipe de marketing da Interconnect coletou alguns dados pessoais da sua clientela, incluindo a informação sobre seus planos e contratos.

Serviços da Interconnect

A Interconnect fornece principalmente dois tipos de serviços:

1. Telefonia fixa. O telefone pode ser conectado a várias linhas ao mesmo tempo.
2. Internet. A rede pode ser estabelecida através de uma linha telefônica (DSL, *digital subscriber line - linha digital de assinante*) ou através de um cabo de fibra óptica.

Alguns outros serviços fornecidos pela empresa incluem:

- Segurança na Internet: software de antivírus (*DeviceProtection* - proteção de dispositivos) e um bloqueador de sites maliciosos (*OnlineSecurity* - segurança online).
- Uma linha dedicada de suporte técnico (*TechSupport*).
- Armazenamento de arquivos na nuvem e backup de dados (*OnlineBackup*).
- Streaming de TV (*StreamingTV*) e um diretório de filmes (*StreamingMovies*).

Os clientes podem escolher entre fazer um pagamento mensal e assinar um contrato de 1 ou 2 anos. Eles podem usar vários métodos de pagamento e receber uma fatura eletrônica após a transação.

Planejamento:

- 1a Etapa: Importação das bibliotecas necessárias; inicialmente, bibliotecas que possibilitem a manipulação dos dados e, posteriormente, a elaboração dos modelos de machine learning que serão aplicados;
- 2a Etapa: Verificação da qualidade dos dados e ajustes que se façam necessários. Nessa etapa, serão verificados se os tipos de dados estão corretos, bem como se há dados nulos ou duplicados em cada um dos quatro conjuntos de dados disponíveis (contratos, internet, telefone e pessoal);
    - Ainda nesta fase, como pré-processamento, serão criadas duas colunas, uma relativa ao Chrurn, e outra com o tempo de duração de cada contrato, de maneira a possibilitar a extração de mais informações quando da realização da AED;
- 3a Etapa: Análise exploratória dos dados. As features serão confrontadas com as taxas de Chrun para identificar quais delas possuem maior ou menor correlação com o cancelamento de contratos;
- 4a Etapa: Conclusões que podemos tirar a partir da análise dos dados, incluídas ao final de cada análise(features categóricas e features numéricas). A partir desta etapa será possível definir quais variáveis serão úteis para os modelos e quais podem ser eliminadas.

Em seguida, passaremos para a preparação dos dados para utiliação nos modelos, fazendo as transformações eventualmente necessárias, como encoding, feature scalling.

Os modelos selecionados foram:
- Regressão Logística;
- LightGBM;
- XGBoost; e
- Random Forest Classifier.

Após o treinamento e teste dos modelos, o que obtiver os melhores resultados de acurácia e AUC ROC será selecionado e faremos um fine tunning de hiperparâmetros utilizando o Optuna, buscando melhorar ainda mais seus resultados.

Nosso objetivo é fornecer à empresa insights sobre quais grupos de cliente têm mais propensão ao cancelamento de contratos para que ela possa, então, tomar medidas com objetivo de retenção de clientes
    
