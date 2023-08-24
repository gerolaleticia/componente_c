# Microserviço: API Wave Prediction

Este projeto faz parte da entrega da sprint 3 do curso de pós graduação em **Engenharia de Software - PUC Rio** 

O objetivo da aplicação é trazer, em uma única tela interativa, as previsões de ondas do litoral paulista considerando direção da ondulação, direção do vento, tamanho de onda esperado (rotas inputadas por esta API) e uma sugestão de traje de banho considerando a temperatura prevista (inputadas por API externa, checar documentação do componente A). 

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
(env)$ flask run --host 0.0.0.0 --port 5000
```

Em modo de desenvolvimento é recomendado executar utilizando o parâmetro reload, que reiniciará o servidor automaticamente após uma mudança no código fonte.

```
(env)$ flask run --host 0.0.0.0 --port 5000 --reload
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


