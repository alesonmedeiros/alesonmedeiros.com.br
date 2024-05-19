---
author: "Áleson Medeiros"
title: "Como instalar e configurar o Starship para o PowerShell"
date: 2024-05-19
description: "Instale e configure o Starship para o PowerShell, criando um prompt de shell rápido e personalizável"
draft: false
tags: ["powershell", "Windows", "terminal", "starship", "packges"]
thumbnail: "/startship-powershell-01.jpeg"
---

O Starship é um prompt de shell rápido e personalizável, que proporciona uma experiência visualmente agradável e informativa no terminal. Neste tutorial, vamos mostrar como instalar e configurar o Starship para o PowerShell no Windows, incluindo a aplicação do preset Gruvbox Rainbow.

### Instalação do Starship
Para instalar o Starship, siga estas etapas:

1. Instalar o Starship com o Scoop:

   * Abra o PowerShell como Administrador.

   * Instale o Starship usando o comando

```powershell
scoop install starship
```

![Instalação via Scoop](/startship-powershell-02.png)

2. Criar e configurar o perfil do PowerShell:

   * Crie o arquivo de perfil do PowerShell (se ainda não existir):

```powershell
New-Item -Path $PROFILE -Type File -Force
```

![Criar o pefil do PowerShell](/startship-powershell-03.png)

   * Adicione o comando de inicialização do Starship ao arquivo de perfil:

```powershell
Add-Content -Path $PROFILE -Value 'Invoke-Expression (&starship init powershell)'
```

![Criar o pefil do PowerShell](/startship-powershell-04.png)

3. Criar a pasta de configuração:

   * Antes de continuar, é necessário criar a pasta `.config` dentro da pasta do usuário no Windows:

```powershell
mkdir ~/.config
```

![Criar a pasta .config](/startship-powershell-05.png)

4. Criar o arquivo de configuração do Starship:

   * Dentro da pasta `.config`, crie um arquivo chamado `starship.toml`:

```powershell
New-Item -Path ~/.config/starship.toml -Type File
```

![Criar o arquivo starship.toml](/startship-powershell-06.png)

### Configurar um preset do Starship

Para aplicar o preset Gruvbox Rainbow ao Starship, siga estas etapas:

1. Copiar o conteúdo do preset Gruvbox Rainbow:

   * Abra o arquivo `starship.toml` criado anteriormente:

```powershell
notepad ~/.config/starship.toml
```

![Incluir o preset Gruvbox Rainbow no starship.toml](/startship-powershell-07.png)

   * Copie e cole o conteúdo do preset Gruvbox Rainbow no arquivo starship.toml. O conteúdo do preset pode ser encontrado no repositório oficial do Starship ou em uma fonte confiável.

2. Salvar e fechar o arquivo:

   * Salve as alterações e feche o editor de texto.

3. Reiniciar o terminal:

   * Feche e reabra o PowerShell para aplicar as configurações.

![Gruvbox Rainbow no terminal](/startship-powershell-08.png)

Neste tutorial, você aprendeu como instalar e configurar o Starship para o PowerShell no Windows, incluindo a aplicação do preset Gruvbox Rainbow. Com o Starship, seu prompt de shell se torna mais informativo e visualmente atraente, melhorando a experiência de uso do terminal. Agora, aproveite a nova aparência do seu PowerShell e explore as diversas opções de personalização que o Starship oferece!

