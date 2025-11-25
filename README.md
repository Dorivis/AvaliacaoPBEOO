# Avaliação sobre Django!

Gostaria de informá-lo que, no decorrer do dia de hoje, será realizada uma avaliação com foco central no universo conceitual e prático das tecnologias relacionadas ao Django REST Framework (DRF), APIs e documentação. A avaliação abrangerá os aspectos mais relevantes explorados ao longo do período letivo, considerando tanto os fundamentos teóricos quanto as práticas aplicadas envolvendo o DRF.

Esta avaliação foi planejada para proporcionar um espaço de reflexão crítica sobre os principais conceitos que sustentam o desenvolvimento de APIs utilizando o Django REST Framework, com ênfase na criação, implementação e documentação de endpoints e serviços RESTful. O objetivo é avaliar não apenas a capacidade de memorização dos conteúdos, mas, principalmente, a competência em aplicar esses conhecimentos de forma estruturada, eficaz e funcional em cenários reais de desenvolvimento.

Dessa forma, espera-se que vocês mobilizem seus conhecimentos prévios e os articulem com as práticas realizadas em aula, demonstrando a habilidade de desenvolver APIs com DRF de forma segura, eficiente e bem documentada. Além disso, será essencial a capacidade de compreender e aplicar boas práticas de documentação de código e de endpoints, utilizando as ferramentas e recursos discutidos ao longo do curso — como serializers, viewsets, routers e ferramentas de documentação automática — para garantir que o sistema seja claro, padronizado e fácil de usar, tanto para desenvolvedores quanto para usuários.

## 📌 Instruções da avaliação:

Mas, respire fundo… porque **hoje não terá avaliação!**. Em vez da prova,vocês irão criar um projeto em django

## 📌 1. O que é Django Rest Framework (DRF)?

Pesquise e responda:

- O que é o DRF?  
- Para que ele serve?  
- Quais são suas vantagens?  
- Que problemas ele resolve em relação ao Django tradicional?

## 📌 2. Instalação e Configuração Inicial

Pesquise:

- Como instalar o DRF em um projeto Django existente.  
- Como habilitar o DRF no arquivo `settings.py` usando `INSTALLED_APPS`.  
- O que significa ter `'rest_framework'` dentro de `INSTALLED_APPS`.




## 📌 3. O que é o decorator `@api_view`?

Pesquise:

- Para que serve o decorator `@api_view`.  
- Quais métodos HTTP ele aceita.  
- Como funciona o controle de métodos, por exemplo:

```python
@api_view(['GET', 'POST'])
```
 - Por que ele é considerado parte da abordagem funcional do DRF.

 ## 📌 4. Criando uma API Simples usando @api_view
 Você deve pesquisar como criar endpoints que realizem:

### a) GET

 - Criar uma view que retorne uma lista simples (ex.: produtos, tarefas, alunos).
 - Pesquisar como retornar JSON utilizando Response.

### b) POST

 - Criar uma view que receba dados enviados pelo cliente e os retorne ou salve temporariamente em uma lista em memória.
 - Pesquisar como acessar dados enviados no corpo da requisição usando request.data.

### c) DELETE

 - Criar uma view que delete um item (em memória ou no banco).
 - Pesquisar como receber parâmetros pela URL:

``` bash
api/item/<int:id>/
```

 ## 📌 5. Rotas (URLs)
 Pesquise:
  - Como registrar suas views no arquivo urls.py.
  - Diferenças entre rotas de Django tradicional e rotas usando views funcionais com DRF.

## Entrega

Seu trabalho deve conter:
 1. Explicações teóricas de todos os tópicos acima.
 2. Trechos de código pesquisados e comentados.
 3. Um passo a passo mostrando como criar uma mini API contendo:
     - 1 rota GET
     - 1 rota POST
     - 1 rota DELETE

 4. Prints mostrando seus testes no Insomnia ou Postman.
