## Arquitetura Proposta
### Camada de dados:
`Fonte de dados`: O LECOM será a fonte principal de dados. Precisaremos extrair informações sobre processos, etapas e usuários.

`Modelagem`: Criar um modelo de dados que consolide as informações necessárias:
	- Tabela **processos**: Contém informações sobre os processos (ID, nome, fluxo, etc.).
	- Tabela **etapas**: Detalha as etapas de cada processo (ID, descrição, status, etc.).
	- Tabela **usuários**: Informações sobre os usuários responsáveis por processos/etapas.
	- Tabela **status**: Relaciona processos, etapas e seus respectivos status (em execução, etc.).

### Camada de Processamento:
`ETL (Extract, Transform, Load)`: Desenvolver uma pipeline ETL para extrair dados do LECOM, transformá-lo conforme o modelo proposto e carregá-los em um banco de dados relacional.

`Agendamento`: Configurar a pipeline para rodar automaticamente à noite, garantindo que os dados estejam atualizados diariamente.

### Camada de visualização:
`Ferramenta de Dashboard`: Utilizar uma ferramenta como o Metabase para criar o dashboard interativo.

`Interface Amigável`: Garantir que os filtros e visualizações sejam intuitivos e fáceis de usar.

#### Funcionalidades do Dashboard:
`Visão por Processo e Etapas`:
	- Filtro para selecionar o processo desejado.
	- Gráfico de barras ou tabela mostrando as etapas e a quantidade de processos parados em cada uma.
`Visão por usuário`:
	- Filtro para selecionar o usuário (papel).
	- Gráfico ou tabela mostrando os processos atribuídos ao usuário e suas respectivas etapas.
`Controle de Acesso`:
	- Implementar autenticação básica para restringir o acesso ao dashboard.
	- Garantir que apenas usuários autorizados possas visualizar os dados.
`Design e Paleta de Cores`:
	- Personalizar o dashboard com a paleta de cores da organização.
	- Usar gráficos claros legíveis, com ênfase na usabilidade.

#### Tecnologias Sugeridas:
`Extração e Processamento de Dados`:
	- Python: Para desenvolver o pipeline ETL.
	- SQL: Para consultas e modelagem no banco de dados.
	- Cron jobs ou Apache Airflow: Para agendar a execução do ETL.
`Armazenamento de dados`:
	- PostgreSQL: Banco de dados relacional para armazenar os dados consolidados.
`Visualização`:
	- Metabase: Opção mais leve e open-source.