
# Kafka Connect

Uma breve descrição sobre o que esse projeto faz e para quem ele é


## Instalação

Como Executar

- Adicionar mysql ao compose ou iniciar o mysql
 - Iniciar a infra com o docke-compose:
 ```bash
docker-compose up -d
```
- Adicionar o conector do mysql:
```bash
curl -X POST  -H  "Content-Type:application/json" http://localhost:8083/connectors -d @mysql.json
```


- Adicionar o conector do postgres:
```bash
curl -X POST  -H  "Content-Type:application/json" http://localhost:8083/connectors -d @postgres.json
```

- Conferir se o conector foi adicionado com sucesso:
```bash
http GET :8083/connectors
```
    