# Histórias de Usuário — Sistema Eventus

## 1. Objetivo

Este documento apresenta as histórias de usuário selecionadas para representar as principais necessidades dos stakeholders do Sistema Eventus.

As histórias foram estruturadas no formato:

`Como [ator], quero [ação], para [benefício].`

A elaboração considerou apenas informações presentes no documento de elicitação e nas análises realizadas. Quando uma funcionalidade depende de uma regra ainda não definida, a respectiva lacuna é indicada.

---

## 2. Histórias de Usuário

### US01 — Visualizar eventos disponíveis

**Como** participante,
**quero** visualizar os eventos disponíveis em um único local,
**para** escolher aqueles dos quais desejo participar.

**Requisito relacionado:** RF01

---

### US02 — Realizar inscrição

**Como** participante,
**quero** me inscrever em um evento ou atividade disponível,
**para** garantir minha participação.

**Requisitos relacionados:** RF02, RF09

---

### US03 — Receber comprovante de inscrição

**Como** participante,
**quero** obter um comprovante após realizar uma inscrição,
**para** ter confirmação do registro da minha participação.

**Requisito relacionado:** RF03

**Lacuna relacionada:** LA05 — forma de envio ou disponibilização do comprovante.

---

### US04 — Consultar minhas inscrições

**Como** participante,
**quero** visualizar minhas inscrições,
**para** acompanhar os eventos e atividades em que estou inscrito.

**Requisito relacionado:** RF04

---

### US05 — Cancelar inscrição

**Como** participante,
**quero** cancelar uma inscrição quando o evento permitir,
**para** desistir da participação sem precisar entrar em contato diretamente com a organização.

**Requisito relacionado:** RF05

**Regra relacionada:** RN03

**Lacuna relacionada:** LA01 — prazo e condições de cancelamento.

---

### US06 — Emitir certificado

**Como** participante,
**quero** emitir meu certificado após o evento,
**para** comprovar minha participação.

**Requisito relacionado:** RF06

**Regra relacionada:** RN09

**Lacuna relacionada:** LA04 — critérios para emissão do certificado.

---

### US07 — Inscrever-se em múltiplos workshops

**Como** participante,
**quero** me inscrever em diferentes workshops no mesmo dia,
**para** participar das atividades de meu interesse.

**Requisito relacionado:** RF07

**Regra relacionada:** RN08

**Lacuna relacionada:** LA07 — tratamento de conflitos de horário.

---

### US08 — Criar evento

**Como** organizador,
**quero** criar eventos no sistema,
**para** centralizar o gerenciamento das atividades oferecidas pela Eventus.

**Requisito relacionado:** RF08

---

### US09 — Controlar vagas automaticamente

**Como** organizador,
**quero** que o sistema controle automaticamente a quantidade de vagas,
**para** evitar inscrições acima da capacidade do evento.

**Requisito relacionado:** RF09

**Regras relacionadas:** RN01, RN02

---

### US10 — Acompanhar quantidade de inscritos

**Como** organizador,
**quero** acompanhar a quantidade de participantes inscritos,
**para** monitorar a ocupação dos eventos.

**Requisito relacionado:** RF10

**Ambiguidade relacionada:** AM01 — significado de “em tempo real”.

---

### US11 — Gerenciar participantes

**Como** organizador,
**quero** consultar e gerenciar os participantes de um evento,
**para** apoiar o controle das inscrições e da realização do evento.

**Requisito relacionado:** RF11

**Ambiguidade relacionada:** AM04 — significado de “gerenciar participantes”.

---

### US12 — Entrar em lista de espera

**Como** participante,
**quero** ter a possibilidade de entrar em uma lista de espera quando uma atividade estiver lotada,
**para** poder ocupar uma vaga caso haja disponibilidade posteriormente.

**Requisito relacionado:** RF12

**Regra relacionada:** RN07

**Lacuna relacionada:** LA03 — funcionamento da lista de espera.

**Status:** História candidata, dependente de validação da regra.

---

### US13 — Definir evento como gratuito ou pago

**Como** responsável pelo gerenciamento do evento,
**quero** identificar se um evento é gratuito ou pago,
**para** que o sistema aplique corretamente as regras financeiras associadas.

**Requisito relacionado:** RF13

**Regra relacionada:** RN04

---

### US14 — Confirmar pagamento

**Como** membro da equipe financeira,
**quero** confirmar o pagamento de uma inscrição,
**para** permitir a liberação das inscrições que dependem de pagamento.

**Requisito relacionado:** RF14

**Regras relacionadas:** RN05, RN12

---

### US15 — Liberar inscrição após pagamento

**Como** participante,
**quero** ter minha inscrição liberada após a confirmação do pagamento quando essa condição for exigida,
**para** concluir minha participação no evento.

**Requisito relacionado:** RF15

**Regra relacionada:** RN05

**Lacuna relacionada:** LA06 — momento da reserva da vaga.

---

### US16 — Tratar reembolso

**Como** membro da equipe financeira,
**quero** registrar e controlar um reembolso quando o participante tiver direito,
**para** tratar corretamente os valores associados a cancelamentos.

**Requisito relacionado:** RF16

**Regra relacionada:** RN06

**Lacuna relacionada:** LA02 — critérios de reembolso.

---

### US17 — Consultar programação

**Como** palestrante,
**quero** consultar a programação das atividades às quais estou associado,
**para** acompanhar meus compromissos no evento.

**Requisito relacionado:** RF17

---

### US18 — Consultar participantes da atividade

**Como** palestrante,
**quero** visualizar os participantes inscritos em minhas atividades,
**para** ter acesso às informações necessárias para sua realização.

**Requisito relacionado:** RF18

**Regra relacionada:** RN10

**Lacuna relacionada:** LA08 — quais dados dos participantes podem ser visualizados.

---

## 3. Histórias não formalizadas como definitivas

Algumas possíveis histórias foram identificadas, mas não foram assumidas como parte definitiva do escopo.

### Notificações automáticas

O documento menciona comprovantes e “demais notificações”, porém não define quais notificações existem ou quais canais serão utilizados.

Por esse motivo, não foi criada uma história definitiva de envio de notificações.

**Lacuna relacionada:** LA05

---

### Controle de presença

O certificado pode depender da confirmação de presença, mas o documento não informa como a presença deve ser registrada.

Por isso, não foi criada uma história definitiva para essa funcionalidade.

**Lacuna relacionada:** LA04

---

### Processamento automático da lista de espera

A IA pode sugerir que o sistema mova automaticamente o próximo participante da lista quando surgir uma vaga.

Essa funcionalidade não foi formalizada porque as regras da lista de espera ainda não foram definidas.

**Lacuna relacionada:** LA03

---

## 4. Uso da Inteligência Artificial Generativa

A IA Generativa foi utilizada para apoiar a transformação das necessidades expressas pelos stakeholders em histórias de usuário.

As sugestões foram revisadas para:

* preservar a perspectiva do stakeholder;
* evitar funcionalidades não presentes na elicitação;
* indicar explicitamente histórias dependentes de lacunas;
* evitar que regras ainda não definidas fossem incorporadas como fatos.

Foram descartadas ou mantidas como candidatas histórias que dependiam de decisões não tomadas, como envio automático de notificações, regras específicas de lista de espera e controle de presença.

---

## 5. Considerações finais

As histórias de usuário representam as principais necessidades funcionais do Sistema Eventus sob a perspectiva dos diferentes stakeholders.

A utilização de referências aos requisitos, regras e lacunas ajuda a manter a rastreabilidade e deixa explícitos os pontos que ainda necessitam de esclarecimento antes da implementação.
