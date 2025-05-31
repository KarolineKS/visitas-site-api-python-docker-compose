# Contador de Visitantes

Uma API simples em Flask que conta visitantes usando PostgreSQL.

## 🚀 Como executar

1. Clone o repositório:

```bash
git clone https://github.com/seu-usuario/contador-visitantes.git

```

2. Subir a aplicação

```bash
docker-compose up -d
```

3. Acessar a API

```bash
curl http://localhost:5005/visitantes
```

## 📋 Endpoints

- `GET /visitantes` - Retorna o número total de visitas

## 🛠️ Tecnologias

- **Flask** - Framework web Python
- **PostgreSQL** - Banco de dados
- **Docker** - Containerização

## 📁 Estrutura

.
├── app/
│ ├── app.py # Aplicação Flask
│ ├── Dockerfile # Container da aplicação
│ └── requirements.txt # Dependências Python
└── docker-compose.yml # Orquestração dos containers

## 📦 Dependências

- Flask
- psycopg2-binary

## 🔧 Configuração

A aplicação roda na porta `5005` e se conecta automaticamente ao PostgreSQL configurado no Docker Compose.

Cada acesso ao endpoint `/visitantes` incrementa o contador e retorna o total atual.

### Comandos Docker Compose Importantes

```bash
docker-compose up -d # Iniciar os containers
docker-compose up -d --build # Iniciar os containers e reconstruir a imagem
docker-compose down # Parar os containers
docker-compose down -v # Parar os containers e remover o volume
docker-compose logs -f # Ver os logs
docker-compose exec app bash # Acessar o container
docker-compose exec db bash # Acessar o container do banco de dados
```
