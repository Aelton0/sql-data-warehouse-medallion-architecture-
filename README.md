Projeto de Data Warehouse e Analytics com Arquitetura Medallion
Este projeto demonstra uma solução completa de Data Warehouse e Analytics, utilizando a arquitetura Medallion (Bronze, Silver e Gold) para transformar dados brutos em insights acionáveis para Business Intelligence e Machine Learning.

🏗️ Visão Geral da Arquitetura:

A arquitetura segue o padrão Medallion dividido em três camadas principais:
<img width="697" height="456" alt="image" src="https://github.com/user-attachments/assets/ec0b2051-93dd-4448-b898-790f6d2e82c6" />

🔸 Camada Bronze – Dados Brutos:
- Fonte: Arquivos CSV extraídos de sistemas ERP e CRM.
- Interface de ingestão: Arquivos via processo batch.
- Tipo de objeto: Tabelas.
- Processamento: Truncar e inserir (Full Load).
- Transformação: Nenhuma.
- Modelagem: Nenhuma.
  
🔹 Camada Prata – Dados Limpos e Padronizados:
- Transformações aplicadas: Limpeza, padronização, normalização, enriquecimento dos dados.
- Tipo de objeto: Tabelas.
- Processamento: Batch, truncar e inserir.
- Modelagem: Nenhuma.
  
🟡 Camada Ouro – Dados para Consumo:
- Transformações aplicadas: Integração, agregação e lógica de negócio.
- Tipo de objeto: Views.
- Modelagem: Star Schema, Tabela Agregada, Flat Table.
- Objetivo: Preparar dados para consumo por BI, consultas SQL ad-hoc e modelos de Machine Learning.
- 
📊 Consumo dos Dados:
Os dados da camada ouro são utilizados para:
- Business Intelligence e Dashboards
- Consultas SQL Ad-hoc
- Modelos de Machine Learning
  
⚙️ Componentes do Projeto:
- ETL Pipelines: Scripts SQL para ingestão, transformação e modelagem.
- Modelagem de Dados: Criação de tabelas fato e dimensões otimizadas para análise.
- Ferramentas utilizadas:
- SQL Server Express
- SQL Server Management Studio (SSMS)
- DrawIO para diagramas
- GitHub para versionamento
- Notion para gerenciamento de tarefas
  
📁 Estrutura do Repositório:
sql-data-warehouse-medallion-architecture-/
├── datasets/              # Dados brutos (ERP e CRM)
├── docs/                  # Documentação e diagramas
│   ├── data_flow.drawio   # Diagrama de fluxo de dados
│   ├── data_models.drawio # Modelagem dimensional
│   └── naming-conventions.md
├── scripts/
│   ├── bronze/            # Scripts de ingestão
│   ├── silver/            # Scripts de transformação
│   └── gold/              # Scripts de modelagem analítica
├── tests/                 # Scripts de validação
├── README.md              # Visão geral do projeto
└── requirements.txt       # Dependências


🎯 Objetivos do Projeto
Engenharia de Dados:
- Consolidar dados de ERP e CRM em um Data Warehouse moderno.
- Resolver problemas de qualidade e padronização.
- Integrar fontes em um modelo analítico único.
Análise de Dados:
- Gerar insights sobre comportamento de clientes, desempenho de produtos e tendências de vendas.
- Suportar decisões estratégicas com dados confiáveis e bem modelados.
  
📜 Licença
Este projeto está licenciado sob a Licença MIT. Livre para uso, modificação e compartilhamento com atribuição adequada.
