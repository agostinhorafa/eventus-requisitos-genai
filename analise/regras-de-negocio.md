# Regras de Negócio — Sistema Eventus

## 1. Objetivo

Este documento apresenta as regras de negócio identificadas a partir do documento de elicitação do Sistema de Gestão de Eventos da empresa Eventus.

As regras foram extraídas das falas e necessidades dos stakeholders.

Quando uma regra depende de informação ainda não definida, ela é registrada como parcial ou acompanhada da respectiva lacuna.

---

## 2. Regras de Negócio Identificadas

### RN01 — Eventos possuem quantidade limitada de vagas

Cada evento ou atividade deverá possuir uma capacidade de participantes.

O número de inscrições confirmadas não poderá ultrapassar a quantidade de vagas disponível.

**Origem:** Organizador

---

### RN02 — O controle de vagas deve ser automático

A quantidade de vagas disponíveis deverá ser atualizada conforme as inscrições forem registradas ou canceladas.

**Origem:** Organizador

**Observação:**
O documento menciona acompanhamento da quantidade de inscritos “em tempo real”, porém não define um intervalo mensurável para essa atualização.

---

### RN03 — Nem todos os eventos permitem cancelamento

A possibilidade de cancelamento dependerá das regras definidas para cada evento.

O participante só poderá cancelar uma inscrição quando o evento permitir essa operação.

**Origem:** Organizador

**Lacuna relacionada:**
Não foi definido até quando o cancelamento poderá ser realizado.

---

### RN04 — Eventos podem ser gratuitos ou pagos

Cada evento deverá ser classificado de acordo com sua condição financeira.

Um evento poderá ser:

* gratuito; ou
* pago.

**Origem:** Equipe Financeira

---

### RN05 — Algumas inscrições dependem de confirmação de pagamento

Quando a inscrição estiver sujeita à confirmação de pagamento, ela somente poderá ser liberada após essa confirmação.

**Origem:** Equipe Financeira

**Lacuna relacionada:**
Ainda não está definido se a vaga é reservada no início do pagamento ou somente depois que o pagamento for confirmado.

---

### RN06 — O direito ao reembolso depende das condições do evento

Nem todo cancelamento implica direito a reembolso.

O sistema deverá considerar as regras aplicáveis ao evento antes de registrar ou autorizar um reembolso.

**Origem:** Equipe Financeira

**Lacuna relacionada:**
Não foram definidas as situações em que o participante terá direito ao reembolso.

---

### RN07 — Lista de espera pode ser utilizada em eventos lotados

Quando um evento atingir sua capacidade máxima, poderá existir uma lista de espera.

**Origem:** Organizador

**Situação:** Regra candidata / parcialmente definida.

**Lacunas relacionadas:**

* não foi definido como o participante entra na lista;
* não foi definida a ordem da lista;
* não foi informado como uma vaga liberada será oferecida;
* não foi definido quanto tempo um participante terá para aceitar uma vaga.

---

### RN08 — Workshops no mesmo horário ocorrem simultaneamente

Workshops programados para o mesmo horário deverão ocorrer simultaneamente.

**Origem:** Organizador

**Lacuna relacionada:**
Não foi definido o comportamento esperado quando um participante tentar se inscrever em dois workshops com conflito de horário.

---

### RN09 — Certificados só podem ser emitidos após o evento

A emissão do certificado ocorrerá depois da realização do evento.

**Origem:** Participante

**Lacuna relacionada:**
Ainda não foi definido se a emissão depende exclusivamente do término do evento ou também da confirmação de presença.

---

### RN10 — Palestrantes consultam participantes apenas de suas atividades

O palestrante poderá consultar os participantes inscritos nas atividades às quais estiver associado.

**Origem:** Palestrante

**Lacuna relacionada:**
Ainda não foram definidos quais dados dos participantes poderão ser visualizados.

---

### RN11 — Organizadores devem acompanhar as inscrições dos eventos

Os organizadores deverão possuir acesso às informações de inscrição necessárias para controlar vagas e participantes.

**Origem:** Organizador

---

### RN12 — A equipe financeira é responsável pela confirmação de pagamentos

A confirmação de pagamentos associados às inscrições deverá ser realizada ou controlada pela equipe financeira.

**Origem:** Equipe Financeira

---

## 3. Regras de negócio ainda não definidas

Algumas regras são necessárias para completar o comportamento do sistema, mas o documento de elicitação não fornece informações suficientes.

### Prazo para cancelamento

Não está definido:

* até quando o participante poderá cancelar;
* se o prazo varia por evento;
* se existem situações excepcionais.

**Status:** Pendente de validação.

---

### Política de reembolso

Não está definido:

* quais eventos permitem reembolso;
* se o valor será integral ou parcial;
* qual relação existe entre prazo de cancelamento e reembolso;
* como o reembolso será processado.

**Status:** Pendente de validação.

---

### Funcionamento da lista de espera

Não estão definidas as regras de:

* entrada;
* ordenação;
* promoção de participantes;
* expiração da oportunidade de ocupar uma vaga.

**Status:** Pendente de validação.

---

### Reserva de vaga durante pagamento

Não está definido se:

* a vaga é reservada ao iniciar o pagamento;
* a vaga só é ocupada após confirmação;
* existe tempo limite para pagamento.

**Status:** Pendente de validação.

---

### Conflitos de horário

O documento informa que workshops no mesmo horário ocorrem simultaneamente, mas não define se o sistema deverá:

* bloquear a inscrição;
* apenas alertar o participante;
* permitir a inscrição mesmo com conflito.

**Status:** Pendente de validação.

---

### Emissão de certificados

Não foi definido se o participante precisa:

* apenas estar inscrito;
* ter pagamento confirmado;
* ter presença confirmada;
* atingir algum percentual mínimo de participação.

**Status:** Pendente de validação.

---

## 4. Relação entre requisitos e regras de negócio

As regras de negócio complementam os requisitos funcionais.

Exemplo:

* o **RF05** define que o participante pode cancelar uma inscrição;
* a **RN03** estabelece que essa possibilidade depende das regras do evento.

Outro exemplo:

* o **RF14** permite confirmar pagamentos;
* a **RN05** estabelece que determinadas inscrições somente são liberadas após essa confirmação.

Essa separação ajuda a evitar que condições de negócio sejam confundidas com funcionalidades do sistema.

---

## 5. Papel da Inteligência Artificial Generativa

A IA Generativa foi utilizada como apoio para separar comportamentos funcionais de regras de negócio.

Durante a análise, algumas sugestões da IA precisaram ser modificadas porque preenchiam automaticamente informações não fornecidas pelos stakeholders.

Foram rejeitadas, por exemplo, definições arbitrárias como:

* cancelamento permitido até 24 ou 48 horas antes do evento;
* reembolso integral em determinado prazo;
* reserva de vaga por um número fixo de minutos;
* ordem específica da lista de espera.

Essas informações foram mantidas como lacunas, porque o documento de elicitação não fornece base para defini-las.

---

## 6. Considerações finais

As regras de negócio identificadas permitem representar as principais condições que regulam inscrições, vagas, cancelamentos, pagamentos, reembolsos, certificados e acesso às informações dos participantes.

Entretanto, parte dessas regras ainda depende de esclarecimento junto aos stakeholders.

A principal preocupação durante a análise foi não transformar inferências ou sugestões plausíveis da IA em regras definitivas sem respaldo no material de elicitação.
