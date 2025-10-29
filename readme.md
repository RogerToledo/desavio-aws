# Sistema de Análise de Dados AWS

## Arquitetura do Sistema

![Architecture Diagram](https://github.com/RogerToledo/desavio-aws/blob/main/image/architecture.png)

Este projeto implementa uma solução completa de análise de dados utilizando serviços AWS, com integração para visualização em PowerBI.

## Componentes da Arquitetura

### AWS Cloud Infrastructure

#### Armazenamento
- **Amazon S3**: Armazenamento arquivos com dados pronto para exibição no PowerBI
- **Amazon EBS**: Armazenamento em bloco para instâncias EC2 que roda um Mongo DB

#### Processamento
- **Amazon EC2 - Aplicação**: Instância dedicada para processamento da aplicação principal
- **Amazon EC2 - MongoDB**: Instância dedicada para banco de dados MongoDB

#### ETL (Extract, Transform, Load)
- **ETL Service**: Responsável pela extração, transformação e carregamento dos dados

### Integração Externa
- **PowerBI**: Ferramenta de Business Intelligence para visualização e análise dos dados
- **Cliente**: Interface de acesso ao sistema

## Fluxo de Dados

1. **Ingestão**: Os dados são processados pela aplicação (EC2)
2. **Armazenamento**: Dados são armazenados no MongoDB (EC2)
3. **Processamento**: O serviço ETL processa e transforma os dados e envia para o S3
4. **Visualização**: PowerBI consome os dados para criação de dashboards e relatórios
5. **Acesso**: Clientes acessam as informações através da interface

## Tecnologias Utilizadas

- **AWS EC2**: Computação em nuvem
- **AWS S3**: Armazenamento de objetos
- **AWS EBS**: Armazenamento em bloco
- **MongoDB**: Banco de dados NoSQL
- **ETL**: Processamento de dados
- **PowerBI**: Business Intelligence
- **AWS Cloud**: Infraestrutura em nuvem
