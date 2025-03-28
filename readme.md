🚀 Microserviço de Processamento de Pedidos - Desafio Backend BTG Pactual
O objetivo deste projeto é construir um microserviço que processa pedidos a partir de uma fila RabbitMQ e disponibiliza uma API REST para consultar:

💵 Valor total de um pedido

📊 Quantidade de pedidos por cliente

📝 Lista de pedidos realizados por cliente

🛠 Tecnologias Utilizadas
Java 21 ☕

Spring Boot ⚡

Spring Data MongoDB 🗃️

RabbitMQ 📦

Docker 🐋

JUnit (para testes unitários) 🧪

Mockito (para mocks em testes) 🎭

🛠 Funcionalidades
Consumo de Pedidos: O serviço consome mensagens de uma fila RabbitMQ, processa e salva as informações de pedidos no banco de dados MongoDB.

API REST: A API disponibiliza os seguintes endpoints:

🛒 GET /orders/{customerId}: Lista de pedidos realizados por um cliente.

💰 GET /orders/{customerId}/total: Valor total dos pedidos realizados por um cliente.

🔢 GET /orders/{customerId}/count: Quantidade de pedidos realizados por um cliente.

Testes Unitários: Implementação de testes unitários com JUnit e Mockito para garantir a qualidade do código e a confiabilidade do sistema.

📦 Como Rodar o Projeto
1. Configuração do Ambiente
Certifique-se de ter o Docker instalado para rodar o MongoDB e RabbitMQ em contêineres.

2. Docker Compose
Use o arquivo docker-compose.yml para configurar o RabbitMQ e o MongoDB. Rode o comando abaixo para levantar os containers:

bash
Copiar
Editar
docker-compose up -d
3. Rodando o Projeto
Clone o repositório:

bash
Copiar
Editar
git clone https://github.com/seu-usuario/microservico-pedidos.git
cd microservico-pedidos
Compile e execute o projeto:

bash
Copiar
Editar
./mvnw spring-boot:run
O projeto estará rodando em http://localhost:8080.

🧪 Testando a API
Utilize ferramentas como Postman ou curl para testar os endpoints disponíveis na API.

Endpoints disponíveis:
🛒 GET /orders/{customerId}: Retorna a lista de pedidos realizados por um cliente.

💰 GET /orders/{customerId}/total: Retorna o valor total dos pedidos realizados por um cliente.

🔢 GET /orders/{customerId}/count: Retorna a quantidade de pedidos realizados por um cliente.

4. Testes Unitários
Os testes unitários estão implementados com JUnit e Mockito. Para rodá-los, basta usar o seguinte comando:

bash
Copiar
Editar
./mvnw test
🗂️ Estrutura do Projeto
OrderController: Controlador responsável por expor os endpoints da API REST.

OrderService: Lógica de negócios relacionada ao processamento de pedidos.

OrderRepository: Interface para interação com o banco de dados MongoDB.

OrderCreatedListener: Listener para consumir mensagens da fila RabbitMQ e processar pedidos.

Order: Entidade que representa um pedido.

OrderItem: Entidade que representa um item dentro de um pedido.

Docker: Arquivos de configuração para rodar o RabbitMQ e MongoDB em containers.

📑 Arquivos Importantes
docker-compose.yml: Configuração do Docker para MongoDB e RabbitMQ.

application.properties: Configurações do Spring Boot, como a URL do banco MongoDB e RabbitMQ.

OrderController.java: Controlador que implementa os endpoints da API.

OrderService.java: Serviço que contém a lógica de negócios para pedidos.

OrderRepository.java: Repositório de MongoDB.

OrderCreatedListener.java: Listener para consumir mensagens do RabbitMQ.

🤝 Contribuindo
Faça um fork do repositório.

Crie uma branch para a sua feature: git checkout -b minha-feature.

Faça suas alterações e commite-as: git commit -m 'Adiciona minha feature'.

Envie para o seu repositório forkado: git push origin minha-feature.

Crie um Pull Request para o repositório original.

📝 Licença
Este projeto está licenciado sob a licença MIT. Consulte o arquivo LICENSE para mais detalhes.
