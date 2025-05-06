## Etapa 1: Requisitos e Análise
- Reunir mais informações sobre o LECOM (APIs disponíveis, formato dos dados, etc...).
	- Formulário de acesso ao banco de dados de homologação do LECOM
		- Enviado para a TI (10/04/2025)
	- Formulário de acesso a VPN
		- Enviado para TI (10/04/2025)
- Confirmar a paleta de cores e requisitos de design com a equipe de UX/UI.
	- Paleta de cores:
		- `Paleta 1`:
			- Paleta para trabalhar com fundo claro:
			- background: #E0DBD8
			- #923F1E
			- #B1772A
			- #0E2B51
		- `Paleta 2`:
			- Paleta para trabalhar com fundo escuro:
			- background: #292A2E
			- #1BA1AE
			- #C1E6B4
			- #FFBD59
			- #FC9437
			- #F84E50

## Etapa 2: Desenvolvimento do Pipeline ETL
- Desenvolver o script ETL para extrair, transformar e carregar os dados.
- Testar o pipeline localmente e configurar o agendamento.

## Etapa 3: Modelagem de dados
- Criar as tabelas no banco de dados.
- Popular as tabelas com dados fictícios para testes.

## Etapa 4: Criação dos Dashboards
- Desenvolver as visualizações no Metabase.
- Integrar o dashboard ao banco de dados.

## Etapa 5: Testes e Implantação
- Realizar testes de usabilidade e validação dos dados.
- Implantar o dashboard em ambiente de produção.