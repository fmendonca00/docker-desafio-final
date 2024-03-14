# Repositório Docker Compose da atividade desafio final do treinamento

### 1. docker-compose.yml

Este arquivo Docker Compose inclui a configuração para os bancos de dados e aplicações.

- PostgreSQL
- PGAdmin
- Traefik
- Nginx

Para iniciar a plataforma, utilize o seguinte comando:

```bash
docker stack deploy -c docker-compose.yml app
```

#### 1.2 Comandos utilizados durante esta atividade

Recuperando o código-fonte do GIT:

```bash
git clone https://github.com/fmendonca00/docker-desafio-final.git
```

Para iniciar a plataforma:

```bash
cd docker-desafio-final/
docker stack deploy -c docker-compose.yml app
```

Para remover a plataforma:

```bash
docker stack rm app
```

Atualizar o código e enviar para o repositório remoto:

```bash
git add .
git commit -m "update"
git push origin main
```

Atualizar o repositório local e posteriormente executar novo deploy da plataforma:

```bash
git pull
```

Analise dos logs da plataforma:

```bash
docker service ls
docker service logs -f app_pgadmin
docker service logs -f app_postgres
docker service logs -f app_nginx
docker service logs -f app_traefik
```

Analise do ambiente:

```bash
docker service ls
docker stack ls
docker node ls
docker network ls
docker node ps $(docker node ls -q)
```
