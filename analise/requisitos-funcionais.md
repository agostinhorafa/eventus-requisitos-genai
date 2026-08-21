# Requisitos Funcionais — Sistema Eventus

## 1. Objetivo

Este documento apresenta os requisitos funcionais identificados a partir do documento de elicitação fornecido para o Sistema de Gestão de Eventos da empresa Eventus.

Os requisitos foram derivados das necessidades expressas pelos stakeholders e foram mantidos dentro dos limites das informações disponíveis no cenário.

Pontos ainda não definidos foram registrados separadamente como lacunas ou ambiguidades, evitando assumir regras que não foram confirmadas pelos stakeholders.

---

## 2. Requisitos Funcionais

### RF01 — Consultar eventos disponíveis

O sistema deve permitir que o participante visualize os eventos disponíveis em um único local.

**Origem:** Participante

---

### RF02 — Realizar inscrição em evento ou atividade

O sistema deve permitir que o participante realize inscrição em eventos e atividades disponíveis.

**Origem:** Participante

---

### RF03 — Emitir comprovante de inscrição

O sistema deve permitir a geração de um comprovante associado à inscrição do participante.

A forma de envio ou disponibilização do comprovante ainda precisa ser definida.

**Origem:** Participante

**Lacuna relacionada:** forma de envio do comprovante.

---

### RF04 — Consultar inscrições realizadas

O sistema deve permitir que o participante acompanhe as inscrições realizadas.

**Origem:** definição do interesse do stakeholder Participante.

---

### RF05 — Cancelar inscrição

O sistema deve permitir o cancelamento da inscrição quando o evento permitir essa operação.

O prazo e demais condições de cancelamento ainda precisam ser definidos.

**Origem:** Participante e Organizador.

**Lacuna relacionada:** prazo limite para cancelamento.

---

### RF06 — Emitir certificado

O sistema deve permitir que o participante emita seu certificado após o evento, quando atender às condições necessárias para emissão.

A regra que determina essas condições ainda precisa ser validada.

**Origem:** Participante.

**Lacuna relacionada:** confirmação de presença e demais critérios para emissão.

---

### RF07 — Permitir múltiplas inscrições em workshops

O sistema deve permitir que o participante se inscreva em mais de um workshop.

O tratamento de workshops com horários conflitantes ainda precisa ser definido.

**Origem:** Participante.

**Lacuna relacionada:** conflito de horários.

---

### RF08 — Criar eventos

O sistema deve permitir que organizadores criem eventos.

**Origem:** interesse do stakeholder Organizador.

---

### RF09 — Controlar vagas dos eventos

O sistema deve controlar automaticamente a quantidade de vagas disponíveis em eventos ou atividades.

**Origem:** Organizador.

---

### RF10 — Consultar quantidade de inscritos

O sistema deve permitir que os organizadores acompanhem a quantidade de participantes inscritos nos eventos.

**Origem:** Organizador.

---

### RF11 — Gerenciar participantes

O sistema deve permitir que os organizadores consultem e gerenciem os participantes associados aos eventos.

**Origem:** interesse do stakeholder Organizador.

---

### RF12 — Manter lista de espera

O sistema deve permitir a existência de uma lista de espera quando um evento ou atividade atingir sua capacidade máxima, caso essa funcionalidade seja adotada.

As regras de entrada, ordenação e chamada da lista ainda precisam ser definidas.

**Origem:** Organizador.

**Lacuna relacionada:** funcionamento da lista de espera.

---

### RF13 — Registrar eventos gratuitos ou pagos

O sistema deve permitir que um evento seja identificado como gratuito ou sujeito a pagamento.

**Origem:** Equipe Financeira.

---

### RF14 — Registrar e confirmar pagamentos

O sistema deve permitir que a equipe financeira confirme pagamentos associados às inscrições.

**Origem:** Equipe Financeira.

---

### RF15 — Condicionar inscrição à confirmação de pagamento

O sistema deve permitir que determinadas inscrições somente sejam liberadas após a confirmação do pagamento, quando essa regra for aplicável ao evento.

**Origem:** Equipe Financeira.

**Lacuna relacionada:** momento em que a vaga é reservada durante o processo de pagamento.

---

### RF16 — Registrar reembolso

O sistema deve permitir o tratamento de reembolso quando o participante tiver direito a ele.

As situações que geram direito ao reembolso ainda precisam ser definidas.

**Origem:** Equipe Financeira.

**Lacuna relacionada:** critérios para concessão de reembolso.

---

### RF17 — Consultar programação das atividades

O sistema deve permitir que palestrantes consultem a programação das atividades das quais participam.

**Origem:** interesse do stakeholder Palestrante.

---

### RF18 — Consultar participantes de uma atividade

O sistema deve permitir que palestrantes consultem a lista de participantes inscritos em suas atividades.

As informações dos participantes que poderão ser visualizadas ainda precisam ser definidas.

**Origem:** Palestrante.

**Lacuna relacionada:** dados dos participantes acessíveis aos palestrantes.

---

## 3. Requisitos não formalizados por falta de informação

Algumas funcionalidades foram mencionadas ou inferidas como possíveis necessidades, mas não possuem informações suficientes para serem transformadas em requisitos completos.

### Notificações

O documento menciona comprovantes e outras notificações aos participantes, porém não define:

* quais eventos geram notificações;
* quais canais devem ser utilizados;
* se o participante poderá escolher o canal;
* quais mensagens deverão ser enviadas.

Por esse motivo, requisitos específicos de notificação deverão ser definidos somente após esclarecimento com os stakeholders.

---

### Controle de presença

A emissão de certificados pode depender da confirmação de presença, porém o cenário não informa como a presença será registrada ou validada.

Esse ponto permanece pendente.

---

### Lista de espera

A existência da lista de espera foi sugerida, mas ainda não foram definidas suas regras.

Não foram assumidas regras sobre:

* posição na fila;
* ordem de prioridade;
* prazo para aceitar uma vaga;
* movimentação automática da lista.

---

## 4. Considerações sobre a análise

Durante a transformação das informações de elicitação em requisitos funcionais, foram evitadas decisões que não estavam presentes no documento original.

Expressões como “seria interessante” foram tratadas como necessidades ou funcionalidades candidatas e, quando dependiam de regras ainda indefinidas, foram mantidas acompanhadas das respectivas lacunas.

Essa abordagem busca preservar a rastreabilidade entre as falas dos stakeholders e os requisitos resultantes, sem transformar hipóteses em decisões definitivas.
