---
author: "Áleson Medeiros"
title: "Como instalar e configurar o Starship para o Bash no Ubuntu"
date: 2024-05-15
description: "Transforme o Bash no Ubuntu com o Starship, um prompt de shell customizável e eficiente"
draft: false
tags: ["ubuntu", "bash", "terminal", "starship", "rust", "prompt"]
thumbnail: "/penguin-prompt.jpeg"
---

O Starship é um prompt de shell rápido, leve e altamente customizável, que fornece informações úteis e visualmente agradáveis diretamente no seu terminal. Neste tutorial, vamos mostrar como instalar e configurar o Starship para o Bash no Ubuntu, para que você possa personalizar e melhorar sua experiência no terminal.

### Instalação do Starship:

Para instalar o Starship, siga estas etapas:

1. Abra o terminal no Ubuntu.

2. Utilize o comando `curl` para baixar e executar o script de instalação do Starship:

```bash
curl -sS https://starship.rs/install.sh | sh
```

![Terminal do XFCE com script](/starship-prompt-1.png)

3. Após a instalação, abra o arquivo `~/.bashrc` em um editor de texto de sua preferência. Você pode usar o `vim` ou o `nano`, por exemplo:

```bash
nano ~/.bashrc
```

4. No final do arquivo `~/.bashrc`, adicione o seguinte comando para inicializar o Starship:

```bash
eval "$(starship init bash)"
```
![Arquivo .bashrc](/starship-prompt-2.png)

5. Salve e feche o arquivo.

6. Para aplicar as alterações, recarregue o arquivo `~/.bashrc` executando:

```bash
source ~/.bashrc
```

### Configurar um preset do Starship:

Agora que o Starship está instalado, você pode configurar um preset para personalizar o prompt. Por exemplo, você pode usar o preset bracketed-segments para adicionar segmentos entre colchetes ao prompt. Para configurar este preset, execute o seguinte comando no terminal:

```bash
starship preset bracketed-segments -o ~/.config/starship.toml
```

![Terminal dentro do VsCode mostrando as informações do projeto](/starship-prompt-3.png)

Neste tutorial, você aprendeu como instalar e configurar o Starship para o Bash no Ubuntu. O Starship é uma ferramenta poderosa que permite personalizar e melhorar a aparência e funcionalidade do seu prompt de terminal. Com o Starship configurado, você pode desfrutar de uma experiência de linha de comando mais rápida, eficiente e visualmente atraente. Experimente diferentes presets e opções de configuração para criar um prompt que atenda às suas necessidades e preferências!
