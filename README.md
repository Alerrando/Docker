# Docker

### Executa o container e inicia uma imagem interativa no container
```
docker run -it <nome da imagem>
```

### Executar um comando dentro de um container e inicia uma imagem interativa no container
```
docker exec it <id do container>
```

### Deletar container
```
docker rm <nome do container>
```

### Mostrar quantos e quais containers estão sendo executados na sua máquina
```
docker ps
```

### Mostrar todos os containers que já foram executas na sua máquina
```
docker ps -a
```

### Exibe informações de uso de CPU, memória e rede.
```
docker stats
```

### Executar uma imagem de teste para testar o funcionamento do Docker
```
docker run hello-world
```

### Parar todos os processos que estão executando em um container
```
docker stop <id do container>
```