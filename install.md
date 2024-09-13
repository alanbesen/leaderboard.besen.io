# ps-leaderboard Installation Guide

## Requisitos do Sistema:

- Este sistema é compatível apenas com **Windows 7 ou superior**. Certifique-se de que seu sistema operacional atenda a este requisito antes de prosseguir.

## Passos para Instalação:

1. **Download do Arquivo ZIP:**
   - Faça o download do arquivo `ps-leaderboard.zip` a partir do link fornecido.

2. **Descompactar o arquivo ZIP:**
   - Após o download, localize o arquivo `ps-leaderboard.zip` na pasta de downloads do seu computador.
   - Clique com o **botão direito do mouse** no arquivo `ps-leaderboard.zip` e escolha a opção **Extrair Tudo...**.
   - Na janela que abrir, selecione o caminho `C:\` como o destino da extração e clique em **Extrair**.
   - Isso criará a pasta `C:\ps-leaderboard` contendo todos os arquivos necessários.

3. **Arquivos e Estrutura de Diretórios:**
   Dentro do diretório `C:\ps-leaderboard`, você encontrará os seguintes arquivos:

   - `remove_service.bat`: Deve ser executado como **Administrador** para remover o serviço.
   - `install_service.bat`: Deve ser executado como **Administrador** para instalar o serviço.
   - `nssm.exe`
   - `ps_service_manager.exe`
   - `config.ini`

   Além disso, você encontrará um subdiretório:
   `C:\ps-leaderboard\ps\`

   Dentro deste subdiretório `ps`, você verá os seguintes itens:
   
   - `config.ini`
   - `ps.exe`

4. **Como Abrir e Editar o Arquivo `config.ini` com o Notepad:**
   - Navegue até o diretório `C:\ps-leaderboard\ps\`.
   - Encontre o arquivo chamado `config.ini`.
   - Clique com o **botão direito do mouse** no arquivo `config.ini`.
   - No menu que aparecer, selecione a opção **Abrir com**.
   - Escolha o programa **Bloco de Notas (Notepad)** da lista e clique em **OK**.

   - Agora, com o arquivo aberto no Bloco de Notas, você deve configurar as seguintes variáveis ou substituir o arquivo por um obtido no portal:
   
     ```ini
     upload_token = xxxxx
     client_id = xxx
     licenca = xxxx
     ```

   - Após fazer as alterações, clique em **Arquivo** no canto superior esquerdo e selecione **Salvar**.

5. **Como Executar os Arquivos `install_service.bat` e `remove_service.bat` como Administrador:**

   - **Passo 1:** Navegue até o diretório `C:\ps-leaderboard` onde os arquivos `install_service.bat` e `remove_service.bat` estão localizados.
   - **Passo 2:** Clique com o **botão direito do mouse** no arquivo `install_service.bat` (ou `remove_service.bat`).
   - **Passo 3:** No menu que aparecer, clique na opção **Executar como administrador**.
   
     > **Nota:** Se aparecer uma mensagem do Controle de Conta de Usuário (UAC) perguntando se você deseja permitir que o programa faça alterações no seu computador, clique em **Sim**.

   - **Passo 4:** O script será executado e o serviço será instalado (ou removido, dependendo do arquivo escolhido). Aguarde até o processo ser concluído.

6. **Instalação do Serviço:**
   - Siga os passos acima para executar o arquivo `install_service.bat` como **Administrador**.

7. **Configuração Final:**
   - Certifique-se de que o arquivo `C:\ps-leaderboard\ps\config.ini` esteja devidamente configurado.
   - Depois disso, execute o `ps_service_manager.exe` para iniciar ou parar o serviço.

8. **Acessar o Painel via Navegador:**
   - Depois de iniciar o serviço, obtenha o endereço IP da máquina para acessar o sistema no navegador. Para obter o IP da máquina no Windows, siga estas etapas:
   
     1. Pressione `Win + R` e digite `cmd` para abrir o Prompt de Comando.
     2. Digite o comando:  
        `ipconfig`
     3. Procure a seção **Adaptador de Rede** (pode variar dependendo do seu tipo de conexão) e localize o **Endereço IPv4**.

   - No navegador, acesse o sistema usando o IP e a porta 5001:  
     `http://<IP>:5001`

9. **Configuração dos Tablets:**
   - Para configurar os tablets, acesse:  
     `http://<IP>:5001/devices`
   
   - **Como obter o IP no tablet:**
     
     **iOS (iPad/iPhone):**
     1. Vá para `Configurações`.
     2. Toque em `Wi-Fi`.
     3. Toque no ícone de "i" ao lado da rede Wi-Fi conectada.
     4. O IP será mostrado na seção **Endereço IP**.
   
     **Android:**
     1. Vá para `Configurações`.
     2. Toque em `Conexões` ou `Rede e Internet` (pode variar entre os dispositivos).
     3. Toque em `Wi-Fi` e selecione a rede conectada.
     4. O endereço IP será exibido em **Endereço IP**.

   - **Configuração do PractiScore:**  
     Certifique-se de que o software `PractiScore` esteja aberto no tablet.
     - Adicione o dispositivo na página de `Devices` e reinicie o scheduler.
   
   - Após isso, os dados começarão a aparecer automaticamente no painel de administração.
