# Parte 1 - Nginx enviando para fluentd através do syslog na porta udp.

```
git checkout parte-1
docker-compose up --build 
```

# Parte 2 - Log do NGINX WAF (ModSecurity) e parser .

```
git checkout parte-2
docker-compose up --build 
curl "http://localhost:8180/foo?testparam=test"
curl "http://localhost:8180/foo?testparam=thisisatestofmodsecurity"
```

# Parte 3 - Logs sendo enviados para o ElasticSearch e Kibana

```
git checkout parte-3
docker-compose up --build 
curl "http://localhost:8180/foo?testparam=test"
curl "http://localhost:8180/foo?testparam=thisisatestofmodsecurity"
```

# Parte 3 - Demonstração de uma carga de dados para o Elastic Search e kibana.
```
git checkout parte-4.1
# realizar o download do arquivo de dados https://encurtador.com.br/kEFRU e extrair na pasta dados

docker-compose up --build 

curl "http://localhost:8180/foo?testparam=test"
curl "http://localhost:8180/foo?testparam=thisisatestofmodsecurity"

```
