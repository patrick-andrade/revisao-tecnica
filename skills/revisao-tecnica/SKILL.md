---
name: revisao-tecnica
description: Revisa a redação de textos técnicos e acadêmicos em português e propõe reescritas literais e exatas, agrupadas por tipo, para aprovação. Usar somente quando o usuário nomear explicitamente a skill revisao-tecnica.
license: MIT
disable-model-invocation: true
metadata:
  author: Patrick Andrade
  version: "1.0.0"
---

# Revisão técnica

Deixar o texto **literal** e **exato**. Cada frase diz o que afirma, com o termo do campo, sem imagem que o leitor precise traduzir e sem palavra que não trabalhe. A unidade de trabalho é a **fragilidade**: um trecho com localizador, forma atual, tipo e proposta de reescrita.

Exatidão não é peso. Uma reescrita que troca um verbo por três substantivos ou esconde quem age piora o texto, por mais formal que pareça. O teste de parada (passo 3) decide o que entra no relatório.

Os tipos de fragilidade, com teste, formas típicas, exemplos e exceções, estão em [references/catalogo.md](references/catalogo.md). As convenções de cada gênero textual estão em [references/generos.md](references/generos.md).

## Passos

### 1. Contexto

Identifique:

- o **gênero** e leia a seção dele em `generos.md`; gênero sem seção própria usa a mais próxima, e o relatório diz qual;
- o **leitor** (especialista do campo, gestor, banca, público amplo) e o **tema**; tema sensível é aquele em que uma imagem ou um rótulo pode ferir o leitor ou as pessoas descritas (saúde, morte e luto, infância, deficiência, pobreza e assistência social, segurança pessoal); nele, toda imagem corporal, de duplo sentido ou estigmatizante é mais grave;
- as **regras locais**: `AGENTS.md`, `CLAUDE.md`, guia de estilo da casa, normas da revista, edital ou termo de referência;
- o **formato** do arquivo e o localizador que ele permite: número de linha em texto puro (.md, .qmd, .tex, .txt), com a frase quando a linha for um parágrafo inteiro (L118, 3ª frase); seção e parágrafo (§3.2 ¶4) em .docx, PDF, Google Docs e página web; quadro, linha e coluna quando o trecho estiver numa tabela, inclusive tabela escrita em código;
- o que **não** se revisa: metadados, citações literais de terceiros e blocos que o autor não escreveu.

Concluído quando gênero, leitor, tema, regras locais, localizador e recorte estão definidos. Quando o documento pertence a um projeto com arquivo de regras (`AGENTS.md`, `CLAUDE.md`, guia de estilo) e a regra de redação técnica ainda não consta dele, ela vira o grupo **G0** do relatório (proposta de incluí-la). Documento avulso não tem G0.

### 2. Varredura

Leia o documento inteiro: parágrafos, listas, células de quadros, legendas, notas e apêndices. Aplique cada tipo do catálogo a cada trecho. Depois da leitura, busque no texto as formas típicas de cada tipo, com as ferramentas que tiver, para pegar o que a leitura deixou passar. A busca usa fronteira de palavra que funcione com acentos, ignora maiúsculas e cobre as flexões: as formas estão no infinitivo ou no singular, então busque também plural, feminino e tempos verbais, ou o radical ("endereç", "efetu"). Em .docx e PDF, busque no texto extraído.

Concluído quando todo trecho foi lido, toda forma típica foi buscada e todo tipo do catálogo está marcado como presente ou ausente.

### 3. Proposta e fidelidade

Para cada candidato, aplique primeiro o **teste de parada**. A reescrita entra no relatório só se fizer ao menos uma destas coisas:

- **(a)** troca o vago pelo verificável;
- **(b)** revela quem age ou põe o termo do campo;
- **(c)** desfaz uma imagem, um duplo sentido ou uma ambiguidade;
- **(d)** encurta a frase ou desfaz um encaixe sem perder sentido;
- **(e)** ajusta a força da afirmação à evidência;
- **(f)** cumpre uma convenção do gênero (`generos.md`) ou uma regra local registrada.

Se a reescrita ficar mais longa **e** mais nominal que o original, declare o ganho na própria proposta; sem ganho declarado, ela não entra. Troca de gosto (um sinônimo por outro de mesmo registro e mesma precisão) não entra: um verbo comum que já nomeia a operação fica.

A proposta é a **menor troca** que resolve a fragilidade: muda a expressão marcada e mantém o sujeito, a ordem e o resto da frase. Reestruturar a frase inteira só cabe quando a fragilidade é a própria estrutura (clivagem em G6, G8, G9, G10).

A proposta é **aplicável**: o texto que ela traz pode entrar no documento como está. Quando a correção depende de um dado que o documento não traz (um número, uma data, uma fonte), ela não vira item: vai para a seção "Dados a pedir ao autor". Intensificador ou adjetivo que não carrega informação vira item de corte, sem pedir dado: em G4 quando é quantidade vaga ("drasticamente"), em G5 quando reforça a própria afirmação ("farta evidência"). Uma imagem que carregava informação (G1) pode virar item literal e, ao mesmo tempo, linha de dado a pedir. Já a ambiguidade que o documento não resolve (duas leituras possíveis, nenhuma confirmável no texto) vira item com as leituras como opções. Uma frase que só repete o que o parágrafo já disse pode virar item de corte, no tipo do problema (G5 quando exagera, G11 quando é preenchimento).

Depois, confira cada proposta:

- **Sentido preservado:** afirma o mesmo que o original, nem mais nem menos; mantém condições, exceções e ressalvas. Quando a reescrita altera um conteúdo atribuído a uma fonte, reabra a fonte e confirme a fidelidade; se a fonte não estiver acessível, marque a proposta com "fidelidade à fonte não conferida". Em texto traduzido, a fonte é o original, quando acessível; sem ele, a reescrita preserva o sentido da tradução e recebe a mesma marca. A marca vai só nos itens que mudam o conteúdo, e não nos ajustes de forma.
- **Nada acrescentado:** a reescrita não ancora a frase em métrica, limite, causa ou agente que o texto não afirma.
- **Fatos com fonte:** toda quantificação nova (um percentual, uma lista de casos no lugar de "alguns") vem de fonte já citada no documento ou de parâmetro do próprio documento, com a localização. Em fonte com código (Quarto, R Markdown, LaTeX), o valor calculado entra como código inline, do mesmo modo que o documento já calcula os seus números.
- **Coerência terminológica:** a reescrita usa o termo que o documento usa no resto do texto.
- **Gramática:** a reescrita sai gramaticalmente correta, mesmo quando o trecho original tem erro; o erro corrigido de passagem é citado em "Notado fora do escopo".
- **Releitura:** releia a proposta procurando os mesmos tipos. Uma reescrita pode trazer metáfora nova ("eixos" no lugar de "pilares") ou nominalização em cadeia.

Quando houver duas reescritas defensáveis com custos diferentes (a mais exata depende de uma premissa), apresente as duas como opções (1) e (2) e nomeie a premissa. A opção (1) é a que não depende da premissa, ainda que seja um corte. Quando as duas opções dependem de premissa, nenhuma é padrão: o item só se aplica com a escolha explícita do usuário. Quando a única alternativa sem premissa é manter o trecho, a reescrita entra como item único, com a premissa nomeada.

### 4. Relatório para aprovação

Abra com um cabeçalho curto: gênero (e a seção de `generos.md` usada), leitor, tema, regras locais consideradas, recorte revisado e número de itens por grupo. Depois, apresente as fragilidades agrupadas por tipo, na ordem dos códigos do catálogo, e pare.

```
## G1. <tipo> — <por que é fragilidade aqui, em uma frase>

- **G1.1** (L118). Atual: "<trecho, com a expressão em negrito>". Proposta: "<reescrita>". [c]
- **G1.2** ...
```

- O código do grupo é o código do tipo no catálogo (G4 é sempre termo vago); grupos sem itens não aparecem. Cada item tem código próprio e termina com as letras dos critérios do teste de parada que atende, entre colchetes (itens de G0 dispensam as letras).
- **Um item é uma expressão**, registrada no tipo cujo teste nomeia o problema principal. Várias expressões do mesmo tipo na mesma frase formam um item; a mesma forma repetida em frases diferentes (cada "só" de G13) também, com todos os localizadores; as seções "Fronteira" do catálogo resolvem os casos entre tipos vizinhos. Um termo que muda de nome ao longo do texto (G3) é um item só, com todos os localizadores. Uma reestruturação (G8, G9, G10) é um item só e absorve as expressões de outros tipos dentro da frase, que o item lista.
- Quando uma frase tem itens de tipos diferentes, o último deles na ordem do relatório traz a nota "Com G…: <frase com todas as mudanças>", montada com a opção (1) de cada item que tiver opções.
- Quando a proposta de um item depende da escolha feita em outro (um pronome que retoma o sujeito reescrito na frase anterior), o item traz a nota "depende de G…" e a redação que vale para cada opção do outro item.
- Um grupo que só faz sentido inteiro (uma lista que precisa de paralelismo) recebe a nota "aprova-se ou recusa-se inteiro".
- **Dados a pedir ao autor:** uma linha por dado que tornaria um trecho verificável (localizador, trecho, dado que falta). Não tem código de aprovação.
- **O que deixei de fora de propósito:** os casos que o autor poderia esperar ver corrigidos e que ficaram, cada um com o motivo (seções "Não agir quando" e "Não é fragilidade" do catálogo, convenção do gênero, teste de parada). Ocorrências rotineiras de uma forma típica (pronomes com antecedente claro) cabem numa linha por forma.
- **Notado fora do escopo:** erro de ortografia, concordância, regência ou digitação; trecho truncado ou corrompido; erro factual ou numérico aparente; referência que não confere; marcas de texto gerado por IA (para a skill humanizer); problemas visuais e de formatação (para a skill ai-slop, se instalada). Registre sem corrigir.
- Feche com a linha de instrução de resposta, com os grupos deste relatório e nesta sintaxe: `G1, G4 menos G4.7, G6 com G6.3(2)`. Item com opções e sem escolha na resposta recebe a opção (1), salvo quando as duas dependem de premissa; nesse caso, pergunte.

Concluído quando todo candidato da varredura está decidido: num grupo, em "Dados a pedir ao autor" ou em "O que deixei de fora de propósito".

Nada é aplicado antes da aprovação, salvo quando o usuário autorizar expressamente a aplicação direta; nesse caso, entregue o relatório junto com o texto revisado.

### 5. Aplicação

Aplique só os itens aprovados, no próprio arquivo e no formato original:

- **Frase com vários itens:** monte a frase final com os itens aprovados da frase, na opção escolhida. Se a nota "Com G…" incluía um item recusado, refaça a frase sem ele.
- **Formato:** mude só o texto. Num .docx, edite com a ferramenta do formato, preservando estilos, numeração e formatação; use controle de alterações quando o usuário pedir.
- **Releitura:** depois de aplicar tudo, releia cada parágrafo alterado. Repetição ou quebra de coesão criada pela soma dos itens (duas frases seguidas que passam a começar com o mesmo sujeito) é relatada com uma proposta, e não aplicada sem nova aprovação.
- **Nova busca:** busque as expressões que os itens aprovados substituíram. Uma que sobrou num trecho aprovado é corrigida; uma fora dos itens aprovados, ou mantida de propósito pela própria proposta aprovada, é relatada, e não corrigida.

Entregue a lista do que foi aplicado (códigos e opções), as frases montadas a partir de vários itens, o resultado da nova busca e da releitura, e os "Dados a pedir ao autor" que continuam pendentes.

## Escopo

Quando o usuário limitar a revisão a grupos, seções ou trechos, revise só esse recorte e diga no cabeçalho do relatório o que ficou de fora.

A skill trata da redação. Autoria por IA, verificação de fatos e referências além do que o passo 3 exige, correção gramatical, formatação ABNT e visual do documento ficam fora; o que for notado vai para "Notado fora do escopo".
