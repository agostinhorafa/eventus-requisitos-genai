# Critérios de Aceitação — Sistema Eventus

## 1. Objetivo

Este documento apresenta os critérios de aceitação associados às principais histórias de usuário do Sistema Eventus.

Os critérios foram escritos no formato Gherkin:

`Dado / Quando / Então`

O objetivo é transformar as necessidades levantadas em comportamentos mais claros e verificáveis, sem preencher automaticamente lacunas que ainda dependem de validação dos stakeholders.

---

## 2. Critérios de Aceitação

### CA01 — Visualizar eventos disponíveis

**História relacionada:** US01
**Requisito relacionado:** RF01

```gherkin
Dado que existem eventos disponíveis para inscrição
Quando o participante acessar a área de eventos
Então o sistema deve apresentar os eventos disponíveis em um único local
```

---

### CA02 — Realizar inscrição em evento com vaga disponível

**História relacionada:** US02
**Requisitos relacionados:** RF02, RF09

```gherkin
Dado que o participante selecionou um evento disponível
E existem vagas disponíveis
Quando solicitar a inscrição
Então o sistema deve registrar a solicitação de inscrição
E atualizar a quantidade de vagas conforme as regras do evento
```

---

### CA03 — Impedir inscrição acima da capacidade

**Histórias relacionadas:** US02, US09
**Requisito relacionado:** RF09
**Regra relacionada:** RN01

```gherkin
Dado que um evento atingiu sua capacidade máxima
Quando um participante tentar realizar uma nova inscrição
Então o sistema não deve confirmar uma inscrição acima do limite de vagas
```

**Observação:**
O comportamento relacionado à lista de espera depende da LA03 e, por isso, não foi incluído como resultado obrigatório neste critério.

---

### CA04 — Gerar comprovante de inscrição

**História relacionada:** US03
**Requisito relacionado:** RF03
**Lacuna relacionada:** LA05

```gherkin
Dado que uma inscrição foi registrada com sucesso
Quando o processo de inscrição for concluído
Então o sistema deve gerar um comprovante associado à inscrição
```

**Pendente de definição:**
A forma de entrega do comprovante ainda deve ser validada com os stakeholders.

---

### CA05 — Consultar inscrições realizadas

**História relacionada:** US04
**Requisito relacionado:** RF04

```gherkin
Dado que o participante possui inscrições registradas
Quando acessar suas inscrições
Então o sistema deve apresentar as inscrições associadas ao participante
```

---

### CA06 — Cancelar inscrição em evento que permite cancelamento

**História relacionada:** US05
**Requisito relacionado:** RF05
**Regra relacionada:** RN03
**Lacuna relacionada:** LA01

```gherkin
Dado que o participante possui uma inscrição
E o evento permite cancelamento
Quando solicitar o cancelamento
Então o sistema deve permitir o cancelamento conforme as regras definidas para o evento
```

**Pendente de definição:**
O prazo limite e demais condições para cancelamento ainda não foram definidos.

---

### CA07 — Impedir cancelamento quando o evento não permite

**História relacionada:** US05
**Regra relacionada:** RN03

```gherkin
Dado que o participante possui uma inscrição
E o evento não permite cancelamento
Quando o participante tentar cancelar a inscrição
Então o sistema deve impedir a operação
E informar que o evento não permite cancelamento
```

---

### CA08 — Emitir certificado após o evento

**História relacionada:** US06
**Requisito relacionado:** RF06
**Regra relacionada:** RN09
**Lacuna relacionada:** LA04

```gherkin
Dado que o evento já foi realizado
E o participante atende aos critérios definidos para emissão do certificado
Quando solicitar o certificado
Então o sistema deve disponibilizar o certificado ao participante
```

**Pendente de definição:**
Os critérios que determinam o direito ao certificado ainda precisam ser validados.

---

### CA09 — Permitir múltiplas inscrições em workshops

**História relacionada:** US07
**Requisito relacionado:** RF07
**Lacuna relacionada:** LA07

```gherkin
Dado que existem diferentes workshops disponíveis no mesmo dia
Quando o participante solicitar inscrição em mais de um workshop
Então o sistema deve permitir múltiplas inscrições
Desde que não exista uma regra validada que impeça a combinação selecionada
```

**Pendente de definição:**
O tratamento de conflitos de horário ainda deve ser definido pelos stakeholders.

---

### CA10 — Criar evento

**História relacionada:** US08
**Requisito relacionado:** RF08

```gherkin
Dado que o organizador possui permissão para gerenciar eventos
Quando cadastrar as informações necessárias de um novo evento
Então o sistema deve registrar o evento
E disponibilizá-lo conforme seu estado e regras de publicação
```

**Observação:**
O documento de elicitação não detalha campos obrigatórios nem fluxo de publicação.

---

### CA11 — Controlar vagas automaticamente

**História relacionada:** US09
**Requisito relacionado:** RF09
**Regras relacionadas:** RN01, RN02

```gherkin
Dado que um evento possui quantidade limitada de vagas
Quando uma inscrição válida alterar a ocupação do evento
Então o sistema deve atualizar a quantidade de vagas disponíveis
E não permitir que o total de inscrições confirmadas ultrapasse a capacidade
```

---

### CA12 — Consultar quantidade de inscritos

**História relacionada:** US10
**Requisito relacionado:** RF10
**Ambiguidade relacionada:** AM01

```gherkin
Dado que existem inscrições registradas para um evento
Quando o organizador consultar a ocupação
Então o sistema deve apresentar a quantidade atual de inscritos
```

**Pendente de definição:**
O significado mensurável de “tempo real” ainda precisa ser estabelecido.

---

### CA13 — Consultar participantes de um evento

**História relacionada:** US11
**Requisito relacionado:** RF11

```gherkin
Dado que existem participantes associados a um evento
Quando o organizador consultar os participantes
Então o sistema deve apresentar a relação de participantes do evento
```

**Observação:**
Operações adicionais de “gerenciamento” dependem do esclarecimento da AM04.

---

### CA14 — Registrar evento como gratuito ou pago

**História relacionada:** US13
**Requisito relacionado:** RF13
**Regra relacionada:** RN04

```gherkin
Dado que um evento está sendo configurado
Quando sua condição financeira for definida
Então o sistema deve permitir classificá-lo como gratuito ou pago
```

---

### CA15 — Confirmar pagamento

**História relacionada:** US14
**Requisito relacionado:** RF14
**Regra relacionada:** RN12

```gherkin
Dado que existe uma inscrição associada a um evento pago
Quando a equipe financeira confirmar o pagamento
Então o sistema deve registrar a confirmação
E atualizar a situação financeira da inscrição
```

---

### CA16 — Liberar inscrição condicionada a pagamento

**História relacionada:** US15
**Requisito relacionado:** RF15
**Regra relacionada:** RN05
**Lacuna relacionada:** LA06

```gherkin
Dado que uma inscrição exige confirmação de pagamento
Quando o pagamento for confirmado
Então o sistema deve permitir a liberação da inscrição conforme as regras do evento
```

**Pendente de definição:**
O momento em que a vaga é efetivamente reservada ainda não foi definido.

---

### CA17 — Não liberar inscrição sem pagamento quando exigido

**História relacionada:** US15
**Regra relacionada:** RN05

```gherkin
Dado que uma inscrição depende de confirmação de pagamento
E o pagamento ainda não foi confirmado
Quando o sistema avaliar a situação da inscrição
Então a inscrição não deve ser tratada como liberada
```

---

### CA18 — Registrar reembolso quando aplicável

**História relacionada:** US16
**Requisito relacionado:** RF16
**Regra relacionada:** RN06
**Lacuna relacionada:** LA02

```gherkin
Dado que um participante cancelou uma inscrição
E atende às regras de reembolso definidas para o evento
Quando a equipe financeira tratar o reembolso
Então o sistema deve permitir registrar o reembolso
```

**Pendente de definição:**
Os critérios que dão direito a reembolso ainda precisam ser validados.

---

### CA19 — Consultar programação do palestrante

**História relacionada:** US17
**Requisito relacionado:** RF17

```gherkin
Dado que o palestrante está associado a uma ou mais atividades
Quando consultar sua programação
Então o sistema deve apresentar as atividades associadas a ele
```

---

### CA20 — Consultar participantes de atividade

**História relacionada:** US18
**Requisito relacionado:** RF18
**Regra relacionada:** RN10
**Lacuna relacionada:** LA08

```gherkin
Dado que o palestrante está associado a uma atividade
E existem participantes inscritos nessa atividade
Quando consultar a lista de participantes
Então o sistema deve apresentar os participantes da atividade
E limitar os dados exibidos aos campos autorizados para o perfil de palestrante
```

**Pendente de definição:**
Ainda não foram definidos quais campos poderão ser visualizados.

---

## 3. Critérios não formalizados por falta de informação

Alguns cenários não foram transformados em critérios de aceitação definitivos porque dependem de decisões ainda não tomadas.

### Lista de espera

Não foram definidos:

* ordem da lista;
* forma de entrada;
* promoção para uma vaga;
* prazo para aceitar uma vaga.

**Lacuna:** LA03

---

### Conflito de horários

Ainda não foi definido se uma inscrição conflitante deve:

* ser bloqueada;
* gerar apenas alerta;
* ser permitida.

**Lacuna:** LA07

---

### Notificações

Não estão definidos:

* canais;
* eventos que geram mensagens;
* prazos;
* preferências dos usuários.

**Lacuna:** LA05

---

### Presença

Não foi definido como a presença será registrada ou como se relaciona com a emissão de certificados.

**Lacuna:** LA04

---

## 4. Critérios de qualidade adotados

Durante a elaboração, buscou-se evitar critérios que utilizassem termos vagos ou não verificáveis.

Por exemplo, não foram transformadas em critérios definitivos expressões como:

* “em tempo real”;
* “logo após”;
* “rapidamente”;
* “de forma segura”.

Esses termos precisam ser refinados antes que possam ser utilizados como base objetiva para testes.

---

## 5. Papel da Inteligência Artificial Generativa

A IA Generativa foi utilizada para apoiar a transformação das histórias de usuário em cenários Dado–Quando–Então.

Foram aproveitadas principalmente sugestões relacionadas a:

* fluxos principais;
* situações de bloqueio;
* estados financeiros;
* relação entre vagas e inscrições;
* diferenciação entre regra confirmada e decisão pendente.

Algumas sugestões foram modificadas quando a IA acrescentou regras não presentes na elicitação.

Foram descartadas definições como:

* cancelamento até determinado número de horas;
* reembolso integral em prazo fixo;
* reserva de vaga por tempo predeterminado;
* posição automática na lista de espera;
* percentual mínimo de presença para certificado.

Essas informações continuam como lacunas até validação dos stakeholders.

---

## 6. Considerações finais

Os critérios de aceitação tornam as histórias de usuário mais objetivas e aproximam a especificação das futuras atividades de validação e testes.

Nos pontos em que a elicitação ainda não fornece informação suficiente, o critério não foi completado com uma suposição.

A decisão adotada foi preservar a lacuna de forma explícita para posterior esclarecimento com os stakeholders.
