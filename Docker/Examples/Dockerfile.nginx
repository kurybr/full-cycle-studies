FROM nginx:latest

# RUN executa comandos dentro da Imagem
RUN apt-get update
RUN apt-get install vim -y

# WORKDIR =>  Diretório referenciado dentro do container.
WORKDIR /app

# Copia a pasta html para dentro da pasta nginx detro do container
COPY html /usr/share/nginx