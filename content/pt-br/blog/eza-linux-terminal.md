---
author: "Áleson Medeiros"
title: "Como instalar e configurar o eza no Linux"
date: 2024-05-22
description: "Substitua o comando ls pelo eza no Linux para uma listagem de arquivos avançada e visualmente aprimorada"
draft: false
tags: ["icons", "ubuntu", "terminal", "starship", "eza"]
thumbnail: "/eza-linux-terminal-01.jpeg"
---

O `eza` é um substituto moderno para o comando `ls`, com recursos avançados como cores, classificação por tipo de arquivo, ícones e outras melhorias. É uma excelente ferramenta para quem deseja aprimorar a experiência no terminal no Linux. Neste tutorial, vamos mostrar como instalar o `eza` e configurá-lo como substituto do comando `ls`, incluindo a criação de um alias.

![Instalação do eza](/eza-linux-terminal-05.png)

### Instalação do eza
Para instalar o `eza`, o método pode variar dependendo da sua distribuição Linux. Aqui estão algumas maneiras de instalá-lo em diferentes distribuições:

* **Ubuntu/Debian**.

1. Atualize a lista de pacotes:

```bash
sudo apt update
```

2. Instale o `eza` a partir do repositório oficial:

```bash
sudo apt install eza
```

![Instalação do eza](/eza-linux-terminal-02.png)

### Configuração do alias para substituir o ls por eza
Após instalar o `eza`, você pode configurá-lo para substituir o comando `ls` usando um alias. Isso torna o uso do `eza` mais intuitivo, pois você pode continuar digitando "ls" e receber a funcionalidade avançada do `eza`. Veja como configurar o alias:

1. Abra seu arquivo de configuração do shell. Se estiver usando o Bash, pode ser o `.bashrc` ou `.bash_profile`. Se estiver usando o Zsh, pode ser o `.zshrc`. Para abrir o arquivo, use:

```bash
nano ~/.bashrc  # Para Bash
```

2. Adicione o alias para substituir o `ls` pelo `eza` com opções adicionais:

```bash
alias ls='eza -lha --icons'
```

![Instalação do eza](/eza-linux-terminal-03.png)

3. Salve o arquivo e feche o editor de texto.

4. Para aplicar as alterações, recarregue o arquivo de configuração ou reinicie seu terminal:

```bash
source ~/.bashrc  # Para Bash
```

![Instalação do eza](/eza-linux-terminal-04.png)

Neste tutorial, você aprendeu como instalar o `eza` no Linux, uma ferramenta moderna para substituir o comando `ls`. Também viu como configurar um alias para usar o `eza` no lugar do `ls`, com opções adicionais para tornar a listagem de arquivos mais visual e informativa. Com esse alias, você pode usar o comando `ls` como de costume, mas com todos os recursos avançados do `eza`. Agora, você pode aproveitar uma experiência de terminal mais rica e eficaz!