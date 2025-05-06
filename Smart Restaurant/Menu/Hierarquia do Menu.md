Entidades envolvidas na hierarquia do Menu:
# Menu
São o nível mais alto da hierarquia e representam o que o restaurante serve. ***exemplo:***  Cardápio Oficial, Cardápio de Drinks, Vinhos-Whiskey-Licores e etc...

# *Um Menu contém* Grupos de Menus
São conjuntos menores dentro do menu. ***exemplo:*** Dentro do cardápio oficial existem grupos menores como Petiscos Tradicionais, Petiscos de Frango, Aipim e etc...

# *Um Grupo de Menu contém* itens do cardápio
Esses são os itens do menu. ***exemplo***: Gorjão de Peixe, casquinha de siri e etc...

# Modificadores
Os modificadores podem ser atribuídos a grupos de menu e itens do menu que são usados para personalizar ainda mais os itens. ***exemplo:*** O item classificado como *camarão à milanesa* poderá ter um modificador para adicionar itens existentes no grupo de modificadores classificados como *queijo*. Poderá ser adicionado ao *camarão à milanesa* o modificador para acrescentar *queijo catupiry* ao seu prato.

Se você atribuir um *grupo de modificadores* a um *grupo de menus*, o grupo de modificadores será aplicado a **todos os itens de menu do grupo** por padrão, embora você possa desabilitar essa herança para itens de menu individuais no grupo, se necessário. Além disso, um item individual do menu pode ter uma combinação de modificadores que herdam de seu grupo pai de menus e modificadores que foram atribuídos ao próprio item de menu. ***exemplo***: O grupo de menu classificado como *batata* poderá ter modificadores de grupo escolhendo o tipo da batata (Simples, Gratinada, à Dom Manolo...) e modificadores do item (Batata gratinada com queijo prato, parmesão e bacon; Batata com alho bacon e calabresa...)

# *Modificadores contém* Grupos de Modificadores
Representam mudanças específicas que podem modificar itens do menu. ***exemplo:*** Um grupo de modificares classificados como *queijo* poderão conter itens como *cheddar*, *provolone* e *gorgonzola* enquanto um grupo de modificadores classificado como *Opções de cozimento* poderão conter *mal passado*, *ao ponto* e *bem passado*. Quando um grupo de modificadores é aplicado a um grupo de menu todos os itens associados àquele grupo serão modificados.

Os modificadores podem conter grupos de modificadores aninhados, permitindo que o cliente ou funcionário personalize ainda mais um modificador. Por exemplo, uma pizza Marguerita pode ter um modificador de Tamanho, podendo ser escolhido entre pequeno, médio e grande. O modificador 'Borda recheada' pode conter um grupo de modificadores aninhado chamado 'Salgada' ou 'Doce', com opções como 'Catupiry' e 'Requeijão' para a salgada e 'Chocolate' e 'Doce de leite' para a Doce.

# Regras de Reuso
O sistema permite compartilhar e reusar as entidades relacionadas ao Menu. ***exemplo:*** os itens "Picanha Fatiada Grelhada" e "Filé Mignon" podem compartilhar o mesmo grupo de modificadores "Guarnições". A lista abaixo descreve as regras de compartilhamento e reutilização:

## **Entidades que NÃO podem ser compartilhadas:**

- **Grupos de menu** não podem ser compartilhados entre menus diferentes.  
    _Exemplo:_ O grupo "Carnes" só pode existir no menu principal, não em outro menu secundário.

---

## **Entidades que PODEM ser compartilhadas:**

1. **Itens de menu** podem ser compartilhados por múltiplos grupos de menu.  
    _Exemplo:_ O item "Arroz" pode ser usado no grupo "Guarnições" e também como acompanhamento para pratos como "Picanha Fatiada Grelhada".
    
2. **Grupos de modificadores** podem ser compartilhados por múltiplos grupos de menu ou itens de menu.  
    _Exemplo:_ O grupo "Molho" (ex: molho de alcaparras, molho de catupiry) pode ser usado tanto para "Filé de Peixe" quanto para "Massas".
    
3. **Modificadores** podem ser compartilhados por múltiplos grupos de modificadores.  
    _Exemplo:_ A opção "Bacon" pode ser um modificador em "Aipim Gratinado" e em "Batata Gratinada".
    

---

## **Entidades que podem ser reutilizadas:**

1. **Reutilização de grupos de menu como grupos de modificadores:**  
    Um grupo de menu existente pode ser reutilizado como grupo de modificadores. Os itens do grupo original funcionam como referências de modificadores.  
    _Exemplo:_ O grupo "Guarnições" pode ser reutilizado como um grupo de modificadores para pratos principais como "Picanha Fatiada Grelhada", onde itens como "Arroz" ou "Batata Frita" são opções de acompanhamento.
    
2. **Reutilização de itens de menu como modificadores:**  
    Um item de menu existente pode ser reutilizado como modificador.  
    _Exemplo:_ O item "Queijo Coalho" (usado em "Aipim Gratinado") pode ser um modificador para personalizar a "Borda Recheada" de pizzas.
    
3. **Aplicação de grupos de modificadores a grupos de menu ou itens:**  
    Grupos de modificadores podem ser vinculados a grupos de menu ou itens específicos.  
    _Exemplo:_ O grupo "Sabor" (Limão, Abacaxi, etc.) pode ser aplicado tanto à "Caipirinha" quanto à "Caipivodka".
    

---

## **Exemplo Prático:**

- **Item Principal:** "Picanha Fatiada Grelhada".
    - **Grupo de Modificadores Compartilhado:** "Guarnições" (Arroz, Batata Frita, Farofa de Ovo).
    - **Modificador Reutilizado:** "Arroz" é um item de menu independente e também uma opção de guarnição.
    - **Modificadores aninhados:** Se o cliente escolher "Arroz de Brócolis", um subgrupo "Molho" (ex: Molho Madeira, Molho de Alho) pode ser aplicado.

