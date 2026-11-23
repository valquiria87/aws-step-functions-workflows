# Conceitos fundamentais do AWS Step Functions

## Orquestração de serviços

Orquestração é a coordenação de diferentes tarefas e serviços para executar um processo com começo, etapas intermediárias e conclusão. Em vez de cada componente precisar controlar manualmente o próximo, um orquestrador central administra o fluxo definido.

O AWS Step Functions permite modelar essa coordenação por meio de workflows visuais.

## Workflow

Um workflow representa o processo automatizado. Ele descreve quais etapas devem ocorrer e como a execução avança entre elas.

## State Machine

A máquina de estados (*State Machine*) é a definição do workflow. Ela especifica os estados disponíveis, as transições e a lógica que determina o caminho da execução.

## Estados

Cada estado representa uma etapa do workflow. Dependendo do tipo, pode executar uma tarefa, tomar uma decisão, aguardar ou encerrar o processo.

Alguns tipos de estado encontrados na documentação do Step Functions:

| Tipo | Finalidade geral |
|---|---|
| Task | Executar uma tarefa ou integração. |
| Choice | Direcionar a execução com base em condições. |
| Wait | Pausar a execução por um período ou até um instante definido. |
| Parallel | Executar ramos de trabalho em paralelo. |
| Pass | Passar dados ou introduzir dados estáticos no fluxo. |
| Succeed | Encerrar a execução com sucesso. |
| Fail | Encerrar a execução indicando falha. |

## Execução

Uma execução (*Execution*) é uma instância de um workflow em andamento ou já concluída. O acompanhamento das execuções ajuda a identificar o estado das etapas e o resultado do processo.

## Planejamento antes do provisionamento

É possível começar pelo desenho da lógica do workflow e configurar suas integrações à medida que os recursos necessários são definidos. Isso separa o planejamento do processo da preparação completa da infraestrutura, embora a execução real dependa dos recursos e permissões exigidos pelas integrações escolhidas.

## Benefícios observados

- Clareza visual da sequência de atividades.
- Separação de responsabilidades entre etapas.
- Integração de serviços.
- Acompanhamento das execuções.
- Facilidade para evoluir o processo conforme novos requisitos.

## Referências

- [AWS Step Functions](https://aws.amazon.com/pt/step-functions/)
- [Conceitos do AWS Step Functions](https://docs.aws.amazon.com/step-functions/latest/dg/concepts.html)
