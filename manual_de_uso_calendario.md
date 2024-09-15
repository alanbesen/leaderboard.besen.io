# Manual de Uso - IPSC.guru - Calendário de Provas IPSC

## Introdução

O **IPSC.guru** é um sistema de gestão de provas destinado a facilitar o cadastro, edição e exclusão de provas de tiro prático no calendário IPSC. 

## Funcionalidades

### 1. **Cadastrar uma Nova Prova**

#### Itens Necessários
Para cadastrar uma nova prova no sistema, o usuário deverá preencher os seguintes campos obrigatórios:

- **Nome da Prova**: O nome da competição.
- **Data de Início**: A data em que a prova começará.
- **Data de Fim**: A data em que a prova terminará.
- **Estado**: O estado brasileiro onde a prova será realizada.
- **Convite** (Opcional): Um campo de descrição com suporte a Markdown para adicionar um convite ou descrição da prova.

#### Campos Opcionais:
- **Link para Inscrição**: Um link para o site de inscrição da prova, se disponível.
- **Status de Exibição**: Por padrão, a prova não estará ativa no calendário. Caso deseje exibi-la, você deve marcar a caixa de seleção para ativá-la.

#### Validações:
- **Datas**: A data de início não pode ser maior que a data de fim. Caso essa regra seja violada, o sistema exibirá uma mensagem de alerta e não permitirá o envio do formulário.
- **Link de Inscrição**: Se fornecido, o link de inscrição deve ser uma URL válida. O sistema validará o formato do link antes de permitir o envio do formulário.

#### Como Adicionar uma Prova:
1. Na página inicial do sistema, clique no botão verde `Cadastrar Nova Prova`.
2. Preencha todos os campos obrigatórios.
3. Se desejar, adicione o link de inscrição e marque a opção de exibir a prova no calendário.
4. Clique em `Adicionar` para salvar a prova no sistema.

### 2. **Editar Prova Existente**

Caso queira modificar uma prova já cadastrada, você poderá utilizar a funcionalidade de edição. Isso pode ser útil caso precise alterar a data da prova, atualizar o link de inscrição ou qualquer outra informação.

#### Como Editar uma Prova:
1. Na lista de provas, localize a prova que deseja editar.
2. Clique no botão amarelo `Editar` ao lado da prova.
3. Faça as modificações desejadas e clique em `Atualizar` para salvar as alterações.

### 3. **Excluir Prova**

Para remover uma prova que não será mais realizada ou que foi cadastrada incorretamente, utilize a função de exclusão.

#### Como Excluir uma Prova:
1. Na lista de provas, localize a prova que deseja excluir.
2. Clique no botão vermelho `Excluir`.
3. Confirme a exclusão para remover a prova do sistema permanentemente.

### 4. **Convite em Markdown**

O campo de convite suporta a linguagem de formatação **Markdown**, permitindo adicionar descrições detalhadas e formatadas à prova. Você pode, por exemplo:
- Criar listas;
- Adicionar negrito e itálico;
- Incluir links e cabeçalhos.

Para saber mais sobre como usar Markdown, clique no link de ajuda disponível no formulário.

### 5. **Validações Implementadas**

O sistema verifica automaticamente os seguintes critérios ao submeter o formulário:

1. **Data de Início x Data de Fim**:
   - A data de início não pode ser maior que a data de fim. Caso essa validação falhe, o sistema exibirá um alerta e pedirá a correção das datas.
   
2. **Link de Inscrição**:
   - Se o campo de link de inscrição for preenchido, o sistema verificará se é uma URL válida. Caso o link seja inválido, um alerta será exibido pedindo uma URL correta.

### Exemplo de Validação:
Se você tentar salvar uma prova onde a data de início é maior que a data de fim, o seguinte erro será exibido:
