## Execução e Gerenciamento de Containers

### Executar uma imagem interativa
```
docker run -it <nome_da_imagem>
```

### Executar um comando dentro de um container existente
```
docker exec -it <id_do_container> <comando>
```

### Parar um container em execução
```
docker stop <nome_do_container ou id>
```

### Deletar um container
```
docker rm <nome_do_container ou id>
```

### Listar containers em execução
```
docker ps
```

### Listar todos os containers
```
docker ps -a
```

### Exibir informações de uso de recursos
```
docker stats
```

## Gerenciamento de Imagens e Redes

### Construir uma imagem a partir de um Dockerfile
```
docker build -t <nome_da_imagem> .
```

### Criar uma rede
```
docker network create <nome_da_rede>
```

### Conectar um container a uma rede existente
```
docker network connect <nome_da_rede> <nome_do_container>
```

### Inspecionar uma rede
```
docker network inspect <nome_da_rede>
```

## Exemplos

### Executar uma imagem de teste
```
docker run hello-world
```

### Criar um container MySQL
```
docker run -p 3307:3306 --name mysqldb -e MYSQL_ROOT_PASSWORD=14725836 -e MYSQL_DATABASE=bank mysql:latest
```

### Criar um container customizado para uma aplicação
```
docker run -p 9090:9090 --name bank --net bank-net -e MYSQL_HOST=mysqldb -e MYSQL_DATABASE=bank -e MYSQL_USER=root -e MYSQL_ROOT_PASSWORD=14725836 bank
```