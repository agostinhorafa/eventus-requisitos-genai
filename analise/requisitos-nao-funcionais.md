# Requisitos Não Funcionais — Sistema Eventus

## 1. Objetivo

Este documento registra os requisitos não funcionais identificados ou propostos para validação a partir do documento de elicitação do Sistema Eventus.

O material fornecido informa explicitamente que não foram levantados requisitos relacionados a:

* segurança;
* desempenho;
* disponibilidade;
* acessibilidade;
* privacidade dos dados.

Por esse motivo, esses itens não foram assumidos como requisitos definitivos.

As necessidades abaixo são tratadas como **propostas a validar com os stakeholders**, evitando transformar sugestões da Inteligência Artificial Generativa em decisões de negócio já aprovadas.

---

## 2. Requisitos Não Funcionais Propostos para Validação

### RNF01 — Proteção de dados pessoais

**Categoria:** Privacidade / Segurança

**Proposta:**
O sistema deverá proteger os dados pessoais dos participantes e limitar sua visualização de acordo com o perfil do usuário.

**Justificativa:**
Palestrantes precisam consultar participantes inscritos em suas atividades, mas o documento não define quais informações poderão ser visualizadas.

**Status:** Proposta a validar.

**Questões pendentes:**

* Quais dados pessoais serão armazenados?
* Quais dados poderão ser visualizados pelos organizadores?
* Quais dados poderão ser visualizados pelos palestrantes?
* Existem informações restritas exclusivamente à equipe administrativa?

---

### RNF02 — Controle de acesso

**Categoria:** Segurança

**Proposta:**
O sistema deverá controlar o acesso às funcionalidades de acordo com os diferentes perfis de usuário.

Os perfis inicialmente identificados são:

* participante;
* organizador;
* equipe financeira;
* palestrante;
* equipe de TI.

**Status:** Proposta a validar.

**Questões pendentes:**

* Como será realizada a autenticação?
* Um usuário poderá possuir mais de um perfil?
* Quais permissões específicas cada perfil deverá possuir?

---

### RNF03 — Proteção das informações financeiras

**Categoria:** Segurança

**Proposta:**
Informações relacionadas a pagamentos e reembolsos deverão ser acessíveis apenas aos perfis autorizados.

**Status:** Proposta a validar.

**Justificativa:**
A equipe financeira é responsável pela confirmação de pagamentos e pelo controle de reembolsos.

**Questões pendentes:**

* Quais dados financeiros serão armazenados pelo sistema?
* O sistema realizará o pagamento ou apenas registrará sua confirmação?
* Haverá integração com um serviço externo de pagamento?

---

### RNF04 — Tempo de atualização das vagas

**Categoria:** Desempenho

**Proposta:**
As informações sobre quantidade de inscritos e vagas disponíveis deverão ser atualizadas em prazo suficientemente curto para evitar inconsistências durante as inscrições.

**Status:** Proposta a validar.

**Observação:**
O documento utiliza a expressão “em tempo real”, porém não informa um limite mensurável.

Por isso, nenhum valor de segundos foi definido.

**Questão pendente:**
Qual é o tempo máximo aceitável para atualização da quantidade de inscritos e vagas disponíveis?

---

### RNF05 — Tempo de resposta do sistema

**Categoria:** Desempenho

**Proposta:**
As principais operações do sistema deverão apresentar tempo de resposta adequado para uso pelos participantes e organizadores.

**Status:** Proposta a validar.

**Observação:**
Não foi definido nenhum valor objetivo no documento de elicitação.

**Questões pendentes:**

* Qual deve ser o tempo máximo de resposta para consulta de eventos?
* Qual deve ser o tempo máximo para confirmação de uma inscrição?
* Existem operações com requisitos de desempenho mais rígidos?

---

### RNF06 — Disponibilidade do sistema

**Categoria:** Disponibilidade

**Proposta:**
O sistema deverá possuir disponibilidade compatível com os períodos de inscrição e realização dos eventos.

**Status:** Proposta a validar.

**Questões pendentes:**

* Qual percentual de disponibilidade é esperado?
* Existem períodos críticos em que o sistema não poderá ficar indisponível?
* Como deverão ser tratadas indisponibilidades durante períodos de inscrição?

---

### RNF07 — Acessibilidade

**Categoria:** Acessibilidade

**Proposta:**
As interfaces destinadas aos participantes deverão considerar requisitos de acessibilidade para permitir seu uso por pessoas com diferentes necessidades.

**Status:** Proposta a validar.

**Questões pendentes:**

* Existe padrão de acessibilidade exigido pela organização?
* Há necessidade de conformidade com WCAG?
* Quais níveis de conformidade deverão ser adotados?

---

### RNF08 — Compatibilidade de dispositivos

**Categoria:** Usabilidade / Compatibilidade

**Proposta:**
O sistema deverá permitir acesso por dispositivos utilizados pelos principais perfis de usuário.

**Status:** Proposta a validar.

**Questões pendentes:**

* O sistema será exclusivamente web?
* Deverá funcionar em smartphones e tablets?
* Existe necessidade de aplicativo móvel nativo?
* Quais navegadores deverão ser suportados?

---

### RNF09 — Rastreabilidade de operações críticas

**Categoria:** Auditoria / Segurança

**Proposta:**
O sistema deverá registrar operações relevantes relacionadas a:

* inscrições;
* cancelamentos;
* pagamentos;
* reembolsos;
* emissão de certificados.

**Status:** Proposta a validar.

**Justificativa:**
Essas operações podem afetar vagas, valores financeiros e direitos dos participantes.

**Questões pendentes:**

* Quais dados deverão ser mantidos no histórico?
* Por quanto tempo os registros serão armazenados?
* Quais usuários poderão consultar esse histórico?

---

### RNF10 — Privacidade na consulta de participantes

**Categoria:** Privacidade

**Proposta:**
Palestrantes deverão visualizar apenas os dados de participantes necessários para execução de suas atividades.

**Status:** Proposta a validar.

**Lacuna relacionada:**
O documento de elicitação não define quais informações dos participantes podem ser consultadas pelos palestrantes.

---

## 3. Requisitos não definidos numericamente

Durante o apoio da IA Generativa, poderiam ser sugeridos valores como:

* disponibilidade de 99,9%;
* resposta em até 2 segundos;
* atualização das vagas em até 1 segundo;
* retenção de logs por 5 anos;
* suporte obrigatório aos navegadores mais recentes.

Esses valores não possuem respaldo no documento de elicitação e, portanto, não foram incorporados como requisitos.

Quando necessário, deverão ser definidos posteriormente junto aos stakeholders.

---

## 4. Classificação das propostas

| ID    | Categoria                     | Situação           |
| ----- | ----------------------------- | ------------------ |
| RNF01 | Privacidade / Segurança       | Proposta a validar |
| RNF02 | Segurança                     | Proposta a validar |
| RNF03 | Segurança                     | Proposta a validar |
| RNF04 | Desempenho                    | Proposta a validar |
| RNF05 | Desempenho                    | Proposta a validar |
| RNF06 | Disponibilidade               | Proposta a validar |
| RNF07 | Acessibilidade                | Proposta a validar |
| RNF08 | Compatibilidade / Usabilidade | Proposta a validar |
| RNF09 | Auditoria / Segurança         | Proposta a validar |
| RNF10 | Privacidade                   | Proposta a validar |

---

## 5. Papel da Inteligência Artificial Generativa

A IA Generativa foi utilizada para apoiar a identificação de categorias de requisitos não funcionais que poderiam ser relevantes para o sistema.

A principal revisão humana realizada foi impedir que essas sugestões fossem apresentadas como requisitos já confirmados.

Como o documento de elicitação não contém critérios objetivos nessas categorias, as sugestões foram registradas como propostas e perguntas para validação.

Também foram descartados valores quantitativos sugeridos sem fonte, pois um requisito não funcional deve ser verificável e respaldado por uma necessidade real dos stakeholders.

---

## 6. Considerações finais

A ausência de requisitos não funcionais no documento de elicitação representa uma lacuna importante.

Segurança, privacidade, desempenho, disponibilidade e acessibilidade podem afetar significativamente a solução, mas seus critérios não devem ser definidos arbitrariamente pelo analista ou pela IA.

O próximo passo recomendado é validar essas propostas com os stakeholders e, somente após essa validação, transformá-las em requisitos não funcionais definitivos e mensuráveis.
