# ps-leaderboard Installation Guide

## Passos para Instalação:

1. **Descompactar o arquivo ZIP:**
   - Extraia o conteúdo do arquivo `ps-leaderboard.zip` para o diretório obrigatório:  
     `C:\ps-leaderboard`

2. **Arquivos e Estrutura de Diretórios:**
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

3. **Configuração do Arquivo `config.ini`:**
   - Navegue até o arquivo de configuração em:  
     `C:\ps-leaderboard\ps\config.ini`
   
   - Você deve configurar as seguintes variáveis manualmente ou baixar o arquivo `config.ini` atualizado diretamente do portal e sobrescrever o arquivo existente:
   
     ```ini
     upload_token = xxxx
     client_id = xxxx
     licenca = xxxx
     ```

4. **Instalação do Serviço:**
   - Abra o **Prompt de Comando** como **Administrador**.
   - Navegue até o diretório `C:\ps-leaderboard`.
   - Execute o comando:  
     `install_service.bat`
   
5. **Configuração Final:**
   - Certifique-se de que o arquivo `C:\ps-leaderboard\ps\config.ini` esteja devidamente configurado.
   - Depois disso, execute o `ps_service_manager.exe` para iniciar ou parar o serviço.

6. **Acessar o Painel via Navegador:**
   - Depois de iniciar o serviço, obtenha o endereço IP da máquina para acessar o sistema no navegador. Para obter o IP da máquina no Windows, siga estas etapas:
   
     1. Pressione `Win + R` e digite `cmd` para abrir o Prompt de Comando.
     2. Digite o comando:  
        `ipconfig`
     3. Procure a seção **Adaptador de Rede** (pode variar dependendo do seu tipo de conexão) e localize o **Endereço IPv4**.

   - No navegador, acesse o sistema usando o IP e a porta 5001:  
     `http://<IP>:5001`
   
7. **Configuração dos Tablets:**
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
