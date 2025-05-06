#### **Etapa 1: Análise e Planejamento**

- Mapear os processos e etapas.
	- Enviado para o TI (10/04/2025)
- Definir a arquitetura do sistema (ETL, banco de dados, visualização).
	- Ver o arquivo [[Estrutura da solução]]
- Documentar os requisitos e funcionalidades.
	- As funcionalidades estão descritas no arquivo [[Entendimento da Demanda]]
- **Tempo Estimado** : **1 semana (40 horas)** .

#### **Etapa 2: Desenvolvimento do Pipeline ETL**

- Extrair dados dos sistemas existentes (ex.: LECOM).
- Transformar os dados para o modelo proposto.
- Carregar os dados em um banco de dados relacional.
- Configurar o agendamento (ex.: cron jobs ou Airflow).
- **Tempo Estimado** : **2 semanas (80 horas)** .

#### **Etapa 3: Modelagem de Dados**

- Criar tabelas no banco de dados para armazenar informações sobre processos, etapas, usuários e status.
- Popular as tabelas com dados fictícios para testes.
- **Tempo Estimado** : **1 semana (40 horas)** .

#### **Etapa 4: Desenvolvimento do Dashboard**

- Criar as visualizações:
    - Gráficos de barras para mostrar processos parados em cada etapa.
    - Tabelas dinâmicas para filtrar por usuário.
- Personalizar o design com a paleta de cores da organização.
- Implementar filtros interativos (processo, usuário, etc.).
- **Tempo Estimado** : **2 semanas (80 horas)** .

#### **Etapa 5: Controle de Acesso**

- Implementar autenticação básica.
- Configurar permissões mínimas para acessar o dashboard.
- **Tempo Estimado** : **1 semana (40 horas)** .

#### **Etapa 6: Testes e Validação**

- Realizar testes de usabilidade e validação dos dados.
- Corrigir bugs e ajustar funcionalidades conforme feedback.
- **Tempo Estimado** : **1 semana (40 horas)** .

#### **Etapa 7: Implantação e Monitoramento**

- Publicar o dashboard em ambiente de produção.
- Configurar monitoramento para garantir atualizações diárias.
- **Tempo Estimado** : **1 semana (40 horas)** .

| ETAPA                           | TEMPO ESTIMADO |
| ------------------------------- | -------------- |
| Análise e Planejamento          | 1 semana       |
| Desenvolvimento do Pipeline ETL | 2 semanas      |
| Modelagem de Dados              | 1 semana       |
| Desenvolvimento do Dashboard    | 2 semanas      |
| Controle de Acesso              | 1 semana       |
| Testes e Validação              | 1 semana       |
| Implantação e Monitoramento     | 1 semana       |
**Total** : **9 semanas (360 horas)**