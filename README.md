# revisao-tecnica

Skill para revisar a redação de textos técnicos e acadêmicos em português: propostas técnicas, relatórios, pareceres, notas técnicas, artigos e redação oficial.

A skill procura **fragilidades**: trechos em que o texto diz algo por meio de imagem, usa termo vago, esconde quem age, empilha substantivos ou mistura nomes para o mesmo conceito. Para cada uma, propõe uma reescrita literal e exata, agrupa as propostas por tipo e **para**, à espera da sua aprovação. Você aprova grupos inteiros e exclui itens soltos ("G1, G6 menos G6.3"); só então ela aplica.

Exatidão não é peso. A skill tem um teste de parada: uma reescrita só entra se tornar o texto verificável, revelar quem age, desfazer ambiguidade, encurtar, ajustar a força da afirmação à evidência ou cumprir uma convenção do gênero. Troca de gosto e "tecnicização" que só alonga a frase ficam de fora.

A skill **não** dispara por contexto. Ter um documento aberto e pedir "revise este texto" não basta: é preciso nomeá-la.

Funciona no [padrão aberto Agent Skills](https://agentskills.io/specification) (`SKILL.md`).

Guia: [Skills na Prática](https://patrick-andrade.github.io/guias/skills-na-pratica.html).

## O que ela faz

- Identifica gênero, leitor, tema e regras locais (guia da casa, normas da revista, edital) antes de revisar.
- Lê o documento inteiro, inclusive quadros, legendas e notas, e busca as formas típicas de 13 tipos de fragilidade.
- Entrega um relatório com código por item (G4.2), trecho atual, proposta e o critério que justifica a mudança. O que depende de um dado que só o autor tem (um número, uma fonte) vai numa lista à parte, "Dados a pedir ao autor", em vez de virar proposta com lacuna.
- Lista o que deixou de fora de propósito (termo técnico que parece metáfora, ressalva proporcional à evidência, convenção do gênero) e o que notou fora do escopo, como erros de digitação e de concordância.
- Depois da aprovação, aplica só os itens aprovados e confere que as formas removidas não voltaram.

| Código | Tipo |
|---|---|
| G1 | Metáfora e imagem |
| G2 | Ambiguidade e impropriedade |
| G3 | Inconsistência terminológica e sigla sem definição |
| G4 | Termo vago |
| G5 | Força da afirmação desproporcional à evidência |
| G6 | Verbo genérico e construção da fala |
| G7 | Jargão de gestão e locução verbal |
| G8 | Nominalização em cadeia e agente oculto |
| G9 | Frase longa ou encaixada |
| G10 | Lista sem paralelismo |
| G11 | Metadiscurso e preenchimento |
| G12 | Estrangeirismo desnecessário |
| G13 | Vocabulário do registro informal |

A skill não trata das marcas de texto gerado por IA (tríades, "não é X, é Y", travessões, vocabulário típico): para isso, use a [humanizer](https://github.com/blader/humanizer). Também não trata do visual do documento (use a [ai-slop](https://github.com/patrick-andrade/ai-slop)), não confere fatos nem referências e não formata segundo a ABNT.

## Instalar

**Neste projeto:**

```bash
npx skills add patrick-andrade/revisao-tecnica
```

**Em todos os projetos desta máquina:**

```bash
npx skills add patrick-andrade/revisao-tecnica --global
```

`npx` vem com o Node.js e baixa o instalador na hora. Sem isso, copie a pasta `skills/revisao-tecnica/` para:

```text
.agents/skills/revisao-tecnica/
├── SKILL.md
├── agents/
│   └── openai.yaml
└── references/
    ├── catalogo.md
    └── generos.md
```

na raiz do projeto. No Claude Code, o equivalente é `.claude/skills/revisao-tecnica/`. No Cursor, `.agents/skills/` também costuma bastar. Inclua `references/`; o `SKILL.md` sozinho não carrega o catálogo.

Abra um **chat novo** depois de instalar.

## Pedir

Nomeie a skill. No Codex, use `$revisao-tecnica`; no Claude Code e no Cursor, `/revisao-tecnica`.

```text
/revisao-tecnica

Revise a redação de relatorio-final.docx. Leitor: diretoria do órgão.
Mostre o relatório por grupo antes de alterar qualquer trecho.
```

Para limitar a revisão:

```text
/revisao-tecnica só G4, G5 e G8, nas seções 3 e 4 de artigo.qmd.
```

Para responder ao relatório, use os códigos:

```text
G1, G4, G6 menos G6.7, G8 com G8.2(1).
```

## Atualizar

Rode de novo o mesmo comando de instalação (com `--global`, se foi assim que instalou) e abra um chat novo. As mudanças de cada versão estão em [CHANGELOG.md](CHANGELOG.md).

## Referências

Os tipos, os testes e os critérios de "não agir" vêm das obras abaixo e de revisões reais aprovadas pelo autor.

- **Manual de Redação da Presidência da República**, 3ª ed., 2018 ([gov.br](https://www.gov.br/pt-br/servicos/consultar-o-manual-de-redacao-da-presidencia-da-republica)). Clareza, precisão, concisão, impessoalidade e formalidade; mesmo termo para a mesma ideia; estrangeirismo só quando indispensável; concisão sem perda de conteúdo. Base de G3, G4, G9, G11, G12 e da seção de redação oficial.
- **ISO 24495-1:2023**, *Plain language — Part 1: Governing principles and guidelines* ([ISO](https://www.iso.org/standard/78907.html); [resumo da IPLF](https://www.iplfederation.org/the-iso-plain-language-standard-part1)). O leitor encontra, entende e usa a informação; a revisão cobre estrutura e coesão, não só vocabulário.
- **Federal Plain Language Guidelines** ([digital.gov](https://digital.gov/guides/plain-language/writing)). Voz ativa, verbos escondidos em substantivos, uma ideia por frase, jargão. Base de G7, G8 e G9.
- **GOV.UK, A to Z style guide** ([GOV.UK](https://guidance.publishing.service.gov.uk/writing-to-gov-uk-standards/style-guides/a-to-z-style-guide/)). Lista de palavras a evitar com a troca recomendada; metáforas escondem o sentido. Base de G1 e G7.
- **Purdue OWL**, concisão e voz passiva ([concisão](https://owl.purdue.edu/owl/general_writing/academic_writing/conciseness/index.html); [voz passiva](https://owl.purdue.edu/owl/general_writing/academic_writing/active_and_passive_voice/choosing_passive_voice.html)). Preenchimento, redundância e usos legítimos da passiva. Base de G8 e G11.
- **Duke Scientific Writing**, voz passiva na escrita científica ([Duke](https://sites.duke.edu/scientificwriting/passive-voice-in-scientific-writing/)). Quando manter a passiva. Base de "Não agir quando" em G8.
- **Bryan A. Garner**, "A Bizspeak Blacklist", *Harvard Business Review*, 2013 ([HBR](https://hbr.org/2013/03/a-bizspeak-blacklist)). Jargão corporativo como sinal de piloto automático. Base de G7.
- **George Orwell**, "Politics and the English Language", 1946 ([Orwell Foundation](https://www.orwellfoundation.com/the-orwell-foundation/orwell/essays-and-other-works/politics-and-the-english-language/)). Metáforas gastas, locuções verbais, palavras sem referente; e a regra de quebrar qualquer regra antes de escrever algo bárbaro, que inspira o teste de parada.
- **Joseph M. Williams**, *Style: Lessons in Clarity and Grace*. Personagens como sujeitos, ações como verbos; quais nominalizações manter. Base de G8.
- **Helen Sword**, "Zombie Nouns", *The New York Times*, 2012 ([Opinionator](https://archive.nytimes.com/opinionator.blogs.nytimes.com/2012/07/23/zombie-nouns/)). Nominalização em excesso tira pessoas e ações da frase. Base de G8.
- **Steven Pinker**, *The Sense of Style*, 2014. Maldição do conhecimento, metadiscurso e ressalva compulsiva. Base de G5 e G11.
- **Ken Hyland**, metadiscurso, *hedges* e *boosters* na escrita acadêmica ([síntese](https://en.wikipedia.org/wiki/Metadiscourse)). A força da afirmação deve acompanhar a evidência. Base de G5.
- **Wikipedia**, *Signs of AI writing* ([Wikipedia](https://en.wikipedia.org/wiki/Wikipedia:Signs_of_AI_writing)). Consultada para separar o escopo desta skill do da humanizer.

## Licença

[MIT](LICENSE). Você pode usar, copiar e adaptar; mantenha o aviso de copyright e da licença.
