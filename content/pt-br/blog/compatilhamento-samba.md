---
author: "Áleson Medeiros"
title: "Montando Compartilhamentos de Rede Windows no Linux: Um Guia Prático"
date: 2024-03-11
description: "Como criar e configurar de forma simples um compartilhamento samba no Linux"
draft: false
tags: ["samba", "smbfs", "cifs"]
thumbnail: "/smb-share.jpg"
---

Se você já se deparou com a necessidade de acessar diretórios compartilhados do Windows em seu servidor Linux, certamente sabe que pode ser uma tarefa desafiadora. Este tutorial foi criado para simplificar esse processo, guiando você passo a passo na montagem de compartilhamentos de rede Windows (CIFS ou SMBFS) no seu ambiente Linux. Vamos direto ao ponto!

### Requisitos:

Antes de começarmos, certifique-se de ter os seguintes requisitos:

- Acesso root no Linux.
- O caminho do compartilhamento do Windows (como //servidor/compartilhamento ou //192.168.0.1/compartilhamento).
- Um usuário e senha do Windows com permissões de acesso ao compartilhamento.

### Procedimento:

Faça login no Linux como root ou execute os comandos com o sudo.
Crie um diretório para montar o compartilhamento:

```bash
mkdir -p /mnt/windows
```
Use o comando `mount` para montar o compartilhamento no diretório criado:

```bash
mount -a
```
### Montagem Manual:

Para montar o compartilhamento casualmente em sua sessão, execute o seguinte comando:

```bash
mount -t cifs //servidor/compartilhamento -o username=usuario,password=senha /mnt/windows
```

Acesse o compartilhamento com os comandos:
```bash
cd /mnt/windows
ls -l
```
O diretório compartilhado agora está montado em seu servidor Linux!

### Fixando a Montagem:

Se deseja que o compartilhamento seja montado automaticamente na inicialização do seu servidor Linux, adicione a seguinte linha no final do arquivo `/etc/fstab`:

```bash
vim /etc/fstab
```
Adicione a linha:

```bash
//servidor/compartilhamento /mnt/windows cifs rw,username=usuario,password=senha 0 0
```
Se por acaso a montagem não funcionar, verifique as permissões do usuário no diretório Windows.

### Conclusão:

Neste tutorial, abordamos de maneira simples e prática como montar compartilhamentos de rede Windows no Linux. Ao seguir esses passos, você poderá facilmente integrar recursos compartilhados do Windows em seu ambiente Linux, melhorando a interoperabilidade entre sistemas operacionais. Lembre-se de ajustar as permissões conforme necessário e desfrute da integração eficiente entre o Linux e o Windows em seu servidor.