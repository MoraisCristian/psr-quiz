# PSR Quiz

# Ambiente de desenvolvimento PHP 8 com PHP-FPM, Nginx e MySQL, usando Docker e Docker Compose

Você precisa ter o Docker e o Docker Compose instalados em seu ambiente para rodar os containers.

Os três containers de serviço usados são:

- Um serviço `app` rodando PHP 8 FPM.
- Um serviço `db` rodando MySQL.
- Um serviço `nginx` que usa `app` para servir o aplicativo para o usuário final.

## Iniciando o ambiente

- Defina as variáveis de ambiente do MySQL criando um arquivo `.env` baseado no arquivo `.env.example`

- Crie a imagem do aplicativo com o seguinte comando:

```bash
docker-compose build app
```

- Quando o build estiver concluído, você poderá executar o ambiente em modo de segundo plano com:

```bash
docker-compose up -d
```

- Para visualizar os seus serviços ativos, rode o comando:

```bash
docker-compose ps