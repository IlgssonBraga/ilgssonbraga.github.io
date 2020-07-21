---
layout: post
title: "Como instalar o Node.js no Fedora 32"
date: 2020-07-20 21:22:00 +0530
categories: Node.js
---

Nesse artigo vamos ver o passo a passo para instalar o Node.js no
Fedora 32 usando o NVM

# O que é o NVM?

NVM é um gerenciador de versões do Node.js. Ele foi criado para ser
instalado pelo usuário e invocado a partir da linha de comando do
terminal. É compatível com qualquer POSIX-compliant shell, ou seja,
qualquer terminal que respeite os padrões do POSIX. Pode ser instalado
em sistemas Unix, macOS e Windows. Aqui vamos fazer a instalação baseado no Fedora 32 Workstation.

# Instalando o NVM

Para instalar o NVM você pode rodar o [script de instalação](https://github.com/nvm-sh/nvm/blob/v0.35.3/install.sh), ou apenas rodar manualmente um dos comandos abaixo:

```bash

curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.35.3/install.sh | bash

```

```bash

wget -qO- https://raw.githubusercontent.com/nvm-sh/nvm/v0.35.3/install.sh | bash

```

Logo após precisamos linkar o conteúdo salvo em ~/.nvm ao perfil do usuário (~/.bash_profile, ~/.zshrc, ~/.profile, or ~/.bashrc).

```bash

export NVM_DIR="$([ -z "${XDG_CONFIG_HOME-}" ] && printf %s "${HOME}/.nvm" || printf %s "${XDG_CONFIG_HOME}/nvm")"
[ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh" # This loads nvm

```

Para verificar se tudo ocorreu da forma correta, podemos rodar:

```bash

nvm --version

```

# Node.js

Instalado o NVM, podemos agora gerenciar qual versão do Node.js nós queremos. O Node.js é um runtime Javascript orientado a eventos assíncronos. Ele foi construído para fazer aplicações escaláveis.

Para instalar o Node.js, precisamos apenas escolher a versão que queremos e rodar o comando abaixo:

```bash

nvm install 12.18.2

```

Nesse caso eu escolhi a versão 12.18.2 porque no momento desse post é a versão LTS (long-term support).

Para usar a versão instalada fazemos:

```bash

nvm use 12.18.2

```

E para mostrar qual versão está ativa no momento rodamos:

```bash

nvm exec node --version

```

Também podemos ver a versão do Node.js com o comando:

```bash

node --version

```

Com cada versão do Node.js também vem instalado o NPM (Node Package Manager) ou gerenciador de pacotes do Node.js. Podemos utilizar o NPM para instalar bibliotecas nos nossos projetos. Também podemos ver qual versão do NPM está instalada rodando:

```bash

npm --version

```

Agora com tudo configurado podemos dar início aos nossos projetos usando
Node.js.
