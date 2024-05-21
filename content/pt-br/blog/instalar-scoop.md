---
author: "Áleson Medeiros"
title: "Como instalar e configurar o Scoop"
date: 2024-05-18
description: "Descubra como instalar e usar o Scoop para gerenciar pacotes no Windows de forma eficiente via linha de comando"
draft: false
tags: ["powershell", "Windows", "terminal", "scoop", "packges"]
thumbnail: "/instalar-scoop-01.jpeg"
---

O Scoop é um gerenciador de pacotes para Windows, semelhante ao Homebrew no macOS. Com ele, é possível instalar e gerenciar uma variedade de software através da linha de comando. Neste tutorial, vamos mostrar como instalar o Scoop e usar comandos básicos para buscar e instalar pacotes.

### Instalação do Scoop
Para instalar o Scoop, siga estas etapas:

1. Abra o PowerShell como Administrador.

2. Digite o seguinte comando para instalar o Scoop:

```powershell
Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser
Invoke-RestMethod -Uri https://get.scoop.sh | Invoke-Expression
```
![Instalar no Terminal do Windows](/instalar-scoop-02.png)

### Comandos básicos para buscar pacotes e instalar
Depois de instalar o Scoop, você pode usar uma variedade de comandos para buscar e instalar pacotes. Aqui estão alguns comandos básicos:

1. **Atualizar o Scoop**: Para garantir que você está usando a versão mais recente do Scoop, use:

```powershell
scoop update
```

2. **Buscar pacotes**: Para procurar um pacote específico, use:

```powershell
scoop search fastfetch
```

![Buscando pacote no terminal](/instalar-scoop-03.png)

3. **Instalar pacotes**: Para instalar um pacote, use:

```powershell
scoop install fastfetch
```

![Instalação do pacote fastfetch](/instalar-scoop-04.png)

4. **Listar pacotes instalados**: Para ver uma lista de pacotes instalados, use:

```powershell
scoop list
```

5. **Remover pacotes**: Para remover um pacote, use:

```powershell
scoop uninstall <nome_do_pacote>
```

![Pacote fastfetch instalado pelo scoop](/instalar-scoop-05.png)

Com o Scoop instalado, você agora pode gerenciar software no Windows com facilidade. Este tutorial mostrou como instalar o Scoop e executar alguns comandos básicos para buscar e instalar pacotes. Explore mais comandos para aumentar sua produtividade com o Scoop!