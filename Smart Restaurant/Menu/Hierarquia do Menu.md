Entidades envolvidas na hierarquia do Menu:
# Menu
Representa o nível mais alto da hierarquia, abrangendo as categorias principais de itens que o restaurante oferece.

**Exemplos:**
- Cardápio Oficial
- Cardápio de Drinks
- Carta de Vinhos, Whisky e Licores
- Menu de Sobremesas
- Promoções da Semana

**Observações:**
- Um restaurante pode ter *múltiplos menus ativos simultaneamente*.
- O Menu serve como um agrupador lógico para as seções e itens do cardápio.

# *Um Menu contém* Grupos de Menus
Dentro de um Menu, encontramos os Grupos de Menus, que representam *conjuntos menores e mais específicos de itens relacionados*. Eles ajudam a organizar o cardápio em categorias mais fáceis de navegar para o cliente.

**Exemplo:**
Considerando o "Cardápio Oficial", podemos ter os seguintes Grupos de Menus:

- Petiscos Tradicionais
- Petiscos de Frango
- Acompanhamentos de Aipim
- Pratos Principais (Carne, Frango, Peixe)
- Massas
- Saladas

**Observações:**
- Um Menu pode conter um ou mais Grupos de Menus.
- Os Grupos de Menus facilitam a estruturação lógica do cardápio.

# *Um Grupo de Menu contém* itens do Menu
Dentro de um Grupo de Menu, encontramos os Itens do Cardápio. Estes representam os produtos ou serviços individuais que o restaurante oferece para venda. Cada item possui detalhes específicos, como nome, descrição, preço e, possivelmente, variações.

**Exemplo:**
Considerando o Grupo de Menu "Petiscos Tradicionais", alguns Itens de Menu poderiam ser:

- Gorjão de Peixe
- Casquinha de Siri
- Bolinho de Bacalhau (unidade)
- Pastel de Queijo (porção com 6)

**Observações:**
- Um Grupo de Menu *contém um ou mais Itens de Menu*.
- Os Itens de Menu são os elementos finais que os clientes podem selecionar e adicionar ao seu pedido.

# Modificadores
Os Modificadores são opções adicionais que podem ser aplicadas a Grupos de Menu e Itens de Menu, permitindo a personalização dos pedidos pelos clientes. Eles oferecem flexibilidade para adaptar os itens às preferências individuais.

**Exemplo de Modificador aplicado a um Item de Menu:**
Considere o Item de Menu "_Camarão à Milanesa_". Podemos atribuir a ele um Grupo de Modificadores chamado "_Queijos Adicionais_". Dentro desse grupo, teríamos opções como:

- Queijo Catupiry (adicionar)
- Queijo Mussarela (adicionar)
- Queijo Parmesão Ralado (adicionar)

Assim, ao selecionar "_Camarão à Milanesa_", o cliente poderia escolher adicionar "_Queijo Catupiry_" ao seu prato.

**Herança de Grupos de Modificadores:**
Ao atribuir um _Grupo de Modificadores_ a um _Grupo de Menus_, por padrão, todos os Itens de Menu dentro desse grupo herdarão as opções de modificação. Isso simplifica a aplicação de modificadores comuns a vários itens. No entanto, essa herança pode ser desabilitada para Itens de Menu específicos dentro do grupo, oferecendo controle granular.

**Exemplo de Herança e Modificadores Individuais:**
Considere o Grupo de Menu "_Batata_". Podemos atribuir a ele um Grupo de Modificadores chamado "_Tipo de Batata_", com opções como:

- Simples
- Gratinada
- À Dom Manolo

Agora, vamos considerar um Item de Menu específico dentro desse grupo: "_Batata Gratinada_". Além de herdar as opções do "_Tipo de Batata_", podemos adicionar Modificadores específicos a este item, como:

- Adicionar Queijo Prato
- Adicionar Queijo Parmesão e Bacon
- Adicionar Alho, Bacon e Calabresa

Nesse caso, ao selecionar "_Batata Gratinada_", o cliente teria as opções herdadas ("Simples", "Gratinada", "À Dom Manolo") e as opções específicas do item ("Adicionar Queijo Prato", "Adicionar Queijo Parmesão e Bacon", "Adicionar Alho, Bacon e Calabresa").

**Observações:**
- Modificadores podem ter diferentes tipos (seleção única, múltipla seleção, entrada de texto, etc.).
- É importante definir claramente os Grupos de Modificadores e suas opções para facilitar a configuração e o uso.

# *Modificadores contém* Grupos de Modificadores
Um Modificador é composto por um ou mais Grupos de Modificadores. Estes representam as categorias de opções específicas que podem ser escolhidas para personalizar um Item de Menu ou um Grupo de Menus.

**Exemplos de Grupos de Modificadores:**
- **Queijo:** Contendo opções como _cheddar_, _provolone_ e _gorgonzola_.
- **Opções de Cozimento:** Contendo opções como _mal passado_, _ao ponto_ e _bem passado_.
- **Tamanho da Pizza:** Contendo opções como _pequena_, _média_ e _grande_.
- **Tipo de Borda:** Contendo opções como _tradicional_ e _recheada_.

**Aplicação a Grupos de Menu:**
Quando um Grupo de Modificadores é aplicado a um Grupo de Menu, todos os Itens de Menu associados a esse grupo herdarão as opções de modificação definidas dentro desse Grupo de Modificadores. Isso garante consistência e facilita a configuração de opções comuns.

**Grupos de Modificadores Aninhados:**
Um recurso poderoso é a possibilidade de aninhar Grupos de Modificadores dentro de outros Grupos de Modificadores. Isso permite uma personalização ainda mais granular e complexa.

**Exemplo de Grupos de Modificadores Aninhados:**
Considere uma pizza Marguerita com um Modificador de "Borda". Este Modificador pode conter um Grupo de Modificadores chamado "Tipo de Borda", com opções como "Tradicional" e "Recheada".

Dentro da opção "Recheada", podemos ter um Grupo de Modificadores aninhado chamado "Recheio da Borda" com duas subcategorias (que poderiam ser implementadas como outros Grupos de Modificadores aninhados):

- **Salgada:** Contendo opções como _Catupiry_ e _Requeijão_.
- **Doce:** Contendo opções como _Chocolate_ e _Doce de Leite_.

Assim, ao escolher a borda "Recheada", o cliente seria apresentado a outro nível de opções para escolher o recheio desejado (Catupiry, Requeijão, Chocolate ou Doce de Leite).

**Observações:**
- A profundidade do aninhamento de Grupos de Modificadores pode variar dependendo da complexidade do cardápio.
- Uma boa organização dos Grupos de Modificadores é crucial para uma experiência de usuário intuitiva.

# Regras de Reuso
Excelente seção sobre as Regras de Reuso! Isso demonstra um planejamento cuidadoso para a flexibilidade e eficiência do sistema. Vamos formatar e organizar essa informação para facilitar ainda mais a compreensão:

### **Entidades que NÃO podem ser compartilhadas:**

- **Grupos de Menu:** Um Grupo de Menu é específico para o Menu ao qual pertence e não pode ser diretamente compartilhado entre diferentes Menus.
    - **Exemplo:** O grupo "Carnes" definido para o "Cardápio Oficial" não pode ser simplesmente transferido para o "Cardápio de Drinks".

### **Entidades que PODEM ser compartilhadas:**

1. **Itens de Menu:** Um Item de Menu pode pertencer a múltiplos Grupos de Menu dentro do mesmo Menu ou até mesmo em Menus diferentes (embora o exemplo dado foque no mesmo Menu).
    
    - **Exemplo:** O item "Arroz Branco" pode ser listado no grupo "Guarnições" e também como um acompanhamento oferecido com diversos pratos principais, como a "Picanha Fatiada Grelhada".
2. **Grupos de Modificadores:** Um Grupo de Modificadores pode ser aplicado a múltiplos Grupos de Menu ou diretamente a Itens de Menu específicos.
    
    - **Exemplo:** O grupo de modificadores "Tipo de Molho" (com opções como molho de alcaparras, molho de catupiry) pode ser oferecido tanto para o Grupo de Menu "Peixes" (aplicando-se ao "Filé de Peixe") quanto para o Grupo de Menu "Massas".
3. **Modificadores (Opções dentro de um Grupo de Modificadores):** Uma opção de modificador individual pode pertencer a múltiplos Grupos de Modificadores.
    
    - **Exemplo:** A opção de modificador "Bacon" pode estar presente no Grupo de Modificadores "Adicionais para Aipim" (para o "Aipim Gratinado") e também no Grupo de Modificadores "Adicionais para Batata" (para a "Batata Gratinada").

### **Entidades que podem ser Reutilizadas:**

1. **Reutilização de Grupos de Menu como Grupos de Modificadores:** Um Grupo de Menu existente pode ser utilizado como um Grupo de Modificadores. Nesse caso, os Itens de Menu originais dentro desse grupo se tornam as opções de modificação.
    
    - **Exemplo:** O Grupo de Menu "Guarnições" (contendo "Arroz", "Batata Frita", "Farofa de Ovo") pode ser reutilizado como um Grupo de Modificadores para o Item de Menu "Picanha Fatiada Grelhada", permitindo que o cliente escolha uma dessas guarnições como acompanhamento.
2. **Reutilização de Itens de Menu como Modificadores:** Um Item de Menu já cadastrado pode ser utilizado como uma opção de modificador para outros itens.
    
    - **Exemplo:** O Item de Menu "Queijo Coalho" (originalmente listado em algum grupo, como "Petiscos") pode ser reutilizado como uma opção dentro de um Grupo de Modificadores chamado "Adicionais para Batata".
3. **Aplicação de Grupos de Modificadores a Grupos de Menu ou Itens:** Esta regra reforça a capacidade de vincular Grupos de Modificadores a Grupos de Menu (afetando todos os itens dentro) ou diretamente a Itens de Menu específicos.
    
    - **Exemplo:** O Grupo de Modificadores "Sabor" (com opções como Limão, Abacaxi) pode ser aplicado tanto ao Item de Menu "Caipirinha" quanto ao Item de Menu "Suco", oferecendo as mesmas opções de sabor para ambas as bebidas.

### **Exemplo Prático Integrado:**

- **Item de Menu Principal:** "Picanha Fatiada Grelhada"
    - **Grupo de Modificadores Compartilhado:** "Guarnições" (reutilizado do Grupo de Menu "Guarnições"), contendo Itens de Menu como "Arroz Branco", "Batata Frita", "Farofa de Ovo".
    - **Item de Menu Reutilizado como Modificador:** "Arroz Branco" é um Item de Menu independente e também uma opção dentro do Grupo de Modificadores "Guarnições".
    - **Modificadores Aninhados (Implícito):** Se o cliente selecionar a guarnição "Arroz de Brócolis" (que seria um Item de Menu dentro do Grupo "Guarnições"), este poderia ter seu próprio Grupo de Modificadores associado, como "Molho" (com opções como Molho Madeira, Molho de Alho), permitindo uma personalização adicional da guarnição escolhida.

**Observações:**
- Essas regras de reuso são cruciais para manter a base de dados do cardápio eficiente e reduzir a duplicação de informações.
- É importante ter uma interface intuitiva para gerenciar essas relações e evitar configurações complexas demais.


