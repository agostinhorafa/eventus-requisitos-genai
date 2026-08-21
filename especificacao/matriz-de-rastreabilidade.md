# Matriz de Rastreabilidade — Sistema Eventus

## 1. Objetivo

Este documento apresenta a matriz de rastreabilidade dos requisitos do Sistema Eventus.

A matriz relaciona os diferentes artefatos produzidos durante a análise e a especificação, permitindo identificar a origem e o detalhamento de cada requisito ao longo da documentação.

A relação utilizada foi:

`Requisito Funcional → Regra de Negócio → Lacuna/Ambiguidade → História de Usuário → Caso de Uso → Critério de Aceitação`

Nem todos os requisitos possuem necessariamente todos os tipos de artefato associados. Os casos de uso, por exemplo, foram produzidos apenas para os fluxos considerados mais complexos.

---

## 2. Matriz Principal de Rastreabilidade

| Requisito | Descrição resumida                               | Regra(s) relacionada(s) | Lacuna / Ambiguidade | História(s)      | Caso de Uso      | Critério(s) de Aceitação     |
| --------- | ------------------------------------------------ | ----------------------- | -------------------- | ---------------- | ---------------- | ---------------------------- |
| RF01      | Consultar eventos disponíveis                    | —                       | —                    | US01             | —                | CA01                         |
| RF02      | Realizar inscrição                               | RN01                    | —                    | US02             | UC01             | CA02, CA03                   |
| RF03      | Emitir comprovante de inscrição                  | —                       | LA05 / AM02          | US03             | UC01             | CA04                         |
| RF04      | Consultar inscrições realizadas                  | —                       | —                    | US04             | UC02             | CA05                         |
| RF05      | Cancelar inscrição                               | RN03                    | LA01                 | US05             | UC02             | CA06, CA07                   |
| RF06      | Emitir certificado                               | RN09                    | LA04                 | US06             | —                | CA08                         |
| RF07      | Permitir múltiplas inscrições em workshops       | RN08                    | LA07 / IC01          | US07             | —                | CA09                         |
| RF08      | Criar eventos                                    | —                       | —                    | US08             | —                | CA10                         |
| RF09      | Controlar vagas                                  | RN01, RN02              | LA03, LA06           | US02, US09, US12 | UC01, UC02, UC03 | CA02, CA03, CA11             |
| RF10      | Consultar quantidade de inscritos                | RN02                    | AM01                 | US10             | —                | CA12                         |
| RF11      | Gerenciar participantes                          | RN11                    | AM04                 | US11             | —                | CA13                         |
| RF12      | Manter lista de espera                           | RN07                    | LA03                 | US12             | UC03             | Critério definitivo pendente |
| RF13      | Registrar evento como gratuito ou pago           | RN04                    | —                    | US13             | UC01             | CA14                         |
| RF14      | Confirmar pagamentos                             | RN12                    | —                    | US14             | UC01             | CA15                         |
| RF15      | Condicionar inscrição à confirmação de pagamento | RN05                    | LA06 / IC03          | US15             | UC01             | CA16, CA17                   |
| RF16      | Registrar reembolso                              | RN06                    | LA02 / IC02 / AM05   | US16             | UC02             | CA18                         |
| RF17      | Consultar programação                            | —                       | —                    | US17             | —                | CA19                         |
| RF18      | Consultar participantes de atividade             | RN10                    | LA08                 | US18             | —                | CA20                         |

---

## 3. Rastreabilidade das Regras de Negócio

| Regra | Descrição resumida                                      | Requisito(s) relacionado(s) | História(s) relacionada(s) |
| ----- | ------------------------------------------------------- | --------------------------- | -------------------------- |
| RN01  | Eventos possuem quantidade limitada de vagas            | RF02, RF09                  | US02, US09                 |
| RN02  | Controle de vagas deve ser automático                   | RF09, RF10                  | US09, US10                 |
| RN03  | Nem todos os eventos permitem cancelamento              | RF05                        | US05                       |
| RN04  | Eventos podem ser gratuitos ou pagos                    | RF13                        | US13                       |
| RN05  | Algumas inscrições dependem de pagamento confirmado     | RF14, RF15                  | US14, US15                 |
| RN06  | Direito a reembolso depende das condições do evento     | RF16                        | US16                       |
| RN07  | Lista de espera pode existir em eventos lotados         | RF12                        | US12                       |
| RN08  | Workshops no mesmo horário ocorrem simultaneamente      | RF07                        | US07                       |
| RN09  | Certificados são emitidos após o evento                 | RF06                        | US06                       |
| RN10  | Palestrantes consultam participantes de suas atividades | RF18                        | US18                       |
| RN11  | Organizadores acompanham participantes e inscrições     | RF10, RF11                  | US10, US11                 |
| RN12  | Equipe financeira confirma pagamentos                   | RF14                        | US14                       |

---

## 4. Rastreabilidade das Lacunas

| Lacuna | Descrição resumida                            | Artefatos afetados                 |
| ------ | --------------------------------------------- | ---------------------------------- |
| LA01   | Prazo para cancelamento                       | RF05, RN03, US05, UC02, CA06       |
| LA02   | Critérios para reembolso                      | RF16, RN06, US16, UC02, CA18       |
| LA03   | Funcionamento da lista de espera              | RF09, RF12, RN07, US12, UC03       |
| LA04   | Critérios para emissão de certificado         | RF06, RN09, US06, CA08             |
| LA05   | Forma de envio de comprovantes e notificações | RF03, US03, CA04                   |
| LA06   | Momento da reserva de vaga em evento pago     | RF09, RF15, RN05, US15, UC01, CA16 |
| LA07   | Tratamento de conflito de horários            | RF07, RN08, US07, CA09             |
| LA08   | Dados visíveis aos palestrantes               | RF18, RN10, US18, CA20             |
| LA09   | Requisitos de segurança                       | RNFs propostos                     |
| LA10   | Requisitos de privacidade                     | RNFs propostos                     |
| LA11   | Requisitos de desempenho                      | RNFs propostos                     |
| LA12   | Requisitos de disponibilidade                 | RNFs propostos                     |
| LA13   | Requisitos de acessibilidade                  | RNFs propostos                     |

---

## 5. Rastreabilidade das Ambiguidades e Inconsistências

| ID   | Descrição                                                       | Artefatos afetados           |
| ---- | --------------------------------------------------------------- | ---------------------------- |
| AM01 | Significado de “em tempo real”                                  | RF10, US10, CA12, RNF04      |
| AM02 | Significado de “logo após a inscrição”                          | RF03, US03, CA04             |
| AM03 | Significado de “determinadas inscrições”                        | RF15, RN05                   |
| AM04 | Significado de “gerenciar participantes”                        | RF11, US11, CA13             |
| AM05 | Significado de “controlar reembolsos”                           | RF16, US16, UC02             |
| IC01 | Múltiplos workshops versus conflito de horário                  | RF07, US07, LA07             |
| IC02 | Cancelamento não implica necessariamente reembolso              | RF05, RF16, RN03, RN06, UC02 |
| IC03 | Diferença entre inscrição iniciada e confirmação após pagamento | RF14, RF15, UC01             |

---

## 6. Exemplos de rastreabilidade ponta a ponta

### Exemplo 1 — Cancelamento e reembolso

`RF05/RF16 → RN03/RN06 → LA01/LA02 → US05/US16 → UC02 → CA06/CA07/CA18`

Nesse fluxo:

* RF05 representa a possibilidade de cancelamento;
* RF16 representa o tratamento de reembolso;
* RN03 estabelece que nem todos os eventos permitem cancelamento;
* RN06 estabelece que reembolso depende das condições do evento;
* LA01 registra a ausência do prazo de cancelamento;
* LA02 registra a ausência da política de reembolso;
* US05 e US16 representam as necessidades dos participantes e da equipe financeira;
* UC02 detalha o fluxo principal e suas exceções;
* CA06, CA07 e CA18 representam comportamentos verificáveis sem definir arbitrariamente as regras ainda ausentes.

---

### Exemplo 2 — Inscrição em evento pago

`RF02/RF14/RF15 → RN01/RN05/RN12 → LA06 → US02/US14/US15 → UC01 → CA02/CA15/CA16/CA17`

Esse fluxo permite acompanhar desde a necessidade de inscrição até a confirmação financeira.

A LA06 permanece explícita porque ainda não foi definido em qual momento a vaga deve ser reservada.

---

### Exemplo 3 — Lista de espera

`RF12 → RN07 → LA03 → US12 → UC03`

Nesse caso, a rastreabilidade também evidencia uma limitação da especificação.

O fluxo básico da lista de espera foi identificado, mas os critérios de aceitação definitivos não foram criados porque as regras de funcionamento ainda dependem de validação dos stakeholders.

---

### Exemplo 4 — Acesso dos palestrantes

`RF18 → RN10 → LA08 → US18 → CA20`

A necessidade de consultar participantes está confirmada, mas a quantidade e o tipo de dados acessíveis ainda permanecem pendentes.

---

## 7. Benefícios da matriz

A matriz de rastreabilidade permite:

* identificar a origem dos requisitos;
* localizar regras de negócio relacionadas;
* identificar pontos ainda pendentes de validação;
* acompanhar a transformação de requisitos em histórias de usuário;
* verificar quais fluxos possuem casos de uso detalhados;
* relacionar requisitos aos critérios de aceitação;
* apoiar análise de impacto em caso de mudança;
* reduzir inconsistências entre os diferentes documentos.

---

## 8. Papel da Inteligência Artificial Generativa

A IA Generativa foi utilizada como apoio para organizar as relações entre os artefatos produzidos.

A ferramenta ajudou a identificar possíveis associações entre requisitos, regras, histórias, casos de uso e critérios de aceitação.

Entretanto, as relações foram revisadas manualmente.

Algumas associações inicialmente sugeridas pela IA foram simplificadas ou removidas quando não existia uma ligação clara no documento de elicitação.

Também foi evitado criar artefatos apenas para completar artificialmente a matriz.

Por exemplo, não foi criado um caso de uso para cada requisito e não foram inventados critérios de aceitação para a lista de espera enquanto suas regras permanecem indefinidas.

---

## 9. Considerações finais

A matriz de rastreabilidade demonstra como as informações obtidas na elicitação foram refinadas e transformadas em diferentes artefatos de análise e especificação.

Ela também deixa explícito quais elementos ainda dependem de validação dos stakeholders.

Dessa forma, a rastreabilidade não serve apenas para relacionar documentos, mas também para evidenciar onde a especificação ainda está incompleta.
