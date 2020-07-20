---
layout: post
title: "Protocolo HTTP"
description: Protocolo HTTP.
date: 2020-07-20 18:03:36 +0530
categories: Web
---

Saiba mais o que é e como funciona o Protocolo HTTP

# O que é o protocolo HTTP?

HTTP (HyperText Transfer Protocol) é um protocolo da camada de aplicação do modelo OSI que permite buscar recursos de um servidor na internet (client-server protocol). Isso significa que uma busca que começa pelo client, geralmente usando um browser, retorna um documento criado a partir de diferentes documentos buscados em servidores na internet.

Quando um cliente busca alguma informação de uma página web dizemos que ele está fazendo uma requisição, e tudo que é retornado a partir disso chamamos simplesmente de resposta.

O protocolo HTTP foi criado no início dos anos 90 e sofreu diversas mudanças ao longo dos anos. É um protocolo da camada de aplicação que é enviado por TCP ou por uma conexão TCP criptografada por TLS.

# Componentes dos sitemas baseados no protocolo HTTP

Como já citamos, o protocolo HTTP é um client-server protocol, o que significa que as requisições são enviadas por um usuário, na maior parte do tempo por meio de um browser. Mas as requisições também podem ser feitas por sistemas programados. Cada requisição é enviada para um servidor que faz o tratamento adequado e devolve uma resposta. Mas entre o cliente fazendo a requisição e o servidor devolvendo uma resposta existe uma série de entidades chamadas de proxies que atuam de diferentes formas para armazenar informações em cache ou fazer redirecionamentos para manter em tempo ágil o fluxo da requisição.

# Cliente

O cliente, ou user-agent, é qualquer entidade que seja capaz de realizar requisições para um servidor.
Para apresentar uma página da web, o navegador envia uma solicitação original para buscar o documento HTML que representa a página. Em seguida, analisa esse arquivo, fazendo solicitações adicionais correspondentes a scripts de execução, informações de layout (CSS) a serem exibidas e sub-recursos contidos na página (geralmente imagens e vídeos). O navegador da web combina esses recursos para apresentar ao usuário um documento completo, a página da Web.

# Servidor

No lado oposto ao cliente está o servidor, que devolve como resposta o documento HTML com o que foi solicitado pelo cliente.
Um servidor não é necessariamente uma única máquina, mas várias instâncias de software para servidor podem ser hospedadas na mesma máquina.

# Proxies

Os proxies fazem parte da camada intermediária de um fluxo de requisição-respota. Os proxies tratam as requisições e devolvem as respostas da melhor maneira para manter um bom desempenho. Algumas funções dos proxies:

- cache (armazena informações públicas ou privadas)
- filtragem (verificações de segurança)
- balanceamento de carga (permite que vários servidores atendam a diferentes solicitações)
- autenticação (controla o acesso a diferentes recursos)
- registro (permite o armazenamento de informações)
