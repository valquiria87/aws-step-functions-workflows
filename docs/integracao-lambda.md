# Integração entre AWS Step Functions e AWS Lambda

## Papel de cada serviço

**AWS Step Functions** coordena o workflow: define a sequência de etapas, controla as transições e acompanha a execução.

**AWS Lambda** executa código sob demanda. Uma função pode ser utilizada como uma tarefa dentro do workflow para realizar uma operação específica.

## Como a integração funciona

Em um cenário típico:

1. Uma execução da máquina de estados alcança um estado do tipo Task.
2. Esse estado invoca uma função Lambda configurada na definição do workflow.
3. A função recebe os dados de entrada definidos para a integração.
4. A função executa sua lógica e retorna uma resposta ou sinaliza uma falha.
5. O Step Functions utiliza o resultado para continuar o fluxo conforme a definição da máquina de estados.

## Exemplo conceitual

Considere um processo de validação de documentos técnicos:

- O Step Functions inicia o processo.
- Uma função Lambda verifica se os campos obrigatórios estão presentes.
- O resultado da função é utilizado por uma etapa de decisão.
- O workflow direciona o documento para processamento ou correção.

Esse exemplo ilustra uma possibilidade de arquitetura. Não representa uma função Lambda implementada neste repositório.

## O que foi acompanhado no laboratório

Durante a aula, foi demonstrada a criação e a execução de funções Lambda integradas ao AWS Step Functions. Esta documentação registra o conceito e a finalidade da integração, sem afirmar que uma solução própria foi implantada.

## Pontos importantes para uma implementação real

- Definir claramente a entrada e a saída da função.
- Conceder somente as permissões IAM necessárias.
- Considerar limites de tempo e erros de execução.
- Planejar como falhas serão tratadas pelo workflow.
- Evitar incluir credenciais ou dados sensíveis no código e nos repositórios.

## Referências

- [AWS Lambda](https://aws.amazon.com/pt/lambda/)
- [Documentação do AWS Lambda](https://docs.aws.amazon.com/lambda/)
- [Integração do Step Functions com Lambda](https://docs.aws.amazon.com/step-functions/latest/dg/connect-lambda.html)
