---
author: "Áleson Medeiros"
title: "Como Exibir o Menu de Contexto Completo no Windows 11"
date: 2024-08-29
description: "Aprenda a restaurar o menu de contexto completo no Windows 11 com este simples tutorial de configuração no Editor de Registro"
draft: false
Mtags: ["Windows", "Menu", "Win11", "Completo"]
thumbnail: "/menu-contexto-completo-windows-11-00.jpg"
---

O Windows 11 introduziu um novo menu de contexto simplificado que aparece ao clicar com o botão direito do mouse, mas nem todos os usuários gostam dessa mudança. Se você prefere o menu de contexto completo do Windows 10, onde não precisa clicar em "Mostrar mais opções", este tutorial vai te guiar na configuração necessária para reverter ao menu antigo.

![Menu de Contexto](/menu-contexto-completo-windows-11-01.png)

### Passos para Configuração

1. Abrir o Editor de Registro

* Pressione Windows + R no seu teclado.
* Na janela "Executar", digite regedit e pressione Enter. Isso abrirá o Editor de Registro do Windows.

2. Navegar até a Chave Necessária

* No Editor de Registro, navegue até o seguinte caminho:

```objectivec
Computador\HKEY_CURRENT_USER\Software\Classes\CLSID
```

3. Criar uma Nova Chave

![Editor de Registro](/menu-contexto-completo-windows-11-02.png)

* Clique com o botão direito na pasta `CLSID`.
* Selecione `Novo` > `Chave`.
* Nomeie a nova chave como:

```objectivec
{86ca1aa0-34aa-4e8b-a509-50c905bae2a2}
```

![Editor de Registro](/menu-contexto-completo-windows-11-03.png)

4. Criar uma Subchave

* Clique com o botão direito na chave `{86ca1aa0-34aa-4e8b-a509-50c905bae2a2}` que você acabou de criar.
* Selecione `Novo` > `Chave`.
* Nomeie a nova chave como:

![Editor de Registro](/menu-contexto-completo-windows-11-04.png)

```objectivec
{86ca1aa0-34aa-4e8b-a509-50c905bae2a2}
```
![Editor de Registro](/menu-contexto-completo-windows-11-04.png)

5. Finalizar a Configuração

* Clique duas vezes na chave `InprocServer32`.
* Em seguida, exclua o valor `Padrão` que foi criado automaticamente.
* Feche o Editor de Registro.

![Menu de Contexto Completo](/menu-contexto-completo-windows-11-05.png)

6. Reiniciar o Sistema

* Para que as alterações tenham efeito, reinicie o seu computador.

Após seguir esses passos, o menu de contexto completo do Windows 11 aparecerá ao clicar com o botão direito do mouse, sem a necessidade de selecionar "Mostrar mais opções".

![Menu de Contexto Completo](/menu-contexto-completo-windows-11-06.png)

Agora você tem o menu de contexto completo do Windows 11, o que pode facilitar o acesso a várias opções com um clique. Essa configuração simples pode melhorar sua experiência de uso, especialmente se você estiver acostumado ao menu do Windows 10.