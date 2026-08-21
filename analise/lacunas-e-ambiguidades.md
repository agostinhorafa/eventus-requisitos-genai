# Lacunas e Ambiguidades — Sistema Eventus

## 1. Objetivo

Este documento registra lacunas, ambiguidades, inconsistências e informações que ainda precisam ser esclarecidas junto aos stakeholders do Sistema Eventus.

O objetivo é evitar que informações incompletas sejam transformadas em requisitos ou regras de negócio definitivas sem validação.

---

## 2. Lacunas identificadas

### LA01 — Prazo para cancelamento de inscrição

**Descrição:**
O documento informa que nem todos os eventos permitem cancelamento, mas não define até quando essa operação pode ser realizada.

**Impacto:**
Sem essa definição, não é possível estabelecer uma regra de negócio objetiva nem critérios de aceitação.

**Perguntas para esclarecimento:**

* Até quando o participante poderá cancelar uma inscrição?
* O prazo será igual para todos os eventos?
* O organizador poderá configurar esse prazo?
* Existem exceções?

**Prioridade:** Alta

**Status:** Pendente de validação

---

### LA02 — Critérios para reembolso

**Descrição:**
Foi informado que em alguns casos há direito a reembolso e em outros não, porém os critérios não foram definidos.

**Impacto:**
Pode gerar conflitos financeiros e interpretações diferentes entre participantes e equipe financeira.

**Perguntas para esclarecimento:**

* Quais situações geram direito a reembolso?
* O reembolso será integral ou parcial?
* O prazo de cancelamento influencia o direito ao reembolso?
* Eventos gratuitos e pagos seguem regras diferentes?
* Quem autoriza o reembolso?

**Prioridade:** Crítica

**Status:** Pendente de validação

---

### LA03 — Funcionamento da lista de espera

**Descrição:**
A criação de uma lista de espera foi sugerida para eventos lotados, mas não foram definidas suas regras.

**Impacto:**
Sem regras claras, não é possível especificar o comportamento da funcionalidade.

**Perguntas para esclarecimento:**

* O participante entra automaticamente na lista?
* A ordem será por data e hora de entrada?
* O participante será avisado quando surgir uma vaga?
* Haverá prazo para aceitar a vaga?
* O sistema promoverá automaticamente o próximo participante?

**Prioridade:** Alta

**Status:** Pendente de validação

---

### LA04 — Critérios para emissão de certificado

**Descrição:**
O participante deseja emitir certificado depois do evento, mas não foi definido o critério necessário para ter direito à emissão.

**Impacto:**
Pode permitir emissão indevida ou impedir participantes legítimos de obter o certificado.

**Perguntas para esclarecimento:**

* A inscrição é suficiente para emissão?
* É necessária confirmação de presença?
* Existe percentual mínimo de participação?
* O certificado será emitido automaticamente?
* O organizador precisa aprovar a emissão?

**Prioridade:** Alta

**Status:** Pendente de validação

---

### LA05 — Envio de comprovantes e notificações

**Descrição:**
O participante deseja receber comprovante após a inscrição, mas o documento não informa como os comprovantes e demais notificações deverão ser enviados.

**Impacto:**
Não é possível definir completamente a funcionalidade de comunicação.

**Perguntas para esclarecimento:**

* O comprovante será disponibilizado na plataforma?
* Será enviado por e-mail?
* Haverá outras formas de notificação?
* Quais eventos deverão gerar mensagens automáticas?
* O participante poderá escolher como deseja ser notificado?

**Prioridade:** Média

**Status:** Pendente de validação

---

### LA06 — Momento da reserva de vaga em eventos pagos

**Descrição:**
Não está definido se a vaga é reservada quando o participante inicia o pagamento ou somente após sua confirmação.

**Impacto:**
Pode ocorrer venda de vagas acima da capacidade ou bloqueio desnecessário de vagas.

**Perguntas para esclarecimento:**

* A vaga fica reservada durante o pagamento?
* Existe prazo máximo para concluir o pagamento?
* O que acontece quando o pagamento expira?
* Outro participante poderá ocupar a vaga durante esse período?

**Prioridade:** Crítica

**Status:** Pendente de validação

---

### LA07 — Conflito de horário entre workshops

**Descrição:**
O documento informa que workshops no mesmo horário acontecem simultaneamente, mas não define como tratar a tentativa de inscrição de um participante em atividades conflitantes.

**Impacto:**
Pode permitir inscrições impossíveis de serem realizadas na prática.

**Perguntas para esclarecimento:**

* O sistema deverá bloquear a inscrição?
* Apenas apresentar um alerta?
* O participante poderá ignorar o alerta?
* Existe alguma exceção?

**Prioridade:** Alta

**Status:** Pendente de validação

---

### LA08 — Informações visíveis aos palestrantes

**Descrição:**
Os palestrantes desejam consultar a lista de participantes, mas não foi definido quais dados poderão ser visualizados.

**Impacto:**
Pode gerar exposição indevida de dados pessoais.

**Perguntas para esclarecimento:**

* Quais informações o palestrante realmente necessita?
* Nome completo será suficiente?
* Poderá visualizar e-mail ou telefone?
* Existem dados que deverão ser restritos?
* Há necessidade de consentimento específico?

**Prioridade:** Alta

**Status:** Pendente de validação

---

### LA09 — Requisitos de segurança

**Descrição:**
Não foram levantados requisitos de segurança durante a elicitação.

**Impacto:**
O sistema manipula dados pessoais e informações financeiras, tornando segurança um aspecto relevante.

**Perguntas para esclarecimento:**

* Como os usuários serão autenticados?
* Quais perfis e permissões existirão?
* Quais operações precisam de registro de auditoria?
* Existem políticas de segurança da organização?

**Prioridade:** Alta

**Status:** Pendente de validação

---

### LA10 — Requisitos de privacidade

**Descrição:**
Não foram definidos requisitos de privacidade para os dados dos participantes.

**Impacto:**
Pode afetar diretamente a forma de armazenamento, acesso e compartilhamento das informações.

**Perguntas para esclarecimento:**

* Quais dados pessoais serão coletados?
* Por quanto tempo serão mantidos?
* Quem poderá acessá-los?
* Existem regras de consentimento ou exclusão?

**Prioridade:** Alta

**Status:** Pendente de validação

---

### LA11 — Requisitos de desempenho

**Descrição:**
Não há valores definidos para tempo de resposta ou atualização das informações.

**Impacto:**
Expressões como “em tempo real” permanecem subjetivas e não verificáveis.

**Perguntas para esclarecimento:**

* Qual o tempo máximo aceitável para atualização de vagas?
* Qual o tempo esperado para consultas?
* Qual volume de usuários simultâneos deve ser suportado?

**Prioridade:** Média

**Status:** Pendente de validação

---

### LA12 — Requisitos de disponibilidade

**Descrição:**
Não foi definida a disponibilidade esperada para o sistema.

**Impacto:**
Períodos de inscrição e realização de eventos podem exigir maior disponibilidade.

**Perguntas para esclarecimento:**

* Existe percentual mínimo de disponibilidade?
* Existem períodos críticos?
* Qual o impacto aceitável de indisponibilidade durante inscrições?

**Prioridade:** Média

**Status:** Pendente de validação

---

### LA13 — Requisitos de acessibilidade

**Descrição:**
Nenhum requisito de acessibilidade foi identificado durante a elicitação.

**Impacto:**
Pode limitar o acesso de participantes com necessidades específicas.

**Perguntas para esclarecimento:**

* Existe padrão de acessibilidade obrigatório?
* Há exigência de conformidade com WCAG?
* Quais perfis de usuário precisam ser considerados?

**Prioridade:** Média

**Status:** Pendente de validação

---

## 3. Ambiguidades identificadas

### AM01 — “Em tempo real”

A expressão utilizada pelos organizadores não estabelece um critério mensurável.

Pode significar:

* atualização instantânea;
* atualização em poucos segundos;
* atualização após cada operação;
* atualização periódica.

É necessário definir um valor verificável.

---

### AM02 — “Logo após a inscrição”

O participante deseja receber comprovante “logo após a inscrição”.

A expressão é ambígua porque não define:

* se o comprovante é gerado imediatamente;
* se depende de pagamento;
* se depende de confirmação;
* qual o tempo máximo aceitável.

---

### AM03 — “Determinado tipo de inscrição”

A equipe financeira informa que determinadas inscrições só podem ser liberadas após o pagamento, mas não define quais.

É necessário esclarecer:

* quais eventos exigem pagamento;
* quais inscrições dependem de confirmação financeira;
* quem configura essa regra.

---

### AM04 — “Gerenciar participantes”

O interesse do organizador inclui gerenciar participantes, mas esse termo pode representar várias operações:

* consultar;
* editar;
* cancelar inscrição;
* confirmar presença;
* alterar status;
* emitir certificado;
* remover participante.

Essas possibilidades precisam ser validadas antes de gerar requisitos adicionais.

---

### AM05 — “Controlar reembolsos”

A responsabilidade da equipe financeira inclui controlar reembolsos, porém não está claro se o sistema deverá:

* apenas registrar o reembolso;
* calcular o valor;
* aprovar a solicitação;
* processar o pagamento;
* integrar-se a um meio de pagamento.

---

## 4. Possíveis inconsistências

### IC01 — Inscrição em vários workshops versus conflitos de horário

O participante expressa interesse em se inscrever em vários workshops no mesmo dia.

Ao mesmo tempo, os organizadores informam que workshops no mesmo horário podem ocorrer simultaneamente.

Essas duas informações não são necessariamente contraditórias, mas criam uma situação que precisa ser resolvida: um participante poderá se inscrever em workshops que acontecem ao mesmo tempo?

**Status:** Necessita decisão dos stakeholders.

---

### IC02 — Cancelamento versus reembolso

A possibilidade de cancelamento e o direito a reembolso aparecem como regras diferentes.

É necessário evitar a interpretação de que:

`cancelamento = reembolso`

O participante pode ter direito a cancelar sem necessariamente receber reembolso.

**Status:** Necessita definição de regras independentes.

---

### IC03 — Inscrição versus confirmação de pagamento

O documento utiliza o termo “inscrição” em situações nas quais a confirmação de pagamento pode ainda não ter ocorrido.

É necessário definir estados distintos, por exemplo:

* inscrição iniciada;
* aguardando pagamento;
* pagamento confirmado;
* inscrição confirmada.

Esses estados são apenas uma proposta conceitual e deverão ser validados antes de se tornarem parte da especificação.

---

## 5. Sugestões da IA não assumidas como definição

Durante a análise com IA Generativa, podem surgir sugestões plausíveis para preencher essas lacunas.

Exemplos:

* cancelamento permitido até 48 horas antes;
* reembolso integral até 7 dias antes;
* reserva da vaga por 15 minutos;
* lista de espera por ordem de chegada;
* certificado liberado com 75% de presença;
* atualização das vagas em até 2 segundos.

Nenhum desses valores deve ser tratado como requisito definitivo sem validação dos stakeholders.

---

## 6. Critério adotado

Foi utilizada a seguinte regra durante a análise:

> Quando o documento de elicitação não fornecer informação suficiente, a IA poderá ajudar a identificar a dúvida, mas não deverá decidir a resposta.

Assim, pontos indefinidos foram transformados em:

* lacunas;
* ambiguidades;
* inconsistências;
* perguntas de esclarecimento.

---

## 7. Papel da Inteligência Artificial Generativa

A IA Generativa apoiou principalmente:

* identificação de informações ausentes;
* análise de termos subjetivos;
* levantamento de possíveis conflitos;
* geração de perguntas para refinamento;
* separação entre informação confirmada e hipótese.

A revisão humana foi necessária para evitar que respostas plausíveis fossem incorporadas como decisões já tomadas.

---

## 8. Considerações finais

O documento de elicitação apresenta informações suficientes para identificar várias necessidades importantes do Sistema Eventus, mas ainda existem decisões relevantes que precisam ser esclarecidas.

O registro dessas lacunas evita que desenvolvedores, analistas ou ferramentas de IA preencham informações ausentes com suposições.

Esses pontos deverão ser validados com os stakeholders antes de sua incorporação definitiva aos requisitos e artefatos de especificação.
