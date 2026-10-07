# Respostas · Avaliação Prática de Docker · ViaSerra Transportes (Turma C)

Nome: MARIANA MARTINS DE SOUSA MELLO
Matrícula: 26174740
Usuário do GitHub: marimello16
Usuário do Docker Hub: marianamartinsmello

Responda com as suas palavras e com o que aconteceu na SUA máquina. Resposta curta e certa vale mais
do que texto longo copiado. Resposta que contradiz o seu próprio Dockerfile vale zero.

## Parte 1 · Dockerfile do portal

1. Qual imagem base você usou e qual o tamanho final da imagem do portal (saída de `docker images`)?

`nginx:1.27-alpine`. O tamanho final da imagem é aproximadamente **43.1 MB**.

2. Em qual pasta do container o Nginx procura os arquivos do site? Mostre o comando que você usou para
   conferir que o `index.html` está lá dentro.

A pasta é `/usr/share/nginx/html/`.
O comando para conferir o arquivo lá dentro foi:
`docker exec -it teste-portal ls -l /usr/share/nginx/html/`

## Parte 2 · Docker Hub

3. Nome completo da imagem publicada e link público do repositório no Docker Hub.

* **Nome completo da imagem:** `marianamartinsmello/viaserra-portal:1.0-26174740`
* **Link público:** `https://hub.docker.com/r/marianamartinsmello/viaserra-portal`

4. Se você mudar o HTML, quais comandos precisa rodar para que a versão nova chegue ao Docker Hub?

```cmd
docker build -t marianamartinsmello/viaserra-portal:1.0-26174740 ./portal
docker push marianamartinsmello/viaserra-portal:1.0-26174740