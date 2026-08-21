# Eventus — Análise e Especificação de Requisitos com GenAI

## Sobre a atividade

Este repositório foi desenvolvido como atividade prática da unidade **Análise e Especificação de Requisitos com Inteligência Artificial Generativa**.

O exercício parte de um documento de elicitação previamente fornecido, referente ao **Sistema de Gestão de Eventos da empresa Eventus**.

A Eventus organiza congressos, workshops e eventos corporativos e atualmente utiliza formulários on-line e planilhas para controlar inscrições, vagas, pagamentos, cancelamentos e certificados.

O objetivo da atividade foi analisar as informações obtidas durante a elicitação e utilizar Inteligência Artificial Generativa como apoio para:

* identificar requisitos funcionais;
* analisar possíveis requisitos não funcionais;
* identificar regras de negócio;
* localizar lacunas, ambiguidades e inconsistências;
* selecionar os artefatos de especificação mais adequados;
* produzir e revisar esses artefatos.

---

## Estrutura do repositório

```text
eventus-requisitos-genai/
├── README.md
├── analise/
│   ├── requisitos-funcionais.md
│   ├── requisitos-nao-funcionais.md
│   ├── regras-de-negocio.md
│   └── lacunas-e-ambiguidades.md
└── especificacao/
    ├── historias-de-usuario.md
    ├── criterios-de-aceitacao.md
    ├── casos-de-uso.md
    └── matriz-de-rastreabilidade.md
```

---

## Análise de Requisitos

A primeira etapa do trabalho consistiu em transformar as informações obtidas nas entrevistas com os stakeholders em elementos estruturados de análise.

Foram produzidos os seguintes documentos:

* [Requisitos Funcionais](analise/requisitos-funcionais.md)
* [Requisitos Não Funcionais](analise/requisitos-nao-funcionais.md)
* [Regras de Negócio](analise/regras-de-negocio.md)
* [Lacunas e Ambiguidades](analise/lacunas-e-ambiguidades.md)

Durante essa etapa, foi adotado o cuidado de diferenciar informações já confirmadas pelos stakeholders de decisões ainda pendentes.

Sempre que o documento de elicitação não fornecia informações suficientes, o ponto foi registrado como:

* lacuna;
* ambiguidade;
* inconsistência;
* proposta a validar.

Essa abordagem foi utilizada para evitar que uma inferência da IA fosse transformada automaticamente em requisito definitivo.

---

## Artefatos de especificação escolhidos

Após a análise dos requisitos e das sugestões fornecidas pela IA Generativa, foram selecionados os seguintes artefatos de especificação:

### Histórias de Usuário

As Histórias de Usuário foram escolhidas para representar as necessidades do sistema a partir da perspectiva dos diferentes stakeholders:

* participantes;
* organizadores;
* equipe financeira;
* palestrantes.

Elas permitem manter o foco no valor esperado por cada perfil e facilitam a comunicação com a equipe de desenvolvimento.

Documento:

[Histórias de Usuário](especificacao/historias-de-usuario.md)

---

### Critérios de Aceitação em Gherkin

Os critérios de aceitação foram escritos no formato:

`Dado / Quando / Então`

Esse formato foi escolhido por tornar as histórias mais objetivas e verificáveis, além de criar uma base que poderá ser utilizada posteriormente para elaboração de casos de teste.

Nos pontos em que ainda existem lacunas de negócio, os critérios não foram completados com regras arbitrárias.

Documento:

[Critérios de Aceitação](especificacao/criterios-de-aceitacao.md)

---

### Casos de Uso

Os Casos de Uso foram utilizados de forma seletiva.

Em vez de produzir um caso de uso para cada funcionalidade, foram detalhados apenas os fluxos que apresentam maior quantidade de regras, decisões e exceções:

* inscrição em evento pago;
* cancelamento e reembolso;
* lista de espera.

Essa escolha evita redundância com as Histórias de Usuário e concentra o detalhamento nos processos mais complexos.

Documento:

[Casos de Uso](especificacao/casos-de-uso.md)

---

### Matriz de Rastreabilidade

A Matriz de Rastreabilidade foi utilizada para relacionar os diferentes artefatos produzidos.

A estrutura geral considerada foi:

`Requisito → Regra de Negócio → Lacuna → História de Usuário → Caso de Uso → Critério de Aceitação`

A matriz facilita a análise de impacto de mudanças e permite identificar quais pontos da especificação ainda dependem de validação dos stakeholders.

Documento:

[Matriz de Rastreabilidade](especificacao/matriz-de-rastreabilidade.md)

---

## Inteligência Artificial Generativa utilizada

A ferramenta utilizada durante a atividade foi o **ChatGPT, da OpenAI**.

A IA foi utilizada como ferramenta de apoio ao processo de Engenharia de Requisitos, e não como responsável pela tomada de decisão.

---

## Como a IA apoiou a atividade

A IA Generativa foi utilizada em diferentes etapas.

### Classificação das informações

A IA auxiliou na separação inicial entre:

* requisitos funcionais;
* requisitos não funcionais;
* regras de negócio;
* lacunas;
* ambiguidades;
* inconsistências.

---

### Identificação de lacunas

A IA foi particularmente útil para questionar informações incompletas.

Por exemplo, a elicitação informa que alguns cancelamentos dão direito a reembolso, mas não define quais situações geram esse direito.

Em vez de definir automaticamente uma regra, foram produzidas perguntas de esclarecimento para os stakeholders.

A mesma abordagem foi utilizada para:

* prazo de cancelamento;
* funcionamento da lista de espera;
* emissão de certificados;
* reserva de vagas durante pagamento;
* conflitos de horários;
* dados dos participantes visíveis aos palestrantes.

---

### Geração inicial dos artefatos

A IA apoiou a criação das primeiras versões de:

* Histórias de Usuário;
* Critérios de Aceitação;
* Casos de Uso;
* Matriz de Rastreabilidade.

Os resultados foram posteriormente revisados e ajustados.

---

### Exploração de fluxos alternativos

A IA também ajudou a identificar cenários que deveriam ser analisados além do fluxo principal, como:

* evento sem vagas;
* evento que não permite cancelamento;
* pagamento ainda não confirmado;
* cancelamento sem direito a reembolso;
* ausência de regras para movimentação da lista de espera.

---

## Sugestões da IA aproveitadas

Foram aproveitadas principalmente as sugestões relacionadas a:

* estruturação das Histórias de Usuário;
* uso de critérios de aceitação em Gherkin;
* identificação de fluxos alternativos e exceções;
* separação entre requisitos e regras de negócio;
* registro separado das lacunas;
* utilização de rastreabilidade entre os artefatos;
* uso seletivo de Casos de Uso para fluxos complexos.

---

## Sugestões modificadas

Algumas sugestões da IA foram consideradas úteis, mas precisaram ser ajustadas.

### Requisitos não funcionais

A IA sugeriu requisitos relacionados a:

* segurança;
* desempenho;
* disponibilidade;
* privacidade;
* acessibilidade.

Entretanto, o documento de elicitação informa que esses aspectos não foram levantados.

Por esse motivo, eles não foram registrados como requisitos definitivos, mas como **propostas a validar com os stakeholders**.

---

### Casos de Uso

Inicialmente, a IA poderia produzir casos de uso para praticamente todas as funcionalidades.

Essa abordagem foi simplificada.

Foram mantidos apenas os casos de uso em que o detalhamento dos fluxos agregava informação relevante à especificação.

---

### Critérios de Aceitação

Alguns critérios precisaram ser ajustados para não incluir regras que ainda não estavam definidas.

Quando a informação era insuficiente, o critério foi mantido acompanhado da respectiva lacuna.

---

## Sugestões descartadas

Foram descartadas sugestões que introduziam valores ou decisões sem respaldo no documento de elicitação.

Exemplos:

* cancelamento permitido até 24 ou 48 horas antes do evento;
* reembolso integral até determinado prazo;
* reserva de vaga por 15 minutos durante o pagamento;
* lista de espera obrigatoriamente organizada por ordem de chegada;
* certificado liberado após um percentual específico de presença;
* disponibilidade de 99,9%;
* resposta do sistema em até 2 segundos;
* definição de tecnologias específicas para implementação.

Essas sugestões poderiam ser plausíveis, mas representariam decisões não tomadas pelos stakeholders.

---

## Critério utilizado durante o uso da IA

Foi adotado o seguinte princípio:

> Quando a informação não estiver presente na elicitação, a IA pode ajudar a identificar a dúvida, mas não deve decidir a resposta.

Dessa forma, uma ausência de informação foi tratada como uma oportunidade de refinamento e não como autorização para completar automaticamente o requisito.

---

## Reflexão sobre o uso da IA Generativa

A IA Generativa mostrou-se útil principalmente para ampliar a cobertura da análise, organizar as informações e identificar aspectos que poderiam passar despercebidos em uma primeira leitura.

Também acelerou a elaboração inicial dos artefatos e permitiu explorar diferentes perspectivas e cenários de exceção.

Entretanto, a atividade também evidenciou uma limitação importante: modelos generativos tendem a preencher informações ausentes com respostas plausíveis.

Em Engenharia de Requisitos, esse comportamento exige atenção especial, pois uma resposta plausível não representa necessariamente uma decisão do stakeholder.

Por esse motivo, todas as sugestões foram analisadas criticamente antes de serem incorporadas à documentação.

A responsabilidade pela interpretação, priorização e decisão final permaneceu humana.

---

## Conclusão

A atividade permitiu aplicar a Inteligência Artificial Generativa como ferramenta de apoio à análise e especificação de requisitos.

O principal benefício observado foi a capacidade de acelerar a organização e exploração das informações.

Ao mesmo tempo, ficou evidente que a IA deve ser utilizada de maneira supervisionada, principalmente quando existem lacunas na elicitação.

A combinação entre análise humana e apoio da IA permitiu produzir uma especificação mais estruturada, rastreável e explícita quanto às decisões que ainda precisam ser validadas.
