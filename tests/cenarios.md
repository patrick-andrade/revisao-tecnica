# Cenários de validação

Rode os cenários a cada mudança no `SKILL.md` ou no catálogo. Cada execução usa um agente novo, que recebe só o pedido do usuário e os arquivos da skill. Registre os resultados em `validacao.md`.

## 1. Invocação

- Em chat novo, com um documento aberto, o pedido "revise este texto" **sem** o nome da skill não a ativa.
- `/revisao-tecnica` (Claude Code, Cursor) e `$revisao-tecnica` (Codex) a ativam.

## 2. Sensibilidade (texto sintético)

Documento: [`sintetico.md`](sintetico.md). Gabarito: [`sintetico-gabarito.md`](sintetico-gabarito.md), que o agente executor não pode ler.

Critério: ao menos 22 dos 27 itens plantados encontrados, com o código esperado ou um código vizinho justificado; nenhuma das armadilhas marcada; toda proposta com o critério do teste de parada.

## 3. Regressão (documento privado do autor)

Documento real do autor, na versão anterior a uma revisão que ele aprovou, com a versão aprovada como gabarito (por exemplo, dois commits de um projeto). Fica fora do repositório; o resultado é registrado só como contagem, sem citar o documento.

Critério: a skill reencontra a maior parte dos itens aprovados naquela revisão, e as propostas novas passam no teste de parada.

## 4. Calibragem (documentos públicos bem editados)

Trechos de 1.500 a 3.000 palavras de documentos publicados. Os textos ficam em `tests/corpus/` (ignorado pelo Git); aqui ficam só a referência e o localizador.

| Nº | Gênero | Documento | Licença ou condição | Trecho |
|---|---|---|---|---|
| 01 | Relatório técnico | Banco Mundial, [*Emprego e Crescimento: A Agenda da Produtividade*](https://hdl.handle.net/10986/29808), 2018 | CC BY 3.0 IGO | cap. 1, p. 1–9 |
| 02 | Comunicado institucional | FMI, [declaração final da missão do Artigo IV ao Brasil](https://www.imf.org/pt/news/articles/2019/05/24/mcs052419-brazil-staff-concluding-statement-of-the-2019-article-iv-mission), 2019 | documento público de organismo multilateral, usado para pesquisa | íntegra (cerca de 2.000 palavras); o site bloqueia download automatizado, então salve a página pelo navegador |
| 03 | Nota técnica (boxe) | BCB, ["Novo crédito consignado privado"](https://www.bcb.gov.br/content/ri/relatorioinflacao/202509/rpm202509b5p.pdf), *Relatório de Política Monetária*, set. 2025 | reprodução com citação da fonte | boxe inteiro, p. 57–63 |
| 04 | Relatório técnico (TD) | Ipea, [TD 3192, *Cenários de expansão do Pé-de-Meia*](https://repositorio.ipea.gov.br/handle/11058/20813), 2026 | reprodução com citação, não comercial | seções 1–2, p. 6–13 |
| 05 | Parecer (voto) | TCU, [Acórdão 2828/2026-Plenário](https://contas.tcu.gov.br/sagas/SvlVisualizarRelVotoAc?codFiltro=SAGAS-SESSAO-ENCERRADA&seOcultaPagina=S&item0=917905) | ato oficial (Lei 9.610/1998, art. 8º, IV) | voto, p. 28–31 |
| 06 | Artigo acadêmico | Luduvice e Pires, ["Indicadores antecedentes de dificuldades financeiras estaduais"](https://www.scielo.br/j/neco/a/jvmXQNnhYkczh4GKd5Hhthm/?lang=pt), *Nova Economia*, 2026 | CC BY 4.0 | seções 1–2, p. 1–7 |
| 07 | Artigo acadêmico | Silva, ["Os efeitos do Programa Bolsa Família (PBF) no mercado de trabalho"](https://www.scielo.br/j/ee/a/Rdc896ZHGvvCGL4sWhFVTmH/?lang=pt), *Estudos Econômicos*, 2026 | CC BY 4.0 | seções 1–2, p. 2–7 |

Os documentos 01 e 07 têm erros de digitação e de concordância nos originais. A skill deve registrá-los em "Notado fora do escopo", sem tratá-los como fragilidade de estilo.

Critério, por documento: nenhuma proposta troca termo técnico consagrado; toda proposta declara o critério do teste de parada e passa na conferência manual; o número de propostas por mil palavras fica registrado, para comparação entre versões.

## 5. Formato e aprovação

Em qualquer cenário: o relatório abre com a linha de contexto, usa os códigos do catálogo, traz "O que deixei de fora de propósito" e a linha de instrução de resposta, e nada é aplicado antes da aprovação.

## 6. Aplicação

Aprove parte dos itens de um relatório sobre um `.md` e sobre um `.docx`. Critério: só os itens aprovados mudam, a formatação do `.docx` se mantém e a nova busca não encontra as formas removidas nos itens aprovados.
