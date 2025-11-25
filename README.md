# Avaliação sobre Django!

Gostaria de informá-lo que, no decorrer do dia de hoje, será realizada uma avaliação com foco central no universo conceitual e prático das tecnologias relacionadas ao Django REST Framework (DRF), APIs e documentação. A avaliação abrangerá os aspectos mais relevantes explorados ao longo do período letivo, considerando tanto os fundamentos teóricos quanto as práticas aplicadas envolvendo o DRF.

Esta avaliação foi planejada para proporcionar um espaço de reflexão crítica sobre os principais conceitos que sustentam o desenvolvimento de APIs utilizando o Django REST Framework, com ênfase na criação, implementação e documentação de endpoints e serviços RESTful. O objetivo é avaliar não apenas a capacidade de memorização dos conteúdos, mas, principalmente, a competência em aplicar esses conhecimentos de forma estruturada, eficaz e funcional em cenários reais de desenvolvimento.

Dessa forma, espera-se que vocês mobilizem seus conhecimentos prévios e os articulem com as práticas realizadas em aula, demonstrando a habilidade de desenvolver APIs com DRF de forma segura, eficiente e bem documentada. Além disso, será essencial a capacidade de compreender e aplicar boas práticas de documentação de código e de endpoints, utilizando as ferramentas e recursos discutidos ao longo do curso — como serializers, viewsets, routers e ferramentas de documentação automática — para garantir que o sistema seja claro, padronizado e fácil de usar, tanto para desenvolvedores quanto para usuários.

## 📌 Instruções da avaliação:

Mas, respire fundo… porque **hoje não terá avaliação!**. Em vez da prova,vocês irão criar um projeto em django



## 📌 CONTEXTO

Você e sua equipe foram contratados por uma rede de restaurantes chamada **Sabor Super Logico** para modernizar a gestão do seu negócio. Atualmente, os restaurantes ainda utilizam processos manuais e planilhas para controlar clientes, pedidos, produtos, funcionários, mesas, fornecedores e estoque, o que gera erros, retrabalho e demora no atendimento.

O objetivo do seu projeto é desenvolver uma API RESTful usando **Django** + **Django REST Framework** para digitalizar e automatizar todas essas operações. Com a API, será possível:

 - Cadastrar, listar, atualizar e deletar clientes, funcionários, produtos, mesas, fornecedores e pedidos;
 - Registrar e gerenciar pagamentos de pedidos;
 - Consultar o histórico de pedidos de um cliente;
 - Verificar produtos disponíveis em estoque;
 - Facilitar a integração com futuras aplicações front-end, como apps de pedidos online ou sistemas de gestão interna.
 - 
Com esta API, o restaurante **Sabor Super Logico** poderá reduzir erros, agilizar o atendimento e melhorar a experiência de seus clientes, enquanto mantém um controle eficiente sobre suas operações diárias.


### Projeto
Criar um projeto django chamado **sabor_super_logico**

### Aplicação
Criar uma aplicação chamada **restaurante_api**

### Modelos
Seguindo o diagrama a seguir, você deve montar todos os models necessários para o desenvolvimento da aplicação

![DER](https://github.com/Dorivis/AvaliacaoPBEOO/blob/main/databaseProjeto.png)


### Endpoints
### Para clientes:
 **Descrição**: Cadastro de clientes do restaurante.
 - GET /clientes/ → Listar todos os clientes
 - GET /clientes/<id>/ → Detalhes de um cliente específico
 - POST /clientes/ → Criar um cliente
 - PUT /clientes/<id>/ → Atualizar informações de um cliente
 - DELETE /clientes/<id>/ → Remover um cliente

### Para funcionários
 **Descrição**: Cadastro de funcionários do restaurante (garçons, cozinheiros, caixas).
 - GET /funcionarios/ → Listar funcionários
 - GET /funcionarios/<id>/ → Detalhes
 - POST /funcionarios/ → Criar funcionário
 - PUT /funcionarios/<id>/ → Atualizar funcionário
 - DELETE /funcionarios/<id>/ → Remover funcionário

### Para Categorias de Produtos
 **Descrição**: Classificação dos produtos (bebidas, lanches, sobremesas).
 - GET /categorias/
 - GET /categorias/<id>/
 - POST /categorias/
 - PUT /categorias/<id>/
 - DELETE /categorias/<id>/

### Para Produtos
 **Descrição**: Produtos vendidos no restaurante.
 - GET /produtos/ → Listar produtos
 - GET /produtos/<id>/ → Detalhes do produto
 - POST /produtos/ → Criar produto
 - PUT /produtos/<id>/ → Atualizar produto
 - DELETE /produtos/<id>/ → Remover produto

### Para Ingredientes
 **Descrição**: Ingredientes que compõem os produtos (controle de estoque).
 - GET /ingredientes/
 - GET /ingredientes/<id>/
 - POST /ingredientes/
 - PUT /ingredientes/<id>/
 - DELETE /ingredientes/<id>/

### Para Mesas
 **Descrição**: Gerenciamento das mesas do restaurante.
 - GET /ingredientes/
 - GET /ingredientes/<id>/
 - POST /ingredientes/
 - PUT /ingredientes/<id>/
 - DELETE /ingredientes/<id>/

### Para Pedidos
 **Descrição**: Registro de pedidos realizados pelos clientes.
 - GET /pedidos/ → Listar pedidos
 - GET /pedidos/<id>/ → Detalhes do pedido
 - POST /pedidos/ → Criar pedido
 - PUT /pedidos/<id>/ → Atualizar pedido (status, itens)
 - DELETE /pedidos/<id>/ → Cancelar pedido

### Para Itens de Pedido
 **Descrição**: Produtos incluídos em cada pedido.
 - GET /itenspedido/ → Listar itens
 - POST /itenspedido/ → Adicionar item a um pedido
 - PUT /itenspedido/<id>/ → Atualizar quantidade
 - DELETE /itenspedido/<id>/ → Remover item do pedido

### Para Pagamentos
 **Descrição**: Registro de pagamentos de pedidos.
 - GET /pagamentos/
 - GET /pagamentos/<id>/
 - POST /pagamentos/ → Registrar pagamento
 - PUT /pagamentos/<id>/ → Atualizar informações
 - DELETE /pagamentos/<id>/

### Para Fornecedores
 **Descrição**: Fornecedores de ingredientes e produtos.
 - GET /pagamentos/
 - GET /pagamentos/<id>/
 - POST /pagamentos/ → Registrar pagamento
 - PUT /pagamentos/<id>/ → Atualizar informações
 - DELETE /pagamentos/<id>/

### Para Compras
 **Descrição**: Registro de compras realizadas com fornecedores, atualizando estoque.
 - GET /compras/ → Listar compras
 - GET /compras/<id>/ → Detalhes da compra
 - POST /compras/ → Registrar compra
 - PUT /compras/<id>/ → Atualizar compra
 - DELETE /compras/<id>/ → Remover compra

**Dica: Reparem que tem metodos com o mesmo endpoint, por exemplo GET /itenspedido/ e POST /itenspedido/ , nesses casos usar o @api_view(['GET', 'POST'])**

### Documentação
<span style="color: red;"> Deve ser feita a documentação de sua API. </span>

### Lembrete
 - O código deve seguir boas praticas, ou seja,
    - nome de classes, variaveis, objetos. Seguindo o padrão devido.
    - <pre style="background-color: red;">COMENTÁRIOS</pre>
    - Seguir o mesmo padrão durante seu codigo, por exemplo: Se estiver usando camelCase, manter o camelCase e não mudar para snake_case, o mesmo vale para o contrario
    - 
