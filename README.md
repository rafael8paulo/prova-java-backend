# Prova Técnica – Desenvolvedor Java Backend Pleno
## Instruções

- Tempo estimado: 4 horas
 - Tecnologias permitidas: Java 17+, Spring Boot, JPA/Hibernate, Redis, RabbitMQ/Kafka, Docker
- Enviar o código em um repositório público do GitHub ou em um arquivo ZIP
- Documentação da API pode ser feita via Swagger ou um arquivo README.md
## Parte 1 – Programação Orientada a Objetos (POO)
### Cenário
Você deve implementar um sistema de gerenciamento de pedidos para um e-commerce.

### Requisitos

1. Criar um modelo de domínio com as seguintes entidades e seus relacionamentos:
- Cliente (id, nome, email)
- Produto (id, nome, preço, estoque)
- Pedido (id, cliente, lista de produtos, status, data do pedido)
2. Aplicar princípios SOLID na modelagem das classes.
3. Implementar um repositório JPA para cada entidade.
4. Criar um serviço para criação de pedidos, validando:
- Se o cliente existe.
- Se os produtos estão disponíveis no estoque.
- Atualizar o estoque após a compra.

## Parte 2 – Redis
### Cenário
O e-commerce precisa armazenar as informações de estoque em cache para reduzir a carga no banco de dados.

### Requisitos
1. Configurar o Redis no projeto.
2. Criar uma funcionalidade para armazenar o estoque dos produtos no Redis com tempo de expiração.
3. Implementar uma busca otimizada que:
- Primeiro verifica se os dados estão no cache do Redis.
- Se não encontrar, consulta no banco de dados e atualiza o cache.

## Parte 3 – Mensageria
### Cenário
Quando um pedido é criado, o sistema deve notificar o setor de faturamento e atualização de estoque.

### Requisitos

1. Configurar um broker de mensageria (RabbitMQ ou Kafka).
2. Criar um publisher que envie mensagens com os detalhes do pedido para um tópico/fila.
3. Implementar um consumer que escute essa mensagem e registre no log a confirmação do processamento.

## Critérios de Avaliação

✅ Código limpo e bem estruturado

✅ Boas práticas de POO e SOLID

✅ Uso correto do Redis para caching

✅ Implementação funcional de mensageria

✅ Testes unitários e/ou de integração

✅ Documentação mínima (README.md ou Swagger)