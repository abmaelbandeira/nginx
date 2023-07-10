# Configuração básica do Nginx

Este é um projeto básico que demonstra como configurar o servidor web Nginx usando o Docker Compose. O Nginx é um servidor web popular que pode ser usado para hospedar sites, aplicativos da web e outros serviços.

## Pré-requisitos

Certifique-se de ter o Docker e o Docker Compose instalados em sua máquina antes de prosseguir. Se você ainda não os tem instalados, siga as instruções em [Docker](https://docs.docker.com/get-docker/) e [Docker Compose](https://docs.docker.com/compose/install/) para instalá-los.

## Instruções

Siga os passos abaixo para configurar o Nginx usando este projeto:

1. Clone este repositório em sua máquina local.
```bash
git clone <URL_DO_REPOSITÓRIO>
```

2. Navegue até o diretório clonado.
```bash
cd <NOME_DO_DIRETÓRIO>
```

3. Inicie os contêiners do Nginx usando o Docker Compose.
```bash
docker-compose up -d
```

4. Instale o Bash e o nano dentro do contêiner do Nginx.
```bash
docker-compose exec nginx apk add bash nano
```

5. Edite o arquivo de configuração padrão do Nginx com base nos arquivos de exemplo: load_balance_example.txt ou reverse_proxy_example.txt
```bash
nano /etc/nginx/conf.d/default.conf
```

6. Verifique se a sintaxe do arquivo de configuração está correta.
```bash
nginx -t
```
Se a saída for semelhante à seguinte, significa que a sintaxe está correta:
nginx: the configuration file /etc/nginx/nginx.conf syntax is ok
nginx: configuration file /etc/nginx/nginx.conf test is successful

7. Reinicie o servidor Nginx para aplicar as alterações.
```bash
nginx -s reload
```

## Conclusão
Este projeto básico fornece um exemplo simples de como configurar o servidor Nginx usando o Docker Compose e usando load balancer. Você pode personalizar ainda mais a configuração do Nginx de acordo com suas necessidades específicas, consultando a documentação oficial do Nginx em nginx.org.
