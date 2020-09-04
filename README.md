# CRUD de Notícias

Crud simples, exemplificando a utilização de Python (Flask) para a construção da API com autenticação JWT, interface do usuário construída em React e utilizando banco de dados nosql (MongoDB)

## Pré-requisitos

. Docker
. Python 3.7 ou superior (com virtualenv e pip)
. NodeJS

## Instalação

1) Clonar o repositório com o comando abaixo:

	git clone git@github.com:alessdr/crud-noticias.git

2) Baixar a imagem do MongoDB (Docker), com o seguinte comando:

	docker pull mongo

3) Criar um container com a imagem baixada:

	docker create -it --name Mongo -p 27017:27017 mongo

4) Inicializar o container criado:

	docker start Mongo

5) Ir para a pasta do projeto Python, criar uma virtualenv, ativa-la e instalar as dependências do mesmo:

	virtualenv API_ENV
	source API_ENV/bin/activate
	pip install -r requirements.txt

6) Criar na raíz do projeto Python um arquivo chamado **.env** e atribuir a ele o seguinte conteúdo

```
PORT=8000
DEBUG=False
THREADS=3
# Environment optios: PRD or DEV
ENVIRONMENT=PRD
JWT_SECRET_KEY = t1NP63m4wnBg6nyHYKfmc2TpCOGI4nss
SECRET_KEY = 5or414C3nP35p37R0Br45
DB_NAME=news
DB_HOST=127.0.0.1
DB_PORT=27017
```

7) Executar o projeto Python:

	python app.py

8) Ir para a pasta do projeto React e instalar suas dependencias

	npm install

9) Executar o projeto React

	npm start

10) Acessar o endereço abaixo

	http://127.0.0.1:3000


