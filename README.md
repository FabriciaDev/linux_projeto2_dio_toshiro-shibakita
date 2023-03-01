# Docker: Utilização prática no cenário de Microsserviços
## Denilson Bonatti, Instrutor - Digital Innovation One

Muito se tem falado de containers e consequentemente do Docker no ambiente de desenvolvimento. Mas qual a real função de um container no cenários de microsserviços? Qual a real função e quais exemplos práticos podem ser aplicados no dia a dia? Essas são algumas das questões que serão abordadas de forma prática pelo Expert Instructor Denilson Bonatti nesta Live Coding. IMPORTANTE: Agora nossas Live Codings acontecerão no canal oficial da dio._ no YouTube. Então, já corre lá e ative o lembrete! Pré-requisitos: Conhecimentos básicos em Linux, Docker e AWS.

o projeto é usado um supermercado fictício em que uma aplicação, no caixa, consulta os dados do produto em um data center no prório supermercado. Quando durante uma expansão o supermercado, a´pos  análise, decidiu migrar para as "nuvens".

Foi decidido também quebrar a aplicação até então "monolítica", ou seja uma coisa só, em microserviços, ou seja dividir a aplicação em vários pequenos pedaços a fim de ter melhor performace. Um detalhe interessante a respeito de microserviços é que os serviços não precisam estarescritos sempre na mesma linguagem.

Neste projeto foi utilizado o Docker Swarm, que é cluster (conjunto de nós) de container de docker.
Para esse projeto foi criado 3 maquinas virtuais no aws. Em uma delas a máquina foi aberta através do PuTTY e rodada uma aplicação para a criação de um banco dados, o arquivo "banco.sql".

Depois foi criada uma aplicação para teste em php dentro de "/var/lib/volumes/app/_data#" de nome "index.php". No vídeo o arquivo foi criado com o nano, que roda sem interface gráfica, considerada uma má pratica quando se trata de uso de servidores.

Foi instruido pequenos detalhes no código para modificar conforme o sistema.

Foi executado o Docker Run com o comando: run --name web-server -dt -p 80:80 --mount type-volume.src-app.dst=/app/ webdevops/php-apache:alpine-php7

Obs . --name é o nome do web server quw roda na porta 80:80

A fim de verificar se apenas um servidor é suficiente, foi feito teste de estresse. No exemplo da foi utilizado o site https://loader.io/

O servidor é interrompido com o comando: "docker ps"

Cria-se então um Docker Swarn como o comando: "docker swarn init"


