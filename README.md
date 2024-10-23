# Projeto Final - Análise e Transformação de Dados com Google Cloud, AWS e Azure

## Descrição do Projeto

Este projeto integra o trabalho final do Bootcamp de Analista de Dados da SoulCode Academy, realizado entre 05/08/2024 e 25/10/2024. Seu objetivo é analisar, transformar e visualizar dados utilizando plataformas de nuvem como Google Cloud, AWS, Azure, além do MongoDB Atlas para o armazenamento de dados NoSQL. O foco está no desenvolvimento de um pipeline de dados robusto, que combina diversas ferramentas de nuvem para criar visualizações interativas que respondam a perguntas-chave de negócios.

A estrutura do projeto segue o modelo ETL (Extração, Transformação e Carga), partindo da coleta de dados no Google Cloud Platform (GCP), com AWS e Azure como plataformas complementares. Os dados foram inicialmente armazenados no Google Cloud Storage, com suporte de serviços como AWS S3 e Azure Blob Storage, e o processamento ocorreu em instâncias MySQL (Google Cloud SQL, AWS RDS e Azure SQL Database).

Após o processamento, os dados tratados foram carregados em ferramentas de visualização, gerando análises detalhadas e insights relevantes para decisões de negócios. O projeto destaca o uso eficaz de múltiplas plataformas de nuvem, permitindo um fluxo de trabalho de dados eficiente e escalável, essencial para atender às demandas de análise de grandes volumes de dados.

## Stacks Utilizadas no Processo

### **Cloud Computing**
![Google Cloud](https://img.shields.io/badge/Google%20Cloud-4285F4?style=for-the-badge&logo=google-cloud&logoColor=white)
![AWS](https://img.shields.io/badge/Amazon%20AWS-232F3E?style=for-the-badge&logo=amazon-aws&logoColor=white)
![Azure](https://img.shields.io/badge/Microsoft%20Azure-0078D4?style=for-the-badge&logo=microsoft-azure&logoColor=white)

### **Banco de Dados**
![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=for-the-badge&logo=mongodb&logoColor=white)

### **Ferramentas de Análise**
![Google Colab](https://img.shields.io/badge/Google%20Colab-F9AB00?style=for-the-badge&logo=googlecolab&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Power BI](https://img.shields.io/badge/Power%20BI-F2C811?style=for-the-badge&logo=power-bi&logoColor=black)

### **Controle de Versão**
![Git](https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white)
![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)
![Bitbucket](https://img.shields.io/badge/Bitbucket-0052CC?style=for-the-badge&logo=bitbucket&logoColor=white)

## Estrutura do Projeto

### Etapa 01: Configuração de Infraestrutura

### Google Cloud Platform (GCP)

- **Criação do Bucket no Google Cloud Storage**:

  ![Criação do Bucket no GCP](./squad03/images/gcp_bucket_creation.png)

- **Big Query Google Cloud Storage**:

  ![Criação do Bucket no GCP](./squad03/images/gcp_big_query_creation.png)

- **Criação da Instância MySQL no Google Cloud SQL**:

  ![Criação do MySQL no GCP](./squad03/images/gcp_mysql_instance.png)

### AWS

- **Criação do Bucket no AWS S3**:

  ![Criação do Bucket no AWS S3](./squad03/images/aws_s3_bucket.png)

- **Criação da Instância MySQL no AWS RDS**:

  ![Criação do MySQL no AWS RDS](./squad03/images/aws_rds_mysql.png)

### Azure

- **Criação do Blob Storage no Azure**:

  ![Criação do Blob Storage no Azure](./squad03/images/azure_blob_storage.png)

- **Criação da Instância SQL no Azure SQL Database**:

  ![Criação do MySQL no Azure SQL Database](./squad03/images/azure_sql_database.png)

### Arquivos relacionados:

- **Modelo Entidade Relacionamento (MER)**:

  ![Modelo Entidade Relacionamento (MER)](./squad03/images/modelo_entidade_relacionamento.jpg)

- **Banco de Dados Não Relacional**:

  ![MongoDB Atlas](./squad03/images/mongodb_atlas.png)

## Etapa 02: Extração, Transformação e Carga (ETL)

O grupo utilizou notebooks Colab para executar o processo de ETL (Extração, Transformação e Carga) dos dados. A extração dos dados foi realizada tanto a partir do Google Cloud Storage quanto do Google Cloud SQL para demonstrar o uso de ambas as ferramentas. Após a extração, os dados passaram por um processo de limpeza e transformação, que incluiu:

- Remoção de valores nulos
- Criação de novas colunas derivadas
- Agregação de dados

## Etapa 03: Carregamento dos Dados Tratados

Após o processo de transformação, os dados foram carregados em três destinos diferentes:

1. **Google BigQuery**: Usado para armazenar grandes volumes de dados e realizar consultas de alta performance.
2. **Google Cloud Storage**: Os dados tratados foram armazenados em um novo bucket dentro da pasta `dados processados`.
3. **MongoDB Atlas**: Uma cópia dos dados tratados foi inserida no MongoDB Atlas para explorar a possibilidade de consultas flexíveis em um banco de dados NoSQL.

## Etapa 04: Visualização de Dados

Os dados tratados foram conectados à ferramenta de visualização de dados **Power BI**, onde foram criados **dashboards** para responder às perguntas de negócios definidas pelo grupo. Entre as análises mais relevantes, destacamos a seguinte:

### Quais os veículos que mais contribuíram para os fretes?

Nesta análise, o objetivo foi identificar quais veículos tiveram maior impacto nas operações de frete. Para isso, foram utilizadas as seguintes métricas:

- **Quantidade de Fretes por Veículo:** Avaliação do número total de fretes realizados por cada veículo.
- **Receita Total Gerada por Veículo:** O somatório de todas as receitas geradas pelos fretes associados a cada veículo.
- **Distância Total Percorrida por Veículo (km):** Total de quilômetros rodados por cada veículo, permitindo correlacionar eficiência e contribuição ao volume de fretes.
- **Custo Operacional por Veículo (R$):** Cálculo dos custos operacionais de cada veículo, considerando combustível, manutenção e outros custos fixos, para identificar a relação entre custos e receita gerada.
- **Contribuição Percentual por Veículo:** Identifica o percentual de contribuição de cada veículo no total de fretes realizados pela frota.

Com essas métricas, foi possível identificar os veículos com maior relevância nas operações de frete, permitindo uma gestão mais eficiente e estratégias de otimização de rotas e custos.

### Imagens relacionadas a parte de visualização:

- **Conexão do PowerBI com o Big Query do GCP**:

  ![Conexão PowerBI](./squad03/images/powerbi_connection.png)

- **Desenvolvimento dos DashBoards PowerBI**:

  ![Desenvolvimento DashBoard PowerBI](./squad03/images/powerbi_development_process.png)

- **DashBoard Final PowerBI - Página Custos Operacionais em Destaque**:

  ![Dashboard Final PowerBI](./squad03/images/powerbi_dashboard.png)

## Etapa 05: Aplicação do Algoritmo K-Means

O algoritmo K-Means foi aplicado para realizar a clusterização dos clientes, visando identificar grupos com padrões semelhantes de comportamento de demanda de fretes. O objetivo principal é segmentar os clientes com base em características como o número de fretes solicitados e o valor total dos fretes. Essa análise permite uma melhor compreensão dos perfis de clientes e pode auxiliar na tomada de decisões estratégicas relacionadas à logística e ao planejamento de operações.

## Como Rodar o Projeto Localmente

### Requisitos:

- Conta no Google Cloud, AWS e Azure.
- Google Colab ou Jupyter Notebook para execução dos scripts.
- Python 3.x e pacotes necessários (ver `requirements.txt`).

### Instalação

1. Clone o repositório:
   ```bash
   git clone https://github.com/seu_usuario/projeto_final_grupo.git
   cd projeto_final_grupo
   ```
2. Instale as dependências:
   ```bash
   pip install -r requirements.txt
   ```
3. Configure suas credenciais do Google Cloud, AWS e Azure:
   3. Configure suas credenciais do Google Cloud, AWS, Azure e bancos de dados:
   ```bash
   export GOOGLE_APPLICATION_CREDENTIALS="/path/to/your/google-service-account.json"
   export AWS_ACCESS_KEY_ID="your_aws_access_key"
   export AWS_SECRET_ACCESS_KEY="your_aws_secret_key"
   export AZURE_STORAGE_ACCOUNT="your_azure_account"
   export SQL_SERVER_USERNAME="your_sql_server_username"
   export SQL_SERVER_PASSWORD="your_sql_server_password"
   export SQL_SERVER_HOST="your_sql_server_host"
   export SQL_SERVER_DATABASE="your_sql_server_database"
   export MYSQL_USER="your_mysql_username"
   export MYSQL_PASSWORD="your_mysql_password"
   export MYSQL_HOST="your_mysql_host"
   export MYSQL_DATABASE="your_mysql_database"
   ```

### Instruções:

- Siga as instruções no notebook Colab para realizar as etapas de ETL.
- Utilize os scripts fornecidos para a configuração de buckets e bancos de dados no GCP, AWS e Azure.
- Os dashboards finais podem ser visualizados no Power BI através do seguinte link: [Power BI Dashboard](https://app.powerbi.com/view?r=eyJrIjoiMzU4OGFiOTAtMTAxYy00ZTRjLTg2MDctOGFjNzQ5MGJhYmZlIiwidCI6ImI1OTYwNjZkLWE0YzgtNDQ1Zi04OTk2LTgwMzA5ZDlkYjQzYiJ9&pageName=34ea0270d3772415684b).

### Contribuições:

## Este projeto foi desenvolvido em colaboração por:

- **Luan Galvão** - Contribuiu no ETL, criação do banco MYSQL, estrutura GCP e BigQuery.  
  ![GitHub](https://img.shields.io/badge/GitHub-luangalvaoxD-181717?style=for-the-badge&logo=github)  
  [https://github.com/luangalvaoxD](https://github.com/luangalvaoxD)

- **Lenaldo Matias** - Contribuiu no ETL, criação do banco MYSQL, estrutura GCP e BigQuery.  
  ![GitHub](https://img.shields.io/badge/GitHub-LenaldoMatias-181717?style=for-the-badge&logo=github)  
  [https://github.com/LenaldoMatias](https://github.com/LenaldoMatias)

- **Eloisa G. D. Oliveira** - Contribuiu no ETL, criação do banco MYSQL, estrutura GCP e BigQuery.  
  ![GitHub](https://img.shields.io/badge/GitHub-eloisagdo04-181717?style=for-the-badge&logo=github)  
  [https://github.com/eloisagdo04](https://github.com/eloisagdo04)

- **Márcio Aquilles Monteles Silva** - Contribuiu com a codificação MongoDB, AWS, Azure, K-Means e Documentação.  
  ![GitHub](https://img.shields.io/badge/GitHub-MarcioAquilles-181717?style=for-the-badge&logo=github)  
  [https://github.com/marcioaquilles](https://github.com/marcioaquilles)

- **Larissa Cerqueira** - Contribuiu no processo de análise, visualização de dados e criação dos Dashboards.  
  ![GitHub](https://img.shields.io/badge/GitHub-larissafcerqueira-181717?style=for-the-badge&logo=github)  
  [https://github.com/larissafcerqueira](https://github.com/larissafcerqueira)

- **Helen Ribeiro** - Contribuiu no processo de análise, elaboração das métricas e KPIs, e visualização de dados.  
  ![LinkedIn](https://img.shields.io/badge/LinkedIn-helenribeiro--dados-0077B5?style=for-the-badge&logo=linkedin)  
  [https://www.linkedin.com/in/helenribeiro-dados/](https://www.linkedin.com/in/helenribeiro-dados/)


## Licença

Este projeto está licenciado sob a Licença MIT - veja o arquivo [LICENSE](LICENSE) para mais detalhes.

![MIT License](https://img.shields.io/badge/License-MIT-yellow.svg)

## Contato

Para dúvidas ou mais informações sobre o projeto, entre em contato com o grupo através dos seguintes e-mails:

- **Helen Ribeiro**: [helenribeiro@gmail.com](mailto:helenribeiro@gmail.com)
- **Larissa Cerqueira**: [lrs.cerqueira@gmail.com](mailto:lrs.cerqueira@gmail.com)
- **Luan Galvão**: [luanestudos98@gmail.com](mailto:luanestudos98@gmail.com)
- **Eloisa G. D. Oliveira**: [eloisagomesdeoliveira6@gmail.com](mailto:eloisagomesdeoliveira6@gmail.com)
- **Márcio Aquilles Monteles Silva**: [marcioaquilles@gmail.com](mailto:marcioaquilles@gmail.com)
- **Lenaldo Matias**: [lenaldomatias@gmail.com](mailto:lenaldomatias@gmail.com)
