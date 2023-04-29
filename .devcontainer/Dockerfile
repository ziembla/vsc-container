ARG VARIANT
FROM mcr.microsoft.com/vscode/devcontainers/typescript-node:0-${VARIANT}

##############################
ARG GIT_NAME=ziembla
ARG GIT_EMAIL=woj@ziembla.com
##############################

# [Optional] Uncomment this section to install additional OS packages.
# RUN apt-get update && export DEBIAN_FRONTEND=noninteractive \
#     && apt-get -y install --no-install-recommends <your-package-list-here>

USER node
RUN printf "\nalias ll='ls -l'\n" >> $HOME/.bashrc
RUN printf "\nif [ -f ~/.bashrc ]; then . ~/.bashrc; fi'\n" >> $HOME/.bash_profile
RUN printf "\n[user]\n\tname = ${GIT_NAME}\n\temail = ${GIT_EMAIL}\n" >> $HOME/.gitconfig

RUN npm install -g npm@latest
RUN npm install -g pnpm@latest
RUN npm install -g vsce@latest
RUN npm install -g yo generator-code
