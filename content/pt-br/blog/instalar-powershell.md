---
author: "Áleson Medeiros"
title: "Como instalar e configurar o PowerShell no formato MSI"
date: 2024-05-17
description: "Aprenda a instalar o PowerShell 7 no Windows, configurá-lo no Windows Terminal e personalizar com fontes NerdFonts"
draft: false
tags: ["powershell", "Windows", "terminal", "starship", "rust", "nerdfonts", "prompt"]
thumbnail: "/instalar-powershell-01.jpeg"
---

O PowerShell é uma poderosa ferramenta de linha de comando e linguagem de script para automatizar tarefas no Windows. A versão mais recente, PowerShell 7, traz diversas melhorias e recursos. Neste tutorial, vamos mostrar como instalar o PowerShell 7 usando o formato MSI, configurá-lo como o shell principal do Windows Terminal e adicionar uma fonte personalizada para melhorar a aparência do terminal.

### Download (MSI)
Para começar, acesse o [site oficial do PowerShell](https://learn.microsoft.com/pt-br/powershell/scripting/install/installing-powershell-on-windows?view=powershell-7.4) para baixar o arquivo MSI da versão mais recente. Selecione a opção adequada para o seu sistema operacional (Windows) e salve o arquivo em seu computador.

### Instalação do PowerShell 7
Depois de baixar o arquivo MSI, siga estas etapas para instalar o PowerShell 7:

1. Clique duas vezes no arquivo MSI para iniciar a instalação.

2. Siga as instruções na tela para concluir a instalação.

3. Após a conclusão, confirme se o PowerShell 7 foi instalado corretamente. Abra o menu Iniciar, digite "PowerShell" e selecione a versão mais recente para abrir o terminal.

![Tela de instalação do PowerShell](/instalar-powershell-02.png)

### Configurar como shell principal do Windows Terminal
O Windows Terminal permite configurar diferentes shells. Para definir o PowerShell 7 como o shell principal, siga estas etapas:

1. Abra o Windows Terminal.

2. Clique na seta para baixo (ícone de menu) e selecione "Configurações".

![Configurações do Terminal](/instalar-powershell-03.png)

3. Na seção "Startup", escolha "PowerShell" como o perfil padrão.

4. Clique em "Salvar" para aplicar as alterações.

![Definir como PowerShell como padrão](/instalar-powershell-04.png)

### Instalação de fonte do NerdFonts (Fantasque Sans Mono)
Para melhorar a aparência do terminal, você pode instalar uma fonte do NerdFonts. Vamos usar a fonte "Fantasque Sans Mono":

1. Acesse o site do NerdFonts e baixe a fonte "[Fantasque Sans Mono](https://github.com/ryanoasis/nerd-fonts/releases/download/v3.2.1/FantasqueSansMono.zip)".

![Nerd Fonts](/instalar-powershell-05.png)

2. Descompacte o arquivo baixado e clique com o botão direito na fonte para instalá-la.

3. Para definir a fonte no Windows Terminal, vá para "Configurações", escolha "PowerShell", e defina a fonte como "Fantasque Sans Mono".

![Definir fonte padrão](/instalar-powershell-06.png)

Neste tutorial, você aprendeu como instalar o PowerShell 7 usando o formato MSI, configurar o PowerShell como shell principal do Windows Terminal e instalar uma fonte personalizada para melhorar a aparência do terminal. Agora você está pronto para explorar os recursos avançados do PowerShell!