# Microserviço: API Wave Prediction

<p float="left">

 <img src="https://user-images.githubusercontent.com/59067501/267109015-98556724-6c57-4212-9d5f-36a9a0b20426.jpg" width="600" />

Componente C que representa o mciroserviço Wave Prediction, construído como parte do MVP da Sprint 3 da Pós Graduação em Engenharia de Software (PUC-RIO).

O objetivo da aplicação é trazer, a partir de uma interação com o front-end Let Me Sea (componente A), as previsões de ondas do litoral paulista considerando direção da ondulação, direção do vento, tamanho de onda esperado (rotas inputadas por esta API).

O objetivo principal é facilitar a organização e programação dos surfistas da cidade. 

---

## Instalação

Será necessário ter todas as libs python listadas no requirements.txt instaladas. Após clonar o repositório, é necessário ir ao diretório raiz, pelo terminal, para poder executar os comandos descritos abaixo.

É fortemente indicado o uso de ambientes virtuais do tipo virtualenv.

```
(env)$ pip install -r requirements.txt
```

Este comando instala as dependências/bibliotecas, descritas no arquivo requirements.txt.

## Executando o servidor
Para executar a API basta executar:

```
(env)$ flask run --host 0.0.0.0 --port 5002
```

Em modo de desenvolvimento é recomendado executar utilizando o parâmetro reload, que reiniciará o servidor automaticamente após uma mudança no código fonte.

```
(env)$ flask run --host 0.0.0.0 --port 5002 --reload
```

## Acesso no browser
Abra o [http://localhost:5002/#/](http://localhost:5002/#/) no navegador para verificar o status da API em execução.

## Como executar através do Docker


Certifique-se de ter o Docker instalado e em execução em sua máquina.

Navegue até o diretório que contém o Dockerfile e o requirements.txt no terminal. Execute como administrador o seguinte comando para construir a imagem Docker:

```
(env)$ docker build -t componente-c .
```

Uma vez criada a imagem, para executar o container basta executar, como administrador, seguinte o comando:

```
(env)$ docker run -p 5002:5002 componente-c
```

Uma vez executando, para acessar a API, basta abrir o [http://localhost:5002/#/](http://localhost:5002/#/) no navegador para verificar o status da API em execução.


