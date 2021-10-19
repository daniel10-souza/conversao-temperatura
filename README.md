# Conversão Temperatura

> Configuração usada no Dockerfile
> ---

FROM node:14.15.4 </br>
WORKDIR /app </br>
COPY package*.json ./ </br>
COPY . . </br>
CMD ["node", "app.js"] </br>
