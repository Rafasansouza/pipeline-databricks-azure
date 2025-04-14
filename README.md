# 📊 Pipeline de Dados com Azure Databricks e Data Factory


Este projeto demonstra a criação e orquestração de pipelines de dados na nuvem utilizando o **Azure Databricks**, o **Azure Data Factory (ADF)** e o **Azure Data Lake Storage (ADLS)**. O objetivo é ilustrar como essas ferramentas podem ser integradas para orquestrar transformações e cargas de dados em um ambiente escalável na nuvem.

## 📝 Descrição do projeto

Nós, como engenheiros de dados de uma empresa do setor imobiliário, fomos responsáveis por desenvolver um pipeline completo de engenharia de dados. A proposta do projeto é estruturar um Data Lake, iniciar a ingestão dos dados de imóveis na camada de entrada (inbound) e, a partir disso, aplicar as transformações necessárias para evoluí-los através das camadas bronze e silver dentro do lake.

Além do processamento, também é fundamental garantir que esse pipeline seja executado automaticamente em intervalos regulares — neste caso, a cada hora — assegurando que os dados estejam sempre atualizados e prontos para uso.

### Ferramentas utilizadas na empresa

A empresa trabalha com o ecossistema de nuvem da Azure, utilizando o Azure Databricks como ambiente principal para o desenvolvimento e execução dos notebooks. Toda a manipulação e transformação dos dados foi feita em Scala, linguagem oficial do projeto. Para a orquestração e agendamento das execuções, utilizamos o Azure Data Factory, o que nos permitiu montar uma solução automatizada, escalável e integrada na nuvem.

## 🚀 Visão Geral

A solução desenvolvida envolve:

- **Azure Data Factory**: Responsável pela orquestração das tarefas ETL, agendamento de execuções e gerenciamento do fluxo dos dados.
- **Azure Databricks**: Utilizado para o processamento e transformação de dados, com notebooks escritos em **Scala**, linguagem principal do projeto.
- **Azure Data Lake Storage (Gen2)**: Repositório utilizado para armazenar os dados brutos e transformados de forma estruturada e escalável.

> 📝 Também foram incluídas versões dos notebooks em **Python** com o propósito de demonstrar familiaridade com a linguagem, embora a execução original tenha sido realizada em Scala.

## 🛠️ Tecnologias Utilizadas

- [Azure Data Factory](https://azure.microsoft.com/pt-br/services/data-factory/)
- [Azure Databricks](https://azure.microsoft.com/pt-br/services/databricks/)
- [Azure Data Lake Storage Gen2](https://learn.microsoft.com/pt-br/azure/storage/data-lake-storage/)
- [Apache Spark](https://spark.apache.org/) com linguagem **Scala**
- [Scala](https://www.scala-lang.org/)
- [Python](https://www.python.org/) *(demonstrativo complementar)*

## 📁 Estrutura do Repositório

```bash
pipeline-databricks-azure/
├── factory/                # Artefatos do Azure Data Factory (pipelines, triggers)
├── linkedService/          # Configurações de conexões (Linked Services)
├── notebooks/
│   ├── scala/              # Notebooks executados em Scala
│   └── python/             # Notebooks traduzidos para Python (demonstração)
├── pipeline/               # Pipelines do ADF
├── trigger/                # Triggers de execução (agendamento)
├── publish_config.json     # Configuração de publicação do ADF
├── .gitignore              # Arquivos e pastas ignoradas pelo Git
└── README.md               # Documentação do projeto
```

## ⚙️ Como Executar

### 1. Provisionamento de Recursos no Azure

- **Grupo de Recursos**: Crie um grupo de recursos para organizar todos os serviços relacionados.
- **Azure Data Lake Storage Gen2**: Configure uma conta de armazenamento para armazenar os dados brutos e processados.
- **Azure Databricks**: Crie um workspace para desenvolvimento e execução dos notebooks.
- **Azure Data Factory**: Configure uma instância para orquestração dos pipelines.

### 2. Configuração do Azure Data Factory (ADF)

- **Linked Services**: Defina conexões com o Azure Databricks e o Azure Data Lake Storage.
- **Datasets**: Configure os conjuntos de dados que serão utilizados nos pipelines.
- **Pipelines**: Crie os pipelines que orquestrarão as tarefas de ETL.
- **Triggers**: Estabeleça gatilhos para execução automática dos pipelines conforme necessidade.

### 3. Desenvolvimento no Azure Databricks

- **Importação de Notebooks**: Importe os notebooks desenvolvidos em Scala para o workspace do Databricks.
- **Configuração de Clusters**: Configure os clusters necessários para execução dos notebooks.
- **Testes Locais**: Realize testes locais para validar o funcionamento dos notebooks antes da integração com o ADF.

### 4. Integração entre ADF e Databricks

- **Atividades de Notebook**: No ADF, adicione atividades que executem os notebooks do Databricks dentro dos pipelines.
- **Parâmetros**: Configure parâmetros necessários para a execução dinâmica dos notebooks.
- **Validação**: Teste a integração para garantir que os notebooks sejam executados corretamente via ADF.

### 5. Execução e Monitoramento

- **Execução dos Pipelines**: Inicie a execução dos pipelines manualmente ou via triggers configurados.
- **Monitoramento**: Utilize as ferramentas de monitoramento do ADF para acompanhar a execução e identificar possíveis falhas.
- **Logs e Diagnóstico**: Analise os logs gerados para diagnóstico e resolução de problemas.

### 6. Manutenção e Atualizações

- **Versionamento**: Utilize o GitHub para versionar os notebooks e pipelines, facilitando o controle de mudanças.
- **Documentação**: Mantenha a documentação atualizada para facilitar futuras manutenções e onboarding de novos colaboradores.
- **Melhorias Contínuas**: Avalie constantemente o desempenho dos pipelines e notebooks, implementando melhorias conforme necessário.


## 💡 Demonstrações com Python

Embora a execução real tenha sido feita em Scala, este repositório também inclui notebooks com a tradução dos scripts para Python, como forma de demonstrar conhecimento na linguagem e aumentar a portabilidade do projeto.

## 📌 Observações

- Certifique-se de configurar as permissões apropriadas no Databricks e no Data Factory.
- Este projeto serve tanto como material de estudo quanto como demonstração prática de habilidades em engenharia de dados com serviços Azure.

## 🤝 Colaboração

Este projeto foi desenvolvido em conjunto com a [Alura](https://www.alura.com.br/), como parte de estudos e práticas avançadas em engenharia de dados com a plataforma Azure.

---

📬 Fique à vontade para abrir *issues* ou sugestões no repositório!

