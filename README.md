# Refinando E-Commerce


# Índice 

* [Refinando E-Commerce](#refinando-e-commerce)
* [Índice](#índice)
* [Descrição do Projeto](#descrição-do-projeto)
* [Status do Projeto](#status-do-projeto)
* [Modificações Realizadas](#modificações-realizadas)
* [Novas Funcionalidades](#novas-funcionalidades)
* [Modelo Entidade Relacional](#modelo-entidade-relacional)
* [Técnicas e tecnologias utilizadas](#técnicas-e-tecnologias-utilizadas)
* [Acesse o Projeto](#acesse-o-projeto)
* [Conclusão](#conclusão)

## Descrição do Projeto

Este projeto de refinamento de banco de dados para um cenário de e-commerce tem como objetivo principal proporcionar uma estrutura eficiente para o gerenciamento de informações relacionadas a clientes, produtos, pedidos, pagamentos, estoque, fornecedores e vendedores. A proposta busca otimizar o armazenamento e a consulta de dados em um ambiente de vendas online, reduzindo redundâncias e garantindo maior flexibilidade para futuras expansões.

O banco de dados visa resolver problemas comuns enfrentados por empresas de e-commerce, como o gerenciamento de clientes de diferentes perfis (pessoas físicas e jurídicas), controle de estoque em múltiplos locais de armazenamento, acompanhamento de entregas com códigos de rastreamento e registro de diferentes formas de pagamento. Além disso, ao unificar informações em tabelas relacionadas, o modelo busca melhorar a precisão dos dados e simplificar as operações de consulta e manutenção.

Este desafio de projeto consiste no refinamento de um projeto lógico de banco de dados para um cenário de e-commerce. O projeto original teve por objetivo gerenciar clientes, produtos, pedidos, pagamentos, estoque, fornecedores e vendedores. Durante a modelagem, foram implementadas chaves primárias e estrangeiras no cenário modelado.

## Status do Projeto

![Status do Projeto](http://img.shields.io/static/v1?label=STATUS&message=Concluído&color=GREEN&style=for-the-badge)


## Modificações realizadas

No escopo da revisão, foram criadas duas tabelas para o cadastro dos clientes:

- **T_Clients_Individuals**: destinada a clientes pessoas físicas, que receberá, dentre várias informações, o CPF da pessoa.
- **T_Clients_Corporate**: destinada ao cadastro dos clientes pessoas jurídicas ou empresas, que receberá, dentre várias informações, o CNPJ da empresa.

Além dessas duas novas tabelas, a tabela **T_Payments** foi modificada para que possa registrar as diversas formas de pagamento disponíveis para um usuário.

As tabelas **T_Clients_Corporate**, **T_Clients_Individuals**, **T_Seller** e **T_Supplier** foram modificadas e receberam uma coluna denominada `Prefix`. A coluna `Prefix` armazena um prefixo para cada uma das tabelas, que é concatenado ao ID de cada registro para criar um código único. Por exemplo:

- Para a tabela **T_Clients_Individuals**, o prefixo pode ser `IND`. Se um cliente tem o ID `001`, o código único será `IND001`.
- Para a tabela **T_Clients_Corporate**, o prefixo pode ser `CORP`. Se uma empresa tem o ID `002`, o código único será `CORP002`.

A inclusão do `Prefix` e a criação de um código único para cada tabela possibilitou a utilização da tabela **T_Address** para armazenar os endereços de cada cliente, fornecedor ou vendedor, reduzindo redundâncias de informações e, consequentemente, otimizando o banco de dados.

## Novas Funcionalidades

No novo modelo E-Commerce, foi adicionada a tabela **T_Shipping**, que receberá um código de rastreio para monitorar a entrega dos produtos adquiridos. A tabela **T_Shipping** foi planejada para registrar informações detalhadas sobre o processo de entrega, como data de envio, data estimada de entrega, status de envio e o código de rastreio, que será uma combinação de letras e números, como por exemplo, `ET123456BR`. Esse código será utilizado no sistema para acompanhar o status da entrega em tempo real, permitindo aos clientes e à equipe de suporte consultar o progresso de suas encomendas.

## Modelo Entidade Relacional

O Modelo Entidade Relacional (MER) apresentado a seguir ilustra a estrutura do banco de dados projetado para o cenário de e-commerce. Esse modelo destaca as principais entidades envolvidas, como clientes, produtos, pedidos, pagamentos, entregas e endereços, além dos relacionamentos entre elas. Ele serve como uma representação visual das tabelas e das conexões lógicas estabelecidas, facilitando o entendimento da arquitetura do sistema proposto.

![Modelo Entidade Relacional - E-Commerce](https://github.com/FredericoSander/Refinando_E-Commerce/blob/main/Imagens/E-Commerce.png)

## Técnicas e tecnologias utilizadas

- ``SQL``
- ``MySQL Workbench 8.0``
- ``Modelagem de dados``
- ``Git``
- ``GitHub``

## Conclusão

O projeto de refinamento do banco de dados para o cenário de e-commerce representa um avanço no gerenciamento de informações cruciais para o ambiente de vendas online. As melhorias implementadas, como a criação de tabelas específicas para diferentes tipos de clientes e a inclusão de códigos únicos, oferecem maior precisão e flexibilidade na gestão dos dados.

Com as próximas etapas focadas na construção de scripts SQL, persistência de dados e criação de consultas simuladas, o projeto estará preparado para atender às necessidades de um ambiente de produção.

Esse refinamento otimiza o desempenho do banco de dados e melhora a experiência do usuário final, garantindo que as informações sejam acessadas de forma rápida e segura.

## Acesse o Projeto

Você pode acessar o projeto clicando [aqui](https://github.com/FredericoSander/Refinando_E-Commerce/tree/main/Arquivos%20SQL)

## Autor

| [<img loading="lazy" src="https://avatars.githubusercontent.com/u/136928502?s=96&v=4" width=115><br><sub>Frederico Sander</sub>](https://github.com/FredericoSander)
| :---: | 