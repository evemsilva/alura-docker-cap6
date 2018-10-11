# alura-docker
Projeto do curso de Docker

<h3>Comandos relacionados à informações</h3>

<b>docker version</b> - exibe a versão do docker que está instalada.

<b>docker inspect ID_CONTAINER</b> - retorna diversas informações sobre o container.

<b>docker ps</b> - exibe todos os containers em execução no momento.

<b>docker ps -a</b> - exibe todos os containers, independente de estarem em execução ou não.

<h3>Comandos relacionados à execução</h3>

<b>docker run NOME_DA_IMAGEM</b> - cria um container com a respectiva imagem passada como parâmetro.

<b>docker run -it NOME_DA_IMAGEM</b> - conecta o terminal que estamos utilizando com o do container.

<b>docker run -d -P --name NOME dockersamples/static-site</b> - ao executar, dá um nome ao container.

<b>docker run -d -p 12345:80 dockersamples/static-site</b> - define uma porta específica para ser atribuída à porta 80 do container, neste caso 12345.

<b>docker run -v "CAMINHO_VOLUME" NOME_DA_IMAGEM</b> - cria um volume no respectivo caminho do container.

<b>docker run -it --name NOME_CONTAINER --network NOME_DA_REDE NOME_IMAGEM</b> - cria um container especificando seu nome e qual rede deverá ser usada.

<h3>Comandos relacionados à inicialização/interrupção</h3>

<b>docker start ID_CONTAINER</b> - inicia o container com id em questão.

<b>docker start -a -i ID_CONTAINER</b> - inicia o container com id em questão e integra os terminais, além de permitir interação entre ambos.

<b>docker stop ID_CONTAINER</b> - interrompe o container com id em questão.

<h3>Comandos relacionados à remoção</h3>

<b>docker rm ID_CONTAINER</b> - remove o container com id em questão.

<b>docker container prune</b> - remove todos os containers que estão parados.

<b>docker rmi NOME_DA_IMAGEM</b> - remove a imagem passada como parâmetro.

<h3>Comandos relacionados à construção de Dockerfile</h3>

<b>docker build -f Dockerfile</b> - cria uma imagem a partir de um Dockerfile.

<b>docker build -f Dockerfile -t NOME_USUARIO/NOME_IMAGEM</b> - constrói e nomeia uma imagem não-oficial.

<b>docker build -f Dockerfile -t NOME_USUARIO/NOME_IMAGEM CAMINHO_DOCKERFILE</b> - constrói e nomeia uma imagem não-oficial informando o caminho para o Dockerfile.

<h3>Comandos relacionados ao Docker Hub</h3>

<b>docker login</b> - inicia o processo de login no Docker Hub.

<b>docker push NOME_USUARIO/NOME_IMAGEM</b> - envia a imagem criada para o Docker Hub.

<b>docker pull NOME_USUARIO/NOME_IMAGEM</b> - baixa a imagem desejada do Docker Hub.

<h3>Comandos relacionados à rede</h3>

<b>hostname -i</b> - mostra o ip atribuído ao container pelo docker (funciona apenas dentro do container).

<b>docker network create --driver bridge NOME_DA_REDE</b> - cria uma rede especificando o driver desejado.