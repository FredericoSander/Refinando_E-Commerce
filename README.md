# Refinando_E-Commerce


## Descrição do projeto

<p align="justify">Este desafio de projeto consiste no refinamento de um projeto lógico de banco de dados para um cenário de e-commerce. O projeto original teve por objetivo gerenciar clientes, produtos, pedidos, pagamentos, estoque, fornecedores e vendedores. Durante a modelagem, foram implementadas chaves primárias e estrangeiras no cenário modelado.
No escopo da revisão, foram criadas duas tabelas para o cadastro dos clientes, a tabela **T_Clients_individuals** destinada a clientes pessoas físicas, que receberá dentre varias informações o CPF da pessoa; e a tabela **T_client_Corporate** é destinada ao cadastro dos clientes pessoas jurídicas ou empresas, e receberá dentre varias informações, o CNPJ da empresa. Além dessas duas novas tabelas, a tabela T_Payments foi modificada para que possa registrar as diversas forma de pagamento disponiíeis para um usuário.

As tabelas **T_Clients_Corporate, T_Clients_Individuals, T_Seller e T_Supplier**, foram modificadas e receberam uma coluna denominada <Strong>Prefix</Strong>. A coluna <b>Prefix</b> armazena um prefixo para cada uma das tabelas, que é concatenado ao ID de cada registro para criar um código único. A inclusão do Prefixo e a criação de um código único para cada tabela possibilitou a utilização da tabela T_Adress para armazenar os endereços de cada cliente, fornecedor ou vendedor reduzindo redundâncias de informações e consequentemente otimizando o banco de dados.

No novo modelo E-commerce ainda foi adicionada a tabela **T_Entrega** que recebrá um código de rastreio para monitorar a entrega dos produtos adquiridos. Novas funcionalidades podem ser incorporadas de forma a modernizar e otimizar a aplicação.

Para a proxima atualização, está prevista a criação dos scripts de construção do bando de dados, presistência de dados para realização de testes de validação, e a criaão de consultas para simular o uso de um banco de dados em ambiente de produção.

Outras revisões podem incluir a criação de views e automações para criação de consultas otimizadas.</p>


## Modelo Entidade Relacional
- Imagem Modelo Entidade Relacional e-commerce
<div aling="center">
 <img src="https://github.com/FredericoSander/Refinando_E-Commerce/blob/main/Imagens/E-Commerce.png">
</div>

## Autor

- [Frederico S N Cota](https://github.com/FredericoSander)