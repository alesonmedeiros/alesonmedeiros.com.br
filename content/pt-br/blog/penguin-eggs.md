---
author: "Áleson Medeiros"
title: "Desbravando o Mundo das ISOs Personalizadas com Penguins' Eggs"
date: 2024-03-28
description: "Como criar uma iso instalável do seu sistema de forma fácil"
draft: false
tags: ["distro", "iso", "instável", "penguin-eggs", "clone"]
thumbnail: "/penguin-eggs.jpeg"
---

No vasto universo do Linux, personalizar e criar sua própria distribuição pode parecer uma tarefa complexa e desafiadora. Entretanto, a ferramenta [Penguins' Eggs](https://penguins-eggs.net/) surge como uma solução inovadora para simplificar esse processo, permitindo que usuários criem suas ISOs de instalação com base em clones de seus sistemas. Neste artigo, exploraremos como utilizar essa ferramenta, com enfoque especial no processo para sistemas Debian, Devuan, Ubuntu e suas derivações.

### Como Usar o Script:

A utilização do Penguins' Eggs é tão intuitiva quanto eficiente. Começaremos baixando a ferramenta da SourceForge e instalando-a em nosso sistema Debian, Devuan, Ubuntu ou derivados com os seguintes comandos:

```bash
sudo dpkg -i eggs_9.6.1_amd64.deb
sudo apt install -f
```

Com a instalação concluída, é hora de configurar a ferramenta. Optando pelo padrão, o Penguins' Eggs realiza automaticamente as configurações necessárias:

```bash
sudo eggs dad --default
```

Se houver a necessidade de mais espaço, o próprio Penguins' Eggs oferece sugestões, como adicionar um compartilhamento remoto ou uma partição local.

Para instalar a ISO gerada usando o instalador Calamares, execute:

```bash
sudo eggs calamares --install
```

Agora, estamos prontos para criar nossa primeira ISO. Para uma distribuição distribuível, utilize:

```bash
sudo eggs produce
```

Caso deseje criar uma cópia completa do seu sistema, utilize a opção `--clone`:

```bash
sudo eggs produce --clone
```

Além disso, é possível transferir um servidor para a internet de forma segura, sem expor diretamente os dados, usando a opção `--cryptedclone`:

```bash
sudo eggs produce --cryptedclone
```

Para obter máxima compressão e remover Penguins' Eggs e o instalador Calamares ao final da instalação, adicione os flags `--max --release`:

```bash
sudo eggs produce --max --release
```

A criação de ISOs personalizadas pode parecer uma jornada complexa, mas com o Penguins' Eggs, esse processo se torna acessível a usuários de todos os níveis. Sua simplicidade de uso aliada à versatilidade de opções, como clonagem e transferência segura de servidores, fazem desta ferramenta uma adição valiosa ao kit de ferramentas de qualquer entusiasta de Linux. Experimente o Penguins' Eggs e desbrave novos horizontes na customização do seu sistema operacional preferido.
