# Sistema de casa de eventos turma 1025

![Print da Homepage](https://i.ibb.co/0BLwdMW/Screenshot-2024-02-19-at-16-30-28.png)

## Tecnologias Utilizadas

- React
- Vite
- Node v20.5.1

## Dependências Utilizadas

- React Router
- Styled Components
- Axios
- React Toastify
- Json Server

## Participantes do projeto

- Aluno 01
- Aluno 02
- Aluno 03

## Responsaveis pelo desenvolvimento:

### Aluno 01

- Criou o componente de rotas
- Foi responsável pelo CSS

### Aluno 02

- Criou a página de login
- Criou o Componente de cabeçalho

## Instruções de Instalação

Clonar o projeto com o comando abaixo:

```sh
git clone https://github.com/roofranklin/casa-de-eventos-react.git
```

Entrar na pasta do projeto

```sh
cd casa-de-eventos-react
```

Instalar as dependencias

```sh
npm install
```

Instalar de maneira global o json-server (Caso você ainda não possua)

```sh
npm install -g json-server
```

## Instruções para rodar o projeto

Digitar o comando abaixo para rodar em desenvolvimento

```sh
npm run dev
```

Digitar o comando abaixo para rodar o mock local

```sh
json-server --watch eventos.json
```

### _Pronto! Seu projeto já estará rodando no endereço http://localhost:5173_

# Implementação de conteinerização

## Compose com build

```sh
docker compose -f docker-compose.toBuild.yml up -d --build
```

## Buildando as imagens no registry de exemplo `renzosa`

```sh
MY_REGISTRY=renzosa
docker buildx build -t ${MY_REGISTRY}/eventos-frontend .
docker buildx build -t ${MY_REGISTRY}/eventos-backend .

docker login
docker push ${MY_REGISTRY}/eventos-frontend
docker push ${MY_REGISTRY}/eventos-backend
```

### Exemplo de Compose com imagens do registry `renzosa`

```sh
docker compose -f docker-compose.renzosa.yml up -d
```
