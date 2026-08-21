# Casos de Uso — Sistema Eventus

## 1. Objetivo

Este documento apresenta casos de uso selecionados para os fluxos do Sistema Eventus que possuem maior quantidade de regras de negócio, exceções ou decisões pendentes.

Foram selecionados os seguintes fluxos:

* inscrição em evento pago;
* cancelamento e reembolso;
* lista de espera.

A escolha foi intencionalmente seletiva para evitar redundância com as histórias de usuário e concentrar o detalhamento nos processos que mais se beneficiam de fluxos principais, alternativos e de exceção.

---

# UC01 — Realizar inscrição em evento pago

## Objetivo

Permitir que um participante solicite inscrição em um evento pago e tenha sua inscrição liberada conforme a confirmação do pagamento.

## Ator principal

Participante.

## Atores secundários

* Equipe Financeira;
* Sistema Eventus.

## Pré-condições

* O evento está disponível para inscrição;
* Existem vagas disponíveis;
* O evento foi definido como pago.

## Pós-condições

Ao final do processo, a inscrição poderá estar:

* aguardando confirmação de pagamento;
* liberada após confirmação do pagamento;
* não concluída.

## Fluxo principal

1. O participante consulta os eventos disponíveis.
2. O participante seleciona um evento pago.
3. O sistema verifica a disponibilidade de vagas.
4. O participante solicita a inscrição.
5. O sistema registra a solicitação.
6. O pagamento é realizado ou informado conforme o processo financeiro adotado.
7. A equipe financeira confirma o pagamento.
8. O sistema registra a confirmação financeira.
9. A inscrição é liberada conforme as regras do evento.
10. O sistema gera o comprovante da inscrição.

## Fluxos alternativos

### A1 — Evento sem vagas disponíveis

1. O participante solicita inscrição.
2. O sistema identifica que o limite de vagas foi atingido.
3. A inscrição não é confirmada.
4. O sistema informa que não existem vagas disponíveis.

A possibilidade de inclusão em lista de espera depende das regras ainda pendentes de validação.

---

### A2 — Pagamento ainda não confirmado

1. O participante solicita inscrição em evento que exige pagamento.
2. O pagamento ainda não foi confirmado.
3. O sistema mantém a inscrição em estado não liberado.
4. A inscrição só poderá ser liberada após a confirmação financeira.

---

### A3 — Falha ou ausência de pagamento

1. A confirmação de pagamento não ocorre.
2. O sistema não libera a inscrição.
3. O tratamento posterior depende das regras financeiras a serem definidas.

---

## Lacunas relacionadas

### LA06 — Momento da reserva de vaga

Ainda não está definido se a vaga:

* é reservada no início do pagamento;
* é reservada somente após confirmação;
* permanece reservada por determinado período.

Por esse motivo, o caso de uso não assume nenhuma dessas possibilidades como regra definitiva.

---

## Requisitos relacionados

RF02, RF03, RF09, RF13, RF14, RF15

## Regras relacionadas

RN01, RN02, RN04, RN05, RN12

## Histórias relacionadas

US02, US03, US09, US13, US14, US15

## Critérios de aceitação relacionados

CA02, CA03, CA04, CA11, CA14, CA15, CA16, CA17

---

# UC02 — Cancelar inscrição e tratar reembolso

## Objetivo

Permitir que um participante solicite o cancelamento de uma inscrição quando o evento permitir e tratar um possível reembolso conforme as regras aplicáveis.

## Ator principal

Participante.

## Atores secundários

* Equipe Financeira;
* Sistema Eventus.

## Pré-condições

* O participante possui uma inscrição registrada;
* O evento possui uma regra definida de cancelamento.

## Pós-condições

A inscrição poderá:

* permanecer ativa;
* ser cancelada sem reembolso;
* ser cancelada com possibilidade de reembolso.

## Fluxo principal

1. O participante acessa suas inscrições.
2. O participante seleciona uma inscrição.
3. O sistema verifica se o evento permite cancelamento.
4. O participante solicita o cancelamento.
5. O sistema valida as condições aplicáveis ao evento.
6. O sistema registra o cancelamento.
7. O sistema atualiza a disponibilidade de vagas quando aplicável.
8. O sistema verifica se existe direito a reembolso.
9. Caso exista, a situação é disponibilizada para tratamento pela equipe financeira.

## Fluxos alternativos

### A1 — Evento não permite cancelamento

1. O participante solicita o cancelamento.
2. O sistema identifica que o evento não permite essa operação.
3. O cancelamento é bloqueado.
4. O sistema informa o participante.

---

### A2 — Cancelamento permitido, mas sem direito a reembolso

1. O participante atende às condições para cancelar a inscrição.
2. O sistema registra o cancelamento.
3. As regras do evento não concedem direito a reembolso.
4. Nenhum reembolso é registrado.

---

### A3 — Cancelamento com direito a reembolso

1. O cancelamento é permitido.
2. As condições definidas para o evento dão direito ao reembolso.
3. O sistema registra a necessidade de tratamento financeiro.
4. A equipe financeira trata o reembolso conforme a política definida.

---

## Lacunas relacionadas

### LA01 — Prazo para cancelamento

Ainda não foi definido:

* até quando o cancelamento pode ocorrer;
* se o prazo varia de acordo com o evento;
* se existem exceções.

### LA02 — Critérios de reembolso

Ainda não foi definido:

* quando existe direito a reembolso;
* se o valor é integral ou parcial;
* se o prazo do cancelamento interfere no valor;
* quem aprova o reembolso.

---

## Requisitos relacionados

RF04, RF05, RF09, RF16

## Regras relacionadas

RN02, RN03, RN06

## Histórias relacionadas

US04, US05, US09, US16

## Critérios de aceitação relacionados

CA05, CA06, CA07, CA11, CA18

---

# UC03 — Gerenciar lista de espera

## Objetivo

Representar o fluxo de um participante que deseja participar de uma atividade lotada por meio de uma lista de espera.

## Ator principal

Participante.

## Ator secundário

Sistema Eventus.

## Pré-condições

* O evento ou atividade atingiu sua capacidade máxima;
* A funcionalidade de lista de espera está habilitada para o evento.

## Pós-condições

O participante poderá permanecer registrado como interessado em uma possível vaga.

## Fluxo principal proposto

1. O participante tenta se inscrever em uma atividade.
2. O sistema identifica que não existem vagas disponíveis.
3. O sistema informa que a atividade está lotada.
4. Quando a lista de espera estiver disponível, o sistema oferece ao participante a possibilidade de registrar interesse.
5. O participante confirma o interesse.
6. O sistema registra o participante na lista de espera.

## Observação importante

Esse fluxo representa apenas a parte que pode ser descrita sem assumir regras ainda não fornecidas.

Não foi definido como ocorre a movimentação posterior da lista.

---

## Fluxos dependentes de validação

### Liberação de vaga

Quando uma vaga ficar disponível, ainda é necessário definir se:

* o sistema promove automaticamente o primeiro participante;
* uma notificação é enviada;
* existe prazo para aceitar;
* a vaga fica reservada temporariamente;
* a pessoa perde a posição caso não responda.

---

### Ordem da lista

Não está definido se a ordem será baseada em:

* data e horário;
* prioridade;
* perfil do participante;
* algum outro critério.

---

## Lacuna relacionada

**LA03 — Funcionamento da lista de espera**

Esse caso de uso é considerado parcialmente especificado e não deve ser utilizado como base definitiva para implementação enquanto as regras não forem validadas.

---

## Requisitos relacionados

RF09, RF12

## Regra relacionada

RN07

## História relacionada

US12

## Critério de aceitação relacionado

Ainda não foi criado um critério definitivo para movimentação da lista de espera devido à ausência das regras necessárias.

---

## 2. Casos de uso não produzidos

Os demais fluxos foram mantidos apenas como histórias de usuário e critérios de aceitação, pois não apresentavam, neste momento, complexidade suficiente para justificar um caso de uso detalhado.

Por exemplo:

* visualizar eventos;
* consultar inscrições;
* consultar quantidade de inscritos;
* consultar programação do palestrante;
* consultar participantes de uma atividade.

A criação de casos de uso para todos esses cenários aumentaria a documentação sem acrescentar informação significativa à especificação.

---

## 3. Papel da Inteligência Artificial Generativa

A IA Generativa foi utilizada como apoio para:

* identificar quais fluxos possuíam maior quantidade de regras;
* estruturar pré-condições e pós-condições;
* levantar fluxos alternativos;
* identificar pontos em que a especificação dependia de lacunas.

Uma sugestão inicialmente apresentada pela IA foi criar casos de uso para praticamente todas as funcionalidades.

Essa abordagem foi descartada por gerar redundância com as histórias de usuário e aumentar desnecessariamente a documentação.

Também foram modificadas sugestões em que a IA completava automaticamente regras ausentes, especialmente relacionadas a:

* prazo de cancelamento;
* valor de reembolso;
* tempo de reserva da vaga;
* funcionamento automático da lista de espera.

Esses pontos foram mantidos como lacunas.

---

## 4. Considerações finais

Os casos de uso foram utilizados de forma seletiva para detalhar apenas os processos com maior complexidade de regras e exceções.

Essa escolha permitiu aprofundar os fluxos relevantes sem duplicar desnecessariamente o conteúdo já representado pelas histórias de usuário e critérios de aceitação.

O caso de uso da lista de espera foi mantido como parcialmente especificado porque ainda depende de decisões dos stakeholders.
