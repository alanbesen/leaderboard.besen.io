---
title: Processo de Exportação / WinMSS s ShootinHouse
---

# Processo de Exportação / WinMSS s ShootinHouse

Este processo de exportação foi desenvolvido para ser utilizado através da interface web da aplicação. Ele é acionado ao clicar no botão **"Exportar para WinMSS"** disponível na página de exportação.

## Contexto
O objetivo principal deste recurso é permitir que os administradores e organizadores de competições possam gerar arquivos compatíveis com os sistemas **WinMSS** e **ShootingHouse** de maneira simplificada e eficiente. Estes arquivos contêm informações detalhadas da competição, como competidores, etapas (stages), resultados e muito mais.

## Processo de Exportação

1. **Ao clicar no botão de exportação**, o sistema processa automaticamente os dados da competição e gera os arquivos necessários nos formatos exigidos pelos sistemas de destino.

2. **Geração de Arquivos XML**: O sistema cria vários arquivos XML com as informações da competição, organizados por categorias e divisões.

3. **Arquivos .cab para WinMSS**: Após a criação dos XMLs, eles são compactados em um arquivo `.cab`.

4. **Arquivos .zip para ShootingHouse**: O sistema também gera um arquivo `.zip` contendo os XMLs, compatível com o ShootingHouse.

5. **Download**: Os arquivos gerados são disponibilizados para download diretamente na página após a conclusão do processo.

## Regras de Negócio

- **Associação de Atletas a Divisões**: Atletas inscritos em múltiplas divisões são tratados individualmente, com um registro separado para cada divisão.
  
- **Ajuste de Pontuações**: Resultados como "DNF" ou "DQ" são convertidos para valores neutros (como `0.00` ou `0`).

- **Geração de Tags Padrão**: Se uma divisão não tiver uma tag específica, uma **tag padrão** é adicionada ao XML.

- **Validação de Dados**: O sistema valida os dados antes da exportação para garantir que estejam no formato correto.

## Instruções para o Sistema ShootingHouse

Ao importar os arquivos gerados no sistema **ShootingHouse**, é necessário utilizar o **campo de identificação interna** do sistema para selecionar a importação. Este campo vincula automaticamente a modalidade importada com a modalidade do **WinMSS**, facilitando o processo de gestão de resultados e assegurando que os dados sejam corretamente associados no sistema.

## Funcionamento na Interface Web

A interação com o usuário é simples: ao clicar no botão **"Exportar para WinMSS"**, todo o processamento é feito em segundo plano, e o usuário pode baixar os arquivos gerados assim que estiverem prontos.

## Vinculação Correta de Modalidades no Arquivo zip para o ShootingHouse

- Para **modalidades padrão como Handgun**, os arquivos gerados pelo sistema estarão corretamente vinculados à modalidade correspondente no **WinMSS**.
  
- Modalidades como **Light, Mini Rifle, CCP**, entre outras, serão associadas como **"Handgun Open"** ao serem importadas no **ShootingHouse**. Isso garante a correta importação e gestão dos resultados para essas modalidades.

## Tags Especiais

- Para a **divisão Light** e/ou **380**, será gerada automaticamente a **tag "380"** nos arquivos XML para garantir que a divisão seja importada corretamente.


- Para a **Semi Auto Open**, geralmente vinculada a Mini Rifle será gerada automaticamente a **tag "MRO"** nos arquivos XML para garantir que a divisão seja importada corretamente.

- Demais divisões, não vão ter tag vinculada. Divisões que estão com o nome de "Unknown - *Divisão*" vão estar sempre vinculadas a **Handgun - Open**

- Outras modalidades que não possuem tags específicas seguirão as regras padrão de vinculação e geração de tags definidas pelo sistema.

