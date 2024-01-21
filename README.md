# Implantação de chatbot com Flask e JavaScript

Neste tutorial foi implantado o chatbot criado [neste](https://github.com/python-engineer/pytorch-chatbot) tutorial com Flask e JavaScript.

Isso oferece 2 opções de implantação:

- Implante no aplicativo Flask com modelo jinja2
- Servir apenas a API de previsão do Flask. Os arquivos html e javascript usados ​​podem ser incluídos em qualquer aplicativo Frontend (com apenas uma ligeira modificação) e podem ser executados completamente separados do aplicativo Flask.

## Configuração inicial - no windows:
Este repositório contém atualmente os arquivos iniciais.

**Clone o Repositório e crie um ambiente virtual**

a) Clonando o repositório
b) Mudando para o repositório clonado
c) Criar um ambiente virtual usando o módulo venv
d) Ativando o ambiente virtual
```
git clone https://github.com/python-engineer/chatbot-deployment.git
cd chatbot-deployment
python -m venv venv
venv\Scripts\activate
```

Erro: [] O erro que você está enfrentando está relacionado à política de execução do PowerShell no Windows.
```
Get-ExecutionPolicy
Set-ExecutionPolicy RemoteSigned
```

Depois de concluir suas tarefas no ambiente virtual, você pode restaurar a política de execução para o valor original usando o comando:
``` Set-ExecutionPolicy <Restricted> ```


**Instalar dependências**
```
(venv) pip install Flask torch torchvision nltk
```
Erro: [] resolvido executando o comando que o proprio terminal deu ```python.exe -m pip install --upgrade pip```

**Instale o pacote nltk**
```
(venv) python
>>> import nltk
>>> nltk.download('punkt')
```

Erro: [] (venv) ```pip install nltk```
Depois pude voltar a instalar os comandos acimas dentro do ambiente python:


**Modifique `intents.json` com diferentes intenções e respostas para o seu Chatbot**

Rodar
```
$ (venv) python train.py
```

Erro[] precisava instalar a biblioteca do numPy ```pip install numpy``` e a do torch 

Isso irá despejar o arquivo data.pth. E então execute o seguinte comando para testá-lo no console.
```
$ (venv) python chat.py
```
Agora, para implantação, siga meu tutorial para implementar app.pye app.js.

## Assista o tutorial
[![Alt text](https://img.youtube.com/vi/a37BL0stIuM/hqdefault.jpg)](https://youtu.be/a37BL0stIuM)  
[https://youtu.be/a37BL0stIuM](https://youtu.be/a37BL0stIuM)

## Observaçao
No vídeo implementamos a primeira abordagem usando templates jinja2 em nosso aplicativo Flask. Apenas pequenas modificações são necessárias para executar o frontend separadamente. Coloquei o código de front-end final para um aplicativo de front-end independente na pasta standalone-frontend [standalone-frontend](/standalone-frontend).

## Creditos:
Este repositório foi usado para o código frontend:https://github.com/thascript/chatbot-deployment

