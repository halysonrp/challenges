## > :construction: Projeto em construção :construction:

## ⚠ Descrição

`` História: Descreve de forma narrativa uma necessidade que uma persona necessita usando como premissa as perguntas: Quem?, O que? e o Motivo? da necessidade. Possui critérios de aceite como regra de aceitação do suprimento da necessidade. 
``

## 💡 Visão de Negócio


### Descrição funcional da História

Eu, como: PO <br />
Quero: Construir uma API que possibilite a criação de pedidos e Pagamentos <br />
Para: atender o site e demais aplicações que queiram criar pedidos e transacionar pagamentos <br />

## 🛠️ Visão técnica da solução

### Desenho de Arquitetura da Solução - Diagrama de Container (C2)

![MS Order Arquitetura (C4Model) (3)](https://user-images.githubusercontent.com/12093535/185700705-748553c2-4a57-4052-abf9-7c8bbf2b1a2a.jpg)
<h6 align="center">Clique na imagem para ampliar</h6>


## :hammer: Funcionalidades do projeto
#### 🛒 Micro Serviço de Pedidos 
- `Funcionalidade 1`: O novo micro serviço deve permitir a criação de novos Pedidos.
- `Funcionalidade 2`: O microservice deve possibilitar 3 tipos de consultas de pedido:
	- Recuperar por id.
	- Recuperar pelo número do pedido.
	- Recuperar os pedidos através do CPF do cliente.
- `Funcionalidade 3`: O Microservice deve ter um campo para armazenar o status do pedido, esse campo deve possuir apenas 3 status possíveis:
	- Pedido Criado
	- Pagamento Confirmado
	- Pagamento não Autorizado
- `Funcionalidade 3.1`:A Alteração de status do pedido só deve acontecer através de mensageria.
- `Funcionalidade 4`: O Microservice deve notificar sempre que houver uma criação de pedido.
- `Funcionalidade 5`: A soma de todos os itens deve ser igual ao valor total do pedido.

#### 💲 Micro Serviço de Pagamentos
- `Funcionalidade 1`: O microservice deve possibilitar 2 tipos de consultas:
	- Recuperar por id do pagamento.
	- Recuperar os pagamentos através do CPF do cliente.
- `Funcionalidade 2`: A criação de um pagamento deve acontecer apenas por mensageria.
- `Funcionalidade 3`: O Microservice deve ter um campo para armazenar o status do pagamento, esse campo deve possuir apenas 2 status possíveis:
	- Pagamento Confirmado.
	- Pagamento não Autorizado.
- `Funcionalidade 4`: O microservice deve propagar atualizações de status de pagamento apenas por mensageria.
- `Funcionalidade 4`: Pagamentos com valor maior igual que R$1.000 não devem ser autorizados.
- `Funcionalidade 5`: Pagamentos com valor menor que R$1.000 devem ser autorizados.

## 🎯 Desafio - O que será avaliado?
1. Espera-se que o aluno desenvolva uma breve explicação dos entregáveis e como abrir e executar o projeto através do README.md.
2. Será avaliado como você codificou a aplicação para produzir e consumir mensagens.
3. O contrato da sua aplicação deve ser bem documentada utilizando o framework Swagger.
4. Também iremos considerar a abordagem utilizada para testar o fluxo da sua aplicação (testes unitários e de integração).
5. Como você dividiu as camadas e responsabilidades da sua aplicação.
6. Boas praticas do HTTP status.
7. Uso de clean code será visto como diferencial.
8. Utilização do padrão para testes unitários na RD (https://github.com/halysonrp/training-shadow/tree/main/1.%20Testes%20Unit%C3%A1rios).
9. No final do projeto deve ser publicado um vídeo de no maximo 5 minutos explicando as principais funcionalidades do seu projeto. O link deve ser disponibilizado através do readme do projeto.

## ✔️ Observações adicionais
1. Use a sua imaginação na escolha dos objetos e atributos para cada api.
2. Como mensageria pode ser utilizado RabbitMQ ou Kafka.
3. O banco de dados fica a escolha do aluno, podendo ser utilizado, MySql, Oracle, Postgress, MongoDB ou até mesmo o H2.
4. O projeto deve ser disponibilizado como privado e o acesso deve ser compartilhado com o seu avaliador/mentor.

