
# api-Should-I-go

Projeto que sobe um Container e, neste, uma API RESTful com o Swagger.

## 📦 Estrutura do Projeto

```
core-swagger-api/
├── Dockerfile.dev
├── docker-compose.yml
├── service/
├── setup.py
...
```

## 🚀 Entrega Contínua (CD) com GitHub Actions

Este repositório está configurado com GitHub Actions para realizar deploy automático da imagem Docker no Docker Hub.

### 🔧 Etapas do Workflow

- **Build da imagem Docker** usando o `Dockerfile.dev`
- **Push da imagem** para o Docker Hub ao fazer push na branch `master`

### 📁 Local do workflow

O arquivo de configuração está em:

```
.github/workflows/deploy.yml
```

### 🐳 Docker Hub

As imagens são publicadas no Docker Hub sob o repositório:

```
https://hub.docker.com/r/<seu-usuário>/simple-choose-app
```

### 🔐 Secrets utilizados

No repositório GitHub, os seguintes secrets devem ser configurados em **Settings > Secrets > Actions**:

- `DOCKERHUB_USERNAME`: seu nome de usuário do Docker Hub
- `DOCKERHUB_TOKEN`: token de acesso gerado no Docker Hub

## 🧪 Execução local

Para executar a aplicação localmente com Docker:

```
docker-compose build
docker-compose up
```

## 👨‍💻 Autores

* **Iaquine** - *Finalização*

---

Template baseado em: https://gist.github.com/PurpleBooth/109311bb0361f32d87a2
