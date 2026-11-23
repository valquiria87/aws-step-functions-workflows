# AWS CloudFormation e workflows

## O que é AWS CloudFormation?

AWS CloudFormation é um serviço de infraestrutura como código (*Infrastructure as Code — IaC*). Ele permite descrever recursos de infraestrutura em templates e utilizá-los para criar e gerenciar esses recursos de maneira estruturada.

Uma stack é o conjunto de recursos gerenciado pelo CloudFormation a partir de um template.

## Relação com AWS Step Functions

O Step Functions coordena a execução de processos. O CloudFormation, por sua vez, descreve e provisiona recursos de infraestrutura.

Em uma solução, os serviços podem atuar de forma complementar: a infraestrutura necessária é definida e gerenciada como código, enquanto o workflow coordena as tarefas do processo.

## O que foi acompanhado no laboratório

A integração entre AWS CloudFormation e AWS Step Functions foi acompanhada durante a aula. Também foram apresentadas validações relacionadas às definições do workflow e da infraestrutura, além de um projeto modelo. O objetivo desta seção é registrar a finalidade dos serviços e a relação entre eles.

**Não foi realizada uma criação ou implantação independente de stack para este projeto.**

## Por que infraestrutura como código é relevante?

- Permite documentar a infraestrutura desejada.
- Favorece repetibilidade na criação de ambientes.
- Facilita revisão e versionamento dos templates.
- Ajuda a manter a infraestrutura organizada junto à evolução da solução.

## Referências

- [AWS CloudFormation](https://aws.amazon.com/pt/cloudformation/)
- [Documentação do AWS CloudFormation](https://docs.aws.amazon.com/cloudformation/)
