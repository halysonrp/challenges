## > :construction: Projeto em construção :construction:

## ⚠ Descrição

`` História: Descreve de forma narrativa uma necessidade que uma persona necessita usando como premissa as perguntas: Quem?, O que? e o Motivo? da necessidade. Possui critérios de aceite como regra de aceitação do suprimento da necessidade. 
``

## 💡 Visão de Negócio


### Descrição funcional da História

Eu, como: PO <br />
Quero: Construir uma API que possibilite a criação de pedidos e Pagamentos <br />
Para: atender o site e demais aplicações que queiram criar pedidos e transacionar pagamentos <br />

## Critérios de aceite
[Escreva seu texto aqui]

## 🎯 Visão técnica da solução

### Desenho de Arquitetura da Solução - Diagrama de Container (C2)

![MS Order Arquitetura (C4Model) (3)](https://user-images.githubusercontent.com/12093535/185700705-748553c2-4a57-4052-abf9-7c8bbf2b1a2a.jpg)

### Detalhes técnicos *

Na busca com filtros deverá ser usada ..... no exemplo abaixo:

```
	@Column(name = "FL_PAGO")
	@SearchField
	private Integer flagPaid;
```

## :hammer: Funcionalidades do projeto
#### 🛒 Micro Serviço de Pedidos 
- `Funcionalidade 1`: O novo micro serviço deve permitir a criação de novos Pedidos.
- `Funcionalidade 2`: O microservice deve permitir recuperar pedidos através do id do pedido, Número do pedido e CPF do Cliente.
- `Funcionalidade 3`: O Microservice deve ter um campo para armazenar o status do pedido, esse campo deve possuir apenas 3 status possíveis:
	- Pedido Criado
	- Pagamento Confirmado
	- Pagamento não Autorizado
- `Funcionalidade 3.1`:A Alteração de status do pedido só deve acontecer através de mensageria.
- `Funcionalidade 4`: O Microservice deve notificar sempre que houver uma criação de pedido.

#### 💲 Micro Serviço de Pagamentos
- `Funcionalidade 1`: O microservice deve permitir recuperar pagamentos através do id do pagamento e CPF do Cliente.
- `Funcionalidade 2`: A criação de um pagamento deve acontecer apenas por mensageria.
- `Funcionalidade 3`: O Microservice deve ter um campo para armazenar o status do pagamento, esse campo deve possuir apenas 2 status possíveis:
	- Pagamento Confirmado
	- Pagamento não Autorizado
- `Funcionalidade 4`: O microservice deve propagar atualizações de status de pagamento através de mensageria.
- `Funcionalidade 4`: Pagamentos com valor maior que R$1.000 não devem ser autorizados.
- `Funcionalidade 5`: Pagamentos com valor menor que R$1.000 devem ser autorizados.

## 🎯 Desafio - O que será avaliado?
1. Espera-se que o aluno desenvolva uma breve explicação dos entregáveis através do README.md do projeto.
2. Será avaliado como você condificou a aplicação para produzir e consumir mensagens.
3. O contrato da sua aplicação deve ser bem documentada utilizando o framework Swagger.
4. Também iremos considerar a abordagem utilizada para testar o fluxo da sua aplicação (testes unitários e de integração).
5. Como você dividiu as camadas e responsabilidades da sua aplicação.
6. Boas praticas do HTTP status.
7. Uso de clean code será visto como diferencial.
8. No final do projeto deve ser publicado um vídeo de no maximo 5 minutos explicando as principais funcionalidades do seu projeto. O link deve ser disponibilizado através do readme do projeto.

## ✔️ Observações adicionais
1. Use a sua imaginação na escolha dos objetos e atributos para cada api.
2. Como mensageria pode ser utilizado RabbitMQ ou Kafka.
3. O banco de dados fica a escolha do aluno, podendo ser utilizado, MySql, Oracle, Postgress, MongoDB ou até mesmo o H2.


**Indique como é possível baixar ou acessar o código fonte do projeto, seja projeto inicial ou final**

## 🛠️ Abrir e rodar o projeto

**Apresente as instruções necessárias para abrir e executar o projeto**
