# Manual de Uso - Editar Etapa

## Introdução
Este documento descreve o uso da interface de edição de etapas no sistema **Scoring Services**. O usuário pode editar informações sobre uma etapa existente, como URLs de briefing, cronograma, inscrição, além de definir datas, estados, e outras opções relacionadas à visibilidade e detalhes do evento.

---

## **Seções da Página de Edição de Etapas**

### 1. **Briefing URL**
   - **Campo:** `Briefing URL`
   - **Descrição:** Informe um link válido para o briefing, como por exemplo um documento no Google Drive.  
   - **Formato válido:** URLs iniciadas com `http://` ou `https://`.

### 2. **Cronograma URL**
   - **Campo:** `Cronograma URL`
   - **Descrição:** Informe um link válido para o cronograma do evento.  
   - **Formato válido:** URLs iniciadas com `http://` ou `https://`.

### 3. **Inscrição URL**
   - **Campo:** `Inscrição URL`
   - **Descrição:** Link para o formulário de inscrição da etapa, como Google Forms ou Shootinghouse.  
   - **Formato válido:** URLs iniciadas com `http://` ou `https://`.

### 4. **Logo da Etapa**
   - **Campo:** `Logo`
   - **Descrição:** Upload da logo do evento. O arquivo deve ser uma imagem em formato válido (JPEG, PNG, etc.).

### 5. **Data de Início e Data de Fim**
   - **Campo:** `Data Início` e `Data Fim`
   - **Descrição:** Selecione as datas de início e fim da etapa. A data de início não pode ser posterior à data de fim.

### 6. **Estado**
   - **Campo:** `Estado`
   - **Descrição:** Selecione o estado onde a etapa será realizada. Esta seleção é obrigatória.
   - **Validação:** Um estado deve ser selecionado, caso contrário, o sistema alertará o usuário.

### 7. **Descrição / Convite**
   - **Campo:** `Descrição / Convite`
   - **Descrição:** Campo de texto que aceita **Markdown** para detalhar a descrição ou convite da etapa. Utilize [esta referência](https://simplemde.com/markdown-guide) para aprender a usar o formato Markdown.

### 8. **Ativa**
   - **Campo:** `Ativa`
   - **Descrição:** Define se a etapa está ativa ou não no sistema. Esta opção está vinculada à exibição da etapa em [Scoring Services](https://m.scoring.services).

### 9. **Exibir na Lista de Provas**
   - **Campo:** `Exibir na Lista de Provas`
   - **Descrição:** Marque para que a etapa apareça na lista de provas disponíveis publicamente. Esta opção está vinculada à exibição pública em [Scoring Services](https://m.scoring.services).

### 10. **Exibir no Calendário**
   - **Campo:** `Exibir no Calendário`
   - **Descrição:** Esta opção só estará disponível se a `Inscrição URL` for preenchida. Marque esta opção para exibir a etapa no calendário público em [IPSC Guru Calendar](https://ispc.guru/calendar).

### 11. **Exibir Squads**
   - **Campo:** `Exibir Squads`
   - **Descrição:** Marque para permitir a exibição dos squads na página da etapa.

### 12. **Exibir Verify**
   - **Campo:** `Exibir Verify`
   - **Descrição:** Marque para habilitar a exibição da opção Verify na página da etapa.

### 13. **Exibir Totais**
   - **Campo:** `Exibir Totais`
   - **Descrição:** Marque para exibir os totais acumulados do evento na página da etapa.

---

## **Validações Importantes**

1. **URLs Válidas:** 
   - Todos os campos de URL (Briefing, Cronograma, Inscrição) devem conter um formato válido (`http://` ou `https://`). Caso contrário, o sistema exibirá uma mensagem de erro solicitando a correção do campo.

2. **Datas de Início e Fim:**
   - A **Data de Início** não pode ser maior que a **Data de Fim**. Se isso ocorrer, o sistema alertará o usuário para corrigir as datas.

3. **Estado Obrigatório:**
   - O campo **Estado** é obrigatório. Caso o estado não seja selecionado, o sistema emitirá uma mensagem de erro para o usuário.

4. **Exibir no Calendário:**
   - A opção **Exibir no Calendário** só estará disponível se o campo **Inscrição URL** for preenchido corretamente. O evento será exibido em [IPSC Guru Calendar](https://ispc.guru/calendar).

---

## **Ações Disponíveis**

- **Salvar:** Confirma todas as alterações feitas no formulário e as aplica ao evento.
- **Cancelar:** Cancela as alterações feitas e retorna à página anterior sem salvar os dados.

---

## **Requisitos Técnicos**

- **Navegadores compatíveis:** Recomendamos o uso das versões mais recentes do Google Chrome, Mozilla Firefox, ou Microsoft Edge.
- **Conexão à internet:** Necessário para acessar o sistema e realizar uploads de arquivos e links externos.
