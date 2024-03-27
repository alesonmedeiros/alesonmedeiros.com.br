---
author: "Áleson Medeiros"
title: "Como Formatar um Chromebook HP e Instalar o Windows: Tutorial Passo a Passo"
date: 2024-03-27
description: "Como formatar de maneira simples o Chromebook e instalar o Windows nele"
draft: false
tags: ["chromebook", "windows", "formatação"]
thumbnail: "/windows-chromebook.jpeg"
---

Os Chromebooks oferecem um ambiente eficiente para muitos usuários, mas alguns podem desejar instalar um sistema operacional diferente, como o Windows. Neste tutorial, vamos guiar você pelo processo de formatação de um Chromebook HP e a instalação do Windows. Para isso, vamos precisar ativar o modo desenvolvedor, verificar e desativar a proteção de gravação, instalar o Coreboot e, por fim, realizar a instalação do Windows.

### Passo 1: Ativando o Modo Desenvolvedor do Chromebook HP

Ligue o Chromebook.
Pressione e segure as teclas Esc + Atualizar (F3) e, em seguida, pressione o botão liga/desliga.
Quando uma tela de aviso for exibida, pressione Ctrl + D para ativar o Modo Desenvolvedor.

### Passo 2: Verificar o Status de Proteção de Gravação do Hardware

Abra o terminal.
Insira o comando: `crossystem | grep wpsw` para verificar o status de proteção de gravação.

### Passo 3: Desativar a Proteção de Gravação via Jumper na Placa do ChromeBook

![Traseira do Chromebook](/chromebook-fundo-01.jpg)
![Ponto para relizar o jumper](/chromebook-fundo-02.jpg)

### Passo 4: Verificar o Status de Gravação via Software

No terminal, digite: `flashrom -p ec --wp-status` para verificar o status de gravação.

### Passo 5: Remover a Proteção de Gravação via Software

No terminal, utilize o comando: `flashrom -p ec --wp-disable` para desabilitar a proteção de gravação.

Passo 6: Executar o Script de Firmware para Instalar o Coreboot

No terminal, digite: `cd; curl -LO mrchromebox.tech/firmware-util.sh && sudo bash firmware-util.sh` para baixar e executar o script de firmware.

### Passo 7: Realizar a Instalação do Windows

Siga as instruções normais para instalar o Windows no Chromebook, utilizando uma unidade USB inicializável com a imagem do Windows.

Formatar um Chromebook e instalar o Windows pode ser um processo desafiador, mas seguindo esses passos, você estará no caminho certo. Lembre-se sempre de fazer backups de seus dados antes de iniciar o processo, pois a formatação resultará na perda de todos os dados armazenados no Chromebook.

Esperamos que este tutorial tenha sido útil para você transformar o seu Chromebook HP para rodar o sistema operacional Windows.

