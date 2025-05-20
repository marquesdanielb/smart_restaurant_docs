## Dados do Usuário
Aqui está um json de dados fictícios para a criação dos gráficos:
``` Json
  {

    id: "user1",

    name: "Ana Silva",

    role: "Analista de IPTU",

    totalBlocked: 24,

    totalBlockedMoreThan6Months: 5,

    totalBlockedMoreThan3Months: 12,

    totalBlockedMoreThan1Month: 18,

    processSteps: [

      { 
	      process: "Certidão de Matrícula do Imóvel", 
	      step: "Assumir Análise de Fiscalização", 
	      blocked: 8, 
	      status: "open", 
	      blockedDays: 45 
	  },

      { 
	      process: "Certidão de Matrícula do Imóvel", 
	      step: "Analisar Fiscalização", 
	      blocked: 5, 
	      status: "open", 
	      blockedDays: 30 
	  },

      { 
	      process: "Atualização Cadastral", 
	      step: "Assumir Atividade", 
	      blocked: 4, 
	      status: "closed", 
	      blockedDays: 0 
	  },

      { 
	      process: "Atualização Cadastral", 
	      step: "Responder Solicitação", 
	      blocked: 3, 
	      status: "open", 
	      blockedDays: 120 
	  },

      { 
	      process: "Transferência de Propriedade", 
	      step: "Analisar Impugnação", 
	      blocked: 4, 
	      status: "open", 
	      blockedDays: 190 
	  },

    ],

  },
```

## Dados do Grupo
Aqui está um json de dados fictícios para a criação dos gráficos:
``` Json
  {

    id: "proc1",

    name: "Certidão de Matrícula do Imóvel",

    processNumber: "PROC-2023-0001",

    currentUser: "Maria Silva",

    blockedDays: 195,

    totalBlocked: 35,

    inRequirement: true,

    requirementDays: 42,

    openDays: 76,

    openingDate: getRandomDate(new Date(2020, 0, 1), new Date(2023, 11, 31)),

    currentStep: "Analisar Fiscalização",

    steps: [

      { 
	      name: "Assumir Análise de Fiscalização", 
	      blocked: 15, 
	      percentage: 42.9, 
	      avgBlockedDays: 210 
	  },

      { 
	      name: "Analisar Fiscalização", 
	      blocked: 8, 
	      percentage: 22.9, 
	      avgBlockedDays: 120 
	  },

      { 
	      name: "Analisar Retorno da Exigência", 
	      blocked: 7, 
	      percentage: 20, 
	      avgBlockedDays: 75 
	  },

      { 
	      name: "Analisar Penalidade", 
	      blocked: 5, 
	      percentage: 14.2, 
	      avgBlockedDays: 65 
	  },

    ],

  },
```
