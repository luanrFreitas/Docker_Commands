# Comandos Docker
## Índice

1. [Gerenciamento de Contêineres](#gerenciamento-de-contêineres)
2. [Gerenciamento de Imagens](#gerenciamento-de-imagens)
3. [Rede](#rede)
4. [Volume](#volume)
5. [Logs e Execução](#logs-e-execução)
6. [Outros Comandos](#outros-comandos)

---

## Gerenciamento de Contêineres

- `docker run <imagem>`: Executa um contêiner a partir de uma imagem.
    - `-it` : Abre um terminal interativo.
    - `-d` : Executa em segundo plano.
    - `-e` : Especifica variáveis de ambiente.
    - `-p` : Libera portas do contêiner <porta_host:porta_contêiner>
    - `--name` : Nomeia um conteiner.
- `docker start <contêiner>`: Inicia um contêiner existente.
- `docker stop <contêiner>`: Para a execução de um contêiner em execução.
- `docker restart <contêiner>`: Reinicia um contêiner.
- `docker rm <contêiner>`: Remove um contêiner.
- `docker ps`: Lista todos os contêineres em execução.
- `docker ps -a`: Lista todos os contêineres, incluindo os que estão parados.
- `docker inspect <contêiner>`: Exibe informações detalhadas sobre um contêiner.
- `docker cp <nome_arquivo> <nome_contêiner:pasta_destino>`: Copia arquivos entre entre a máquina local e um contêiner.

## Gerenciamento de Imagens

- `docker pull <imagem:tag>`: Baixa uma imagem do Docker Hub ou de um registro de contêiner.
- `docker images`: Lista todas as imagens disponíveis localmente.
- `docker rmi <imagem>`: Remove uma imagem.
- `docker build <caminho>`: Constrói uma imagem a partir de um Dockerfile no caminho especificado.
- `docker commit <contêiner> <imagem>`: Cria uma nova imagem a partir do estado atual de um contêiner.

## Rede

- `docker network ls`: Lista todas as redes disponíveis.
- `docker network create <nome>`: Cria uma nova rede.
- `docker network inspect <rede>`: Exibe informações detalhadas sobre uma rede.
- `docker network connect <rede> <contêiner>`: Conecta um contêiner a uma rede.
- `docker network disconnect <rede> <contêiner>`: Desconecta um contêiner de uma rede.

## Volume

- `docker volume ls`: Lista todos os volumes disponíveis.
- `docker volume create <nome>`: Cria um novo volume.
- `docker volume inspect <volume>`: Exibe informações detalhadas sobre um volume.
- `docker volume rm <volume>`: Remove um volume.

## Logs e Execução

- `docker logs <contêiner>`: Exibe os logs de um contêiner em execução.
- `docker exec -it <contêiner> <comando>`: Executa um comando dentro de um contêiner em execução.

## Outros Comandos

- `docker version`: Exibe a versão do Docker instalada.
- `docker info`: Exibe informações sobre o ambiente do Docker.
- `docker login`: Autentica-se em um registro de contêiner.
- `docker logout`: Desconecta-se de um registro de contêiner.
- `docker system prune`: Remove todos os contêineres parados, redes não utilizadas e imagens não utilizadas.

