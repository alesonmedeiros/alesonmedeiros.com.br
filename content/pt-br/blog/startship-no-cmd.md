---
author: "Áleson Medeiros"
title: "Como instalar e configurar o Starship para o CMD"
date: 2024-05-20
description: "Melhore o CMD com o Starship e Clink, tornando-o mais moderno e eficiente com um prompt customizável"
draft: false
tags: ["cmd", "Windows", "terminal", "starship", "packges"]
thumbnail: "/startship-no-cmd-01.jpeg"
---

O Starship é um prompt de shell rápido e personalizável, que pode ser usado tanto no PowerShell quanto no CMD. Neste tutorial, vamos mostrar como instalar e configurar o Starship para o CMD no Windows, utilizando o Clink para integrar o Starship ao CMD e aplicando o preset Gruvbox Rainbow.

### Instalação do Starship
Se você já instalou o Starship usando o Scoop no tutorial anterior, pode pular esta etapa. Caso contrário, siga estas instruções:

1. Instalar o Starship com o Scoop:

   * Abra o CMD como Administrador.

   * Instale o Starship usando o comando

```cmd
scoop install starship
```

### Instalação do Clink
Para integrar o Starship ao CMD, precisamos instalar o Clink. Siga estas etapas:

1. Baixar e instalar o Clink:

   * Visite o site do Clink [aqui](https://chrisant996.github.io/clink/clink.html) e baixe o instalador.

   * Execute o instalador e siga as instruções para concluir a instalação.

### Configuração do Clink com Starship
Para configurar o Clink para usar o Starship, siga estas etapas:

1. Criar o arquivo de configuração do Clink:

   * Crie um arquivo chamado `starship.lua` no caminho `%LocalAppData%\clink\`.

   * Para fazer isso, abra o Explorer e navegue até `%LocalAppData%\clink\`, depois clique com o botão direito e selecione *Novo > Documento de Texto*. Renomeie o arquivo para `starship.lua`.

2. Adicionar o conteúdo de inicialização do Starship:

   * Abra o arquivo starship.lua com um editor de texto (por exemplo, Notepad):

   * Adicione o seguinte conteúdo ao arquivo:

```lua
load(io.popen('starship init cmd'):read("*a"))()
```

   * Salve e feche o arquivo.

![Criação do arquivo starship.lua](/startship-no-cmd-02.png)

### Configuração do preset do Starship
Se você já seguiu o Tutorial 3 e configurou o preset Gruvbox Rainbow, pode pular esta etapa. Caso contrário, siga estas instruções:

1. Criar a pasta de configuração:

   * Crie a pasta `.config` dentro da pasta do usuário no Windows.

```cmd
mkdir %USERPROFILE%\.config
```

2. Criar o arquivo de configuração do Starship:

   * Crie um arquivo chamado `starship.toml` dentro da pasta `.config`:

```cmd
type NUL > %USERPROFILE%\.config\starship.toml
```

3. Adicionar o conteúdo do preset Gruvbox Rainbow:

   * Abra o arquivo starship.toml com um editor de texto (por exemplo, Notepad):

   * Copie e cole o conteúdo do preset Gruvbox Rainbow no arquivo starship.toml. O conteúdo do preset pode ser encontrado no repositório oficial do Starship ou em uma fonte confiável.

   * Salve e feche o arquivo.

![Criação do arquivo starship.lua](/startship-no-cmd-03.png)

Neste tutorial, você aprendeu como instalar e configurar o Starship para o CMD no Windows, utilizando o Clink para integrar o Starship ao CMD e aplicando o preset Gruvbox Rainbow. Com o Starship configurado, seu prompt de CMD será mais informativo e visualmente atraente, melhorando a experiência de uso do terminal. Aproveite a nova aparência do seu CMD e explore as diversas opções de personalização que o Starship oferece!