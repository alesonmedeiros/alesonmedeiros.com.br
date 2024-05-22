---
author: "Áleson Medeiros"
title: "Como instalar e configurar o Terminal-Icons para o PowerShell"
date: 2024-05-21
description: "Adicione ícones ao PowerShell com o Terminal-Icons para uma navegação mais visual e intuitiva"
draft: false
tags: ["icons", "Windows", "terminal", "starship", "powershell", "gallery"]
thumbnail: "/terminal-icons-powershell-01.jpeg"
---

O `Terminal-Icons` é um módulo do PowerShell que adiciona ícones a diretórios e arquivos no terminal, facilitando a visualização e identificação. Com este módulo, você pode tornar a experiência no PowerShell mais visual e intuitiva. Neste tutorial, vamos mostrar como instalar e configurar o `Terminal-Icons` para o PowerShell.

![Terminal sem ícones](/terminal-icons-powershell-02.png)

### Instalação do Terminal-Icons
Para instalar o `Terminal-Icons`, siga estas etapas:

1. Abra o PowerShell como Administrador.

2. Para instalar o módulo, use o `PowerShell Gallery`, que é um repositório de módulos para o PowerShell. Digite o seguinte comando para instalar o `Terminal-Icons`:

```powershell
Install-Module -Name Terminal-Icons -Force -Scope CurrentUser
```

![Instalação do Terminal Icons](/terminal-icons-powershell-03.png)

3. Se solicitado a confirmar a instalação de pacotes adicionais, como a conexão com o `PowerShell Gallery`, digite "Y" para continuar.

### Configuração do Terminal-Icons
Depois de instalar o módulo, você precisa carregá-lo no PowerShell para que os ícones sejam exibidos. Aqui está o processo para carregar e usar o `Terminal-Icons`:

1. Carregue o módulo digitando o seguinte comando no PowerShell:

```powershell
Import-Module Terminal-Icons
```

![Importação do PowerShell](/terminal-icons-powershell-04.png)

2. Para garantir que o `Terminal-Icons` seja carregado automaticamente sempre que abrir o PowerShell, adicione o comando `Import-Module Terminal-Icons` ao seu perfil do PowerShell. Para fazer isso, siga estas etapas:

   * Abra o arquivo de perfil do PowerShell. Normalmente, está localizado em:

```powershell
notepad $PROFILE
```

   * Adicione a seguinte linha ao arquivo de perfil:

```powershell
Import-Module Terminal-Icons
```

![Importação dentro do arquivo de perfil](/terminal-icons-powershell-06.png)

   * Salve e feche o arquivo. Reinicie o PowerShell para aplicar as alterações.

3. Agora, ao listar diretórios e arquivos no PowerShell, você verá ícones associados a diferentes tipos de arquivos e pastas. Por exemplo, um ícone de pasta para diretórios, um ícone de arquivo de texto para arquivos .txt, e assim por diante.

![Terminal-Icons ativados](/terminal-icons-powershell-05.png)

Neste tutorial, você aprendeu como instalar e configurar o Terminal-Icons para o PowerShell, trazendo ícones visuais para o terminal. Com esse módulo, a experiência no PowerShell é mais agradável e intuitiva, facilitando a navegação entre arquivos e pastas. Agora você pode aproveitar seu terminal com um toque visual adicional!