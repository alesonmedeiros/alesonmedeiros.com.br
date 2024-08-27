---
author: "Áleson Medeiros"
title: "Como instalar e usar o Openfortivpn no Linux"
date: 2024-08-26
description: "Instale e configure o Openfortivpn no Ubuntu para conexões VPN seguras"
draft: false
tags: ["vpn", "ubuntu", "terminal", "fortinet","openfortivpn"]
thumbnail: "/openfortivpn-linux.jpeg"
---

Muitas empresas utilizam VPNs para permitir que funcionários e clientes acessem sua rede local de forma segura pela internet. Um dos provedores de VPN mais populares é a FortiNET, conhecida por seus produtos de segurança confiáveis e práticos.

No entanto, o aplicativo oficial FortiClient para Linux não permite a conexão direta a uma VPN. Por isso, muitos usuários recorrem a clientes alternativos. Após enfrentar alguns problemas com outras soluções, descobri o Openfortivpn, um cliente de código aberto para Fortinet que funciona de maneira eficiente. Neste tutorial, vou ensinar como instalar e configurar o Openfortivpn no Ubuntu.

### Instalação

Ubuntu: Execute o seguinte comando para instalar o Openfortivpn:

```bash
sudo apt install openfortivpn
```

### Configuração
Depois de instalar o Openfortivpn, você precisará configurá-lo. O processo é simples e rápido.

O arquivo de configuração
Para evitar a necessidade de digitar seu usuário e senha sempre que conectar, você pode editar o arquivo de configuração do Openfortivpn e inserir suas credenciais lá. O arquivo está localizado em:

`/etc/openfortivpn/config`

Abra o arquivo com sudo em seu editor de texto:

```bash
sudo vim /etc/openfortivpn/config
```
O conteúdo do arquivo será assim:

```bash
host =
port =
username =
password =
```

Preencha os campos com as informações apropriadas, como no exemplo abaixo:

```bash
host = seu.servidorfortivpn.com
port = 10443
username = joao.silva
password = senha123
```

Se você usar um PIN + token gerado em tempo real para a senha, exclua o campo de senha do arquivo. Nesse caso, o Openfortivpn solicitará a senha quando você o usar.

### Configuração de certificado confiável
Se você encontrar um erro relacionado à validação do certificado, adicione o certificado confiável ao arquivo de configuração. O erro pode ser algo assim:

```bash
ERROR:  Gateway certificate validation failed, and the certificate digest is not in the local whitelist. If you trust it, rerun with:
ERROR:      --trusted-cert 6389a2c37974a6fc74763a2b6090asdfasdfw970ce21390df15ceeadcdce990dfd7
```

Para corrigir, copie o certificado fornecido e adicione ao arquivo de configuração:

```bash
trusted-cert = 6389a2c37974a6fc74763a2b6090asdfasdfw970ce21390df15ceeadcdce990dfd
```
### Execução
Depois de configurar o Openfortivpn, você pode conectá-lo executando:

```bash
sudo openfortivpn
```
Se tiver problemas ao usar o Openfortivpn, entre em contato através dos comentários ou do formulário de contato.

Se preferir uma interface gráfica, confira o [Openfortigui](https://github.com/theinvisible/openfortigui).