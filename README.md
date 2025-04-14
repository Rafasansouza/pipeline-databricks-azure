# 📊 Pipeline de Dados com Azure Databricks e Data Factory

Este projeto demonstra a criação e orquestração de pipelines de dados na nuvem utilizando o **Azure Databricks** e o **Azure Data Factory (ADF)**. O objetivo é ilustrar como essas ferramentas podem ser integradas para orquestrar transformações e cargas de dados em um ambiente escalável na nuvem.

## 🚀 Visão Geral

A solução desenvolvida envolve:

- **Azure Data Factory**: Responsável pela orquestração das tarefas ETL, agendamento de execuções e gerenciamento do fluxo dos dados.
- **Azure Databricks**: Utilizado para o processamento e transformação de dados, com notebooks escritos em **Scala**, linguagem principal do projeto.

> 📝 Também foram incluídas versões dos notebooks em **Python** com o propósito de demonstrar familiaridade com a linguagem, embora a execução original tenha sido realizada em Scala.

## 🛠️ Tecnologias Utilizadas

- [Azure Data Factory](https://azure.microsoft.com/pt-br/services/data-factory/)
- [Azure Databricks](https://azure.microsoft.com/pt-br/services/databricks/)
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

1. **Provisionamento de Recursos**:
   - Crie um workspace no **Azure Databricks**.
   - Configure uma instância do **Azure Data Factory**.

2. **Importação dos Artefatos**:
   - Importe os notebooks Scala no seu workspace do Databricks.
   - Configure os pipelines, triggers e linked services no ADF.

3. **Atualização das Conexões**:
   - Atualize os arquivos de `linkedService` com suas credenciais e parâmetros específicos do ambiente Azure.

4. **Execução da Pipeline**:
   - Inicie a execução dos pipelines pelo ADF. Os notebooks Scala serão acionados conforme definido na orquestração.

## 💡 Demonstrações com Python

Embora a execução real tenha sido feita em Scala, este repositório também inclui notebooks com a tradução dos scripts para Python, como forma de demonstrar conhecimento na linguagem e aumentar a portabilidade do projeto.

## 📌 Observações

- Certifique-se de configurar as permissões apropriadas no Databricks e no Data Factory.
- Este projeto serve tanto como material de estudo quanto como demonstração prática de habilidades em engenharia de dados com serviços Azure.

## 🤝 Colaboração

Este projeto foi desenvolvido em conjunto com a [Alura](https://www.alura.com.br/), como parte de estudos e práticas avançadas em engenharia de dados com a plataforma Azure.

---

📬 Fique à vontade para abrir *issues* ou sugestões no repositório!

