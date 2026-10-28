# Catálogo de fragilidades

Tipos aplicados na varredura e usados como grupos do relatório. Os códigos são fixos e seguem a gravidade, do risco ao sentido (G1, imagem; G2, ambiguidade) ao registro de vocabulário (G13). G0 é reservado à proposta de regra local. Grupo sem ocorrência não aparece no relatório, e os demais mantêm o código.

Cada tipo traz: **O que é**, **Teste**, **Formas típicas** (lista para a busca textual do passo 2), exemplos de antes e depois e **Não agir quando**; alguns trazem **Fronteira**, que diz onde registrar o caso que reprova em dois tipos. Registre cada ocorrência uma vez, no tipo cujo teste nomeia o problema principal. Exemplos sem marca vieram de revisões aprovadas pelo autor, adaptados para não identificar a origem; os marcados *ilustrativo* aguardam confirmação numa revisão real.

As formas típicas localizam candidatos; quem decide é o teste do tipo e o teste de parada do SKILL.md.

## G1. Metáfora e imagem

**O que é:** a expressão diz uma coisa por meio de outra, e o leitor precisa traduzi-la. Em tema sensível, a imagem pode evocar sentido inadequado.

**Teste:** a frase continua verdadeira lida ao pé da letra? Se não, é imagem.

**Formas típicas:** dar peso, peso, alavanca, pilar, pilares, eixo, eixos, caminho, porta de entrada, ponte, premiar, frágil, sólido, robusto, visível, aparecer como, passar pelas mãos, bem construído, fraco, janela, gargalo, guarda-chuva, termômetro, motor, raiz, berço, vitrine, carro-chefe, pano de fundo, divisor de águas, na ponta.

| Atual | Literal |
|---|---|
| os pacientes passam todos os dias por suas mãos | atendem diretamente esses pacientes todos os dias |
| o que dá peso prático ao critério de manutenção preventiva | circunstância que confere relevância prática ao critério 7, relativo à manutenção preventiva (ganho: nomeia o critério) |
| uma política bem construída não aparecerá como fraca sem explicação, e a lacuna de cobertura ficará visível | essa classificação impede que uma política seja interpretada como deficiente sem essa ressalva e explicita a eventual lacuna de cobertura |
| cada tipo de documento chega por um caminho | cada tipo de documento tem um canal de acesso próprio |
| para que o contratante não se apoie num número frágil | para que o contratante não tome como conclusivo um índice que dependa da regra de agregação adotada |
| também premia uma leitura equivocada aplicada sempre do mesmo modo | também atribui consistência a uma interpretação equivocada aplicada de modo uniforme |
| numa operação terceirizada, a alavanca está no contrato | numa operação terceirizada, a alteração depende do contrato |
| é um dos pilares da campanha | integra a campanha |

A reescrita boa descreve a relação ("integra"); trocar uma imagem por outra ("pilares" por "eixos") não resolve. Se a imagem carregava uma informação (prioridade, centralidade), a reescrita a diz de forma literal e com fonte ("é uma das três ações prioritárias do plano"), ou pede o dado ao autor.

**Não agir quando:** o termo é o nome técnico no campo ("robusto" em estatística, "janela" em séries temporais, "ponte" em engenharia, "gargalo" em teoria das filas), ou a imagem é a única forma consagrada de nomear o objeto ("curva de aprendizagem"), ou é o nome de uma divisão definida no próprio documento ou na norma que ele segue ("eixo 2 do programa"), ou é sentido figurado dicionarizado e corrente no gênero ("a inflação arrefeceu", "demanda aquecida"), ou é rótulo da literatura citado entre aspas e atribuído ("o chamado 'efeito X' (Autor, ano)"). O mesmo rótulo adotado pelo autor sem aspas nem atribuição, em tema sensível, é fragilidade.

## G2. Ambiguidade e impropriedade

**O que é:** trecho que admite duas leituras ou que usa uma palavra em sentido que ela não tem. Inclui pronome, demonstrativo ou elipse com mais de um antecedente possível ou com antecedente distante; modificador de alcance incerto ("riscos associados à seleção e à execução"); base de percentual indefinida ("sendo que 19,5%"); palavra imprópria ("observância" por "observação").

**Teste:** aponte o antecedente, o alcance ou o sentido. Se houver duas leituras, se o antecedente estiver a mais de uma frase, ou se "o mesmo" funcionar como pronome, é fragilidade.

**Formas típicas:** ele, ela, eles, elas, isso, isto, este, esta, esse, essa, o mesmo, a mesma, os mesmos, as mesmas, tal, tais, o referido, a referida, aquele, aquela, o qual, a qual, este último, esta última, o primeiro, o segundo.

| Atual | Exato |
|---|---|
| (antecedente a duas frases de distância) ele é o próprio local de trabalho | o hospital é o próprio local de trabalho |
| Os dados foram enviados ao laboratório, e **o mesmo** os analisou em março. | Os dados foram enviados ao laboratório, que os analisou em março. *(ilustrativo)* |
| A taxa de resposta caiu e o custo por entrevista subiu. **Isso** indica perda de eficiência. | A queda da taxa de resposta e a alta do custo por entrevista indicam perda de eficiência. *(ilustrativo)* |

**Não agir quando:** o antecedente é único e está na frase anterior, ou o contexto o resolve sem esforço. Repetir o substantivo em toda frase pesa o texto sem ganho.

## G3. Inconsistência terminológica e sigla sem definição

**O que é:** o mesmo conceito com nomes diferentes ao longo do documento, ou a mesma palavra com dois sentidos; sigla usada antes de ser definida.

**Teste:** liste os termos-chave do documento (os definidos, os do título, os das variáveis e critérios). Cada um tem um só nome do início ao fim? Cada sigla aparece por extenso na primeira ocorrência?

**Formas típicas:** sem lista fixa. Busque cada termo-chave e seus sinônimos prováveis, e as palavras em maiúsculas de 2 a 6 letras (siglas).

| Atual | Exato |
|---|---|
| "taxa de evasão" na seção 2, "abandono" na seção 3, "desistência" na tabela 4, para o mesmo indicador | "taxa de evasão" em todo o documento, definida na primeira ocorrência *(ilustrativo)* |
| a matriz é categórica, mas o texto fala em "notas" | "classificações" |
| o FNDE repassou… (primeira ocorrência) | o Fundo Nacional de Desenvolvimento da Educação (FNDE) repassou… *(ilustrativo)* |

Sigla de órgão, programa ou indicador de âmbito nacional, cuja forma por extenso é pública, é expandida na proposta; sigla local ou do próprio projeto vai para "Dados a pedir ao autor".

Nome próprio (programa, lei, órgão, projeto) com duas grafias no documento também é G3: a proposta usa a grafia do ato ou do sítio oficial, citado no item; sem como conferir, as duas grafias viram opções (1) e (2).

**Não agir quando:** a sigla é de uso corrente para o leitor do gênero (PIB, IBGE, ONU em texto de economia), ou a variação nomeia de propósito conceitos diferentes. A regra vale para os termos-chave: sinônimo de termo-chave usado "para não repetir" é fragilidade. Palavra comum, fora dos termos-chave, pode variar para evitar repetição próxima.

## G4. Termo vago

**O que é:** intensificador, quantificador, marcador de tempo ou adjetivo valorativo sem medida; atribuição a fonte indeterminada; termo comum no lugar do termo técnico do campo.

**Teste:** o leitor consegue verificar a afirmação? Se a resposta depende de "quanto?", "quais?", "quem?" ou "desde quando?", quantifique ou nomeie, sempre com fonte (passo 3 do SKILL.md).

**Formas típicas:** bem, muito, bastante, pouco, alguns, algumas, vários, várias, diversos, diversas, inúmeros, curto, longo, tarde, cedo, hoje, atualmente, recentemente, nos últimos anos, expressivo, significativo, considerável, notável, relevante, importante, especialistas, estudos mostram, a literatura aponta, sabe-se que, sorteio.

| Atual | Exato |
|---|---|
| há redes em transição em alguns estados | há redes em transição ou recém-reestruturadas, como nos dois estados citados na seção 2 |
| depende de alguns insumos | depende dos seguintes insumos |
| hoje de R$ 1.200,00 (a resolução que fixa o valor está citada na seção 4) | de R$ 1.200,00, valor fixado pela resolução citada na seção 4 (ganho: a data passa a ser verificável pelo ato) |
| a diária proposta fica bem abaixo desse parâmetro | a diária proposta corresponde a cerca de 40% do valor de 8 horas por esse parâmetro (R$ 2.400,00); calculado a partir dos parâmetros do documento, com a premissa de 8 horas declarada |
| Prazo total curto | Prazo total de 30 dias úteis |
| Documentos chegam tarde | Recebimento de documentos após a segunda entrega (P2) |
| um sorteio simples | uma amostra aleatória simples |
| houve um aumento expressivo da arrecadação (a tabela 3 traz 12% entre 2022 e 2024) | a arrecadação aumentou 12% em termos reais entre 2022 e 2024 (tabela 3) *(ilustrativo)* |
| o custo de transação pode cair drasticamente | o custo de transação pode cair *(ilustrativo)* |

Quando o documento não traz o dado ("estudos mostram" sem citação; "várias escolas" sem número em lugar nenhum), o caso vai para "Dados a pedir ao autor", e não para o grupo. Só vira item o vago que se resolve com informação do próprio documento ou com corte.

**Não agir quando:** "significativo" se refere a teste estatístico informado (se não se sabe se o sentido é estatístico ou de magnitude, o caso é G2, com as duas leituras como opções); o vago é proposital e declarado (estimativa preliminar, intervalo); "atualmente" vem com data ou ato que o fixa; o tempo relativo ("hoje", "nos últimos cinco anos") se ancora na data do documento e o ano dos dados é o mesmo; o resumo, a introdução ou o sumário executivo antecipam com palavras o que o corpo quantifica.

**Fronteira com G5:** adjetivo ou advérbio que reforça a própria afirmação ("farta evidência", "inovadora", "claramente") é G5; quantidade, prazo ou fonte indeterminados são G4.

## G5. Força da afirmação desproporcional à evidência

**O que é:** *booster* (comprova, claramente, sem dúvida) em afirmação que a evidência não sustenta; ou *hedges* empilhados (pode eventualmente sugerir) em afirmação estabelecida.

**Teste:** qual é a evidência da frase (dado, estimativa, citação, inferência do autor)? A força do verbo e dos modificadores corresponde a ela? Resultado correlacional ou de amostra pequena pede "indica", "sugere", "está associado a"; fato estabelecido e citado dispensa ressalva.

**Formas típicas:** comprova, comprovam, demonstra, demonstram, prova, provam, claramente, evidentemente, obviamente, certamente, sem dúvida, inegável, indiscutível, sempre, nunca, todos, possivelmente, eventualmente, talvez, parece sugerir, de certa forma, em certa medida, pode vir a.

| Atual | Exato |
|---|---|
| Os resultados comprovam que o programa reduziu a evasão. (regressão sem estratégia de identificação) | Os resultados indicam que o programa está associado a menor evasão. *(ilustrativo)* |
| Esses dados podem eventualmente sugerir uma possível relação entre renda e frequência. | Esses dados sugerem uma relação entre renda e frequência. *(ilustrativo)* |

**Não agir quando:** a ressalva corresponde ao desenho do estudo (preserve "sugere" em resultado correlacional); o *booster* vem acompanhado do teste ou da fonte que o sustenta.

## G6. Verbo genérico e construção da fala

**O que é:** verbo de sentido amplo (ver, mostrar, fazer, ficar, dar, caber, haver) ou construção oral (clivagem "o que se faz é", "a pergunta é", "quem tem") no lugar do verbo que nomeia a operação.

**Teste:** existe um verbo que nomeia exatamente a operação (identificar, verificar, examinar, reproduzir, registrar, requerer)? Se existe, use-o, como verbo. Trocar o verbo genérico por um substantivo ("fazer" por "a realização de") é G8, e não correção.

**Formas típicas:** ver, mostrar, mostra, fazer, refazer, ficar, fica, caber, cabe, há, dizer, dirá, ideias, coisa, coisas, o que se, a pergunta é, a quem tem, quem tem, o que pedir.

| Atual | Técnico |
|---|---|
| assim será possível ver o que cada plano já garante, onde fica aquém desse padrão e o que falta | com essa matriz, será possível identificar, em cada plano, o que já está previsto, as lacunas em relação a esse padrão e as alterações necessárias |
| dirigidas a quem tem instrumento para mudar cada plano | dirigidas ao ator com competência para alterar cada plano |
| O que se avalia é o conteúdo normativo | Avalia-se o conteúdo normativo |
| o que importa num setor em contato permanente com o público | aspecto relevante para um setor em contato permanente com o público |
| a equipe poderá refazer qualquer avaliação | esse registro permitirá à equipe reproduzir qualquer avaliação |
| o relatório dirá isso de forma explícita | o relatório registrará essa alteração explicitamente |
| é um primeiro passo razoável: não exige um segundo avaliador e cabe no prazo | é um procedimento inicial adequado: dispensa um segundo avaliador e é compatível com o prazo |
| a pergunta é se o texto trata os riscos | verifica-se se o texto trata os riscos |
| em qualquer arranjo, há a comissão interna e o acordo coletivo | em qualquer arranjo, estão disponíveis a comissão interna e o acordo coletivo |
| indicando o que pedir, a quem e por qual via | indicando a medida a recomendar, o destinatário e o instrumento de alteração |
| essa combinação se aplica diretamente a uma pesquisa que exige ler documentos normativos | essa formação é pertinente a uma pesquisa que exige ler documentos normativos |

**Não agir quando:** o verbo comum já é exato ("o gráfico 2 mostra a série mensal"; "a amostra tem 1.200 domicílios"). Trocar "mostra" por "evidencia" sem ganho de precisão é troca de gosto: "a busca preliminar já mostra essa diferença" fica como está.

## G7. Jargão de gestão e locução verbal

**O que é:** verbo ou expressão de jargão corporativo que não nomeia ação concreta (alavancar, endereçar, entregar), ou locução que dilui um verbo simples em verbo-suporte mais substantivo (fazer uso de, dar origem a, realizar a análise de).

**Teste:** dá para dizer qual ação concreta, sobre qual objeto? Existe um verbo simples com o mesmo sentido? Se sim, use-o.

**Formas típicas:** alavancar, endereçar, entregar, entrega, entregas, impactar, potencializar, otimizar, agregar valor, sinergia, empoderar, estratégico, estratégica, robustez, robustecer, mapear, engajar, engajamento, fazer uso de, dar origem a, levar a cabo, proceder à, proceder ao, realizar a, realizar o, efetuar, no sentido de, com vistas a.

| Atual | Exato |
|---|---|
| o projeto vai alavancar os resultados da rede | o projeto pretende aumentar a taxa de aprovação da rede *(ilustrativo)* |
| a proposta endereça o problema da fila | a proposta reduz o tempo de espera na fila *(ilustrativo)* |
| a equipe fará uso de dados administrativos | a equipe usará dados administrativos *(ilustrativo)* |
| a mudança deu origem a atrasos | a mudança causou atrasos *(ilustrativo)* |

**Não agir quando:** o termo tem sentido técnico no campo ("alavancagem" em finanças, "entregável" como item de contrato ou termo de referência, "fomento" como modalidade de política pública, "mapear" em cartografia).

**Fronteira com G1:** verbo de jargão ("alavancar", "endereçar") é G7; substantivo-imagem ("alavanca", "pilar") é G1.

## G8. Nominalização em cadeia e agente oculto

**O que é:** ação transformada em substantivo (-ção, -mento, -idade, -ância) encadeada com outras por "de", com verbo fraco; ou passiva e "-se" que escondem quem age onde o leitor precisa saber (recomendação, responsabilidade, decisão). É o risco oposto ao G6: o texto parece técnico e fica opaco.

**Teste:** sublinhe as primeiras palavras de cada frase. O sujeito é longo e abstrato? A ação principal está num substantivo? Há dois ou mais substantivos de ação em cadeia na mesma oração? Numa recomendação ou atribuição de responsabilidade, o leitor sabe quem age?

**Formas típicas:** realização de, efetivação de, implementação de, implantação de, promoção de, viabilização de, otimização de, operacionalização de, foi realizado, foi realizada, foram realizados, foram identificados, recomenda-se, sugere-se, propõe-se, faz-se necessário, torna-se necessário.

| Atual | Exato |
|---|---|
| A realização da avaliação da implementação do programa foi efetuada pela equipe técnica. | A equipe técnica avaliou a implementação do programa. *(ilustrativo)* |
| Recomenda-se a revisão do contrato até junho. | A secretaria deve revisar o contrato até junho. (se o documento identifica a secretaria como responsável) *(ilustrativo)* |
| Faz-se necessária a promoção da capacitação dos servidores. | Os servidores precisam ser capacitados. / A escola de governo deve capacitar os servidores. *(ilustrativo)* |

**Não agir quando:** a nominalização nomeia um conceito do campo ("a inflação", "a desigualdade de renda") ou retoma a frase anterior ("Essa redução…"); a passiva ou o "-se" estão na seção de métodos, o agente é óbvio ou irrelevante, ou o gênero exige impessoalidade (ver `generos.md`); o item é de lista nominalizada (G10).

**Fronteira com G6:** verbo-suporte com substantivo de ação ("a aplicação deveria ser feita", "realizar a análise") é G8 quando há cadeia de substantivos ou agente oculto, e G7 quando é só a locução; o verbo genérico sozinho ("ver", "mostrar") é G6.

## G9. Frase longa ou encaixada

**O que é:** frase que obriga o leitor a guardar várias informações antes de chegar ao verbo ou à conclusão: muitas intercalações, sujeito longe do verbo, condição, exceção e ressalva na mesma frase.

**Teste:** basta uma das condições: (1) a frase tem mais de cerca de 30 palavras **e** duas ou mais intercalações; (2) o núcleo do sujeito está separado do verbo por mais de cerca de 10 palavras, com ou sem pontuação. Intercalação é um trecho entre vírgulas, travessões ou parênteses que separa sujeito e verbo, ou verbo e complemento; enumeração, oração final de gerúndio e indicação de autoria ("desenvolvido por Autor (ano)") não contam. Essas exceções valem para as duas condições, e o nome próprio por extenso (de lei, programa ou órgão) não conta na distância entre sujeito e verbo. Se alguma condição se cumpre, divida ou reordene em ordem direta.

**Formas típicas:** sem lista fixa. Procure parágrafos de uma só frase, frases com três ou mais vírgulas antes do verbo principal e cadeias de "que… que…".

| Atual | Exato |
|---|---|
| O levantamento, que, conforme previsto no plano de trabalho aprovado em março, deveria abranger todas as unidades da rede, inclusive as conveniadas, foi concluído em apenas 60% delas. | O plano de trabalho aprovado em março previa levantamento em todas as unidades da rede, inclusive as conveniadas. O levantamento foi concluído em 60% delas. *(ilustrativo)* |

**Não agir quando:** a frase é longa, mas linear: sujeito, verbo e complemento em ordem direta, seguidos de coordenadas ou de enumeração; dividir quebraria uma condição que precisa estar junto da regra.

## G10. Lista sem paralelismo

**O que é:** itens de lista com classes gramaticais diferentes, ou redigidos como perguntas faladas ("o que ele chama de", "por onde a pessoa denuncia", "se trata de"), com sujeito vago ("a pessoa", "o caso").

**Teste:** todos os itens começam com a mesma classe gramatical? Cada item nomeia um objeto de análise?

**Correção:** pôr todos os itens no mesmo padrão. Em lista de objetos de análise, o padrão é o substantivo; em lista de ações, o verbo no infinitivo. O grupo se aprova inteiro, porque o paralelismo vale para a lista toda.

**Formas típicas:** só no início de itens de lista (na prosa, não são candidatos): o que, por onde, quem, que, se, como.

| Atual | Paralelo |
|---|---|
| o que ela chama de dado pessoal, e se inclui o coletado por terceiros | a definição de dado pessoal adotada e a inclusão dos dados coletados por terceiros |
| por onde a pessoa denuncia e quem apura | os canais de denúncia e a instância responsável pela apuração |
| que proteção ela recebe durante e depois do caso | as medidas de proteção ao denunciante durante e após a apuração |
| se alcança o pessoal terceirizado | a cobertura do pessoal terceirizado |
| que papel dá ao encarregado e ao comitê | as atribuições conferidas ao encarregado e ao comitê |
| quem faz o acompanhamento, e com que periodicidade | a instância responsável pelo acompanhamento, e a periodicidade prevista |

**Não agir quando:** a lista é de perguntas de pesquisa ou de roteiro de entrevista, em que a forma de pergunta é o conteúdo.

## G11. Metadiscurso e preenchimento

**O que é:** frase ou expressão que anuncia o conteúdo em vez de dizê-lo ("cabe destacar que"), expressão de enchimento ("no que tange a", "em termos de") ou redundância ("planejamento prévio", "elo de ligação").

**Teste:** apague a expressão. A frase perde informação? Se não, a expressão é preenchimento.

**Formas típicas:** cabe destacar, cabe ressaltar, cabe salientar, é importante destacar, é importante ressaltar, é importante salientar, vale ressaltar, vale lembrar, vale destacar, convém notar, nesse sentido, nesse contexto, de forma geral, de modo geral, no que tange, no que se refere, no que diz respeito, a nível de, em termos de, ao longo deste trabalho, planejamento prévio, elo de ligação, consenso geral, outra alternativa, acrescentar mais, há anos atrás.

| Atual | Exato |
|---|---|
| Cabe destacar que a inflação de serviços caiu no trimestre. | A inflação de serviços caiu no trimestre. *(ilustrativo)* |
| No que tange à questão da arrecadação, houve queda. | A arrecadação caiu. *(ilustrativo)* |
| Nesta seção, apresentaremos os resultados, que serão discutidos a seguir. (nota técnica de quatro páginas) | (frase removida) *(ilustrativo)* |

**Não agir quando:** o metadiscurso orienta a leitura num documento longo (roteiro do artigo na introdução, remissão a seção ou anexo), ou marca uma ressalva real, isto é, a frase que segue limita ou contradiz o que veio antes ("convém notar que a série muda de metodologia em 2020").

## G12. Estrangeirismo desnecessário

**O que é:** palavra estrangeira com equivalente consagrado em português, ou termo estrangeiro necessário sem itálico ou sem explicação na primeira ocorrência.

**Teste:** existe termo em português com o mesmo sentido, usado no campo? Se sim, use-o. Se não existe, o termo fica em itálico e é explicado na primeira ocorrência.

**Formas típicas:** feedback, gap, insight, insights, framework, benchmark, stakeholders, stakeholder, deadline, performance, budget, report, paper, workshop, briefing, follow-up, input, inputs, output, outputs, roadmap, overview, case, expertise, approach.

| Evitar | Usar |
|---|---|
| gap | lacuna; o termo do campo, quando houver ("defasagem de aprendizagem") |
| feedback | retorno, devolutiva |
| insight | constatação, achado |
| framework (conceitual) | referencial, quadro analítico |
| benchmark | referência comparativa, parâmetro |
| stakeholders | partes interessadas |
| performance | desempenho |
| input / output | insumo / produto |
| roadmap | roteiro, cronograma |

**Não agir quando:** o termo é consagrado no campo sem equivalente exato (*trade-off*, *spillover*, *dummy*, *software*, *hedge* em finanças): mantenha-o em itálico e explicado na primeira ocorrência. O termo estrangeiro entre parênteses como glosa do termo em português ("sistemas de alerta antecipado (*early warning systems*)") também fica. Estrangeirismo dicionarizado e corrente no campo (*commodity*, *markup*) fica. Nome próprio, nome de método (*Causal Forest*), título de obra e citação literal ficam como estão.

## G13. Vocabulário do registro informal

**O que é:** palavra correta, mas de registro coloquial, com equivalente formal de mesmo sentido.

**Formas típicas:** só, só que, junto com, o combinado, deixar de fora, a gente, pra, tá, bater com, dar conta de.

| Evitar | Usar |
|---|---|
| só | apenas, somente |
| só que | mas |
| junto com | acompanhado de, com |
| o combinado | o acordado |
| deixar de fora | excluir |
| a gente | nós, ou quem age ("a equipe") |
| pra, tá | para, está |
| bater com | coincidir com |
| dar conta de | cumprir, abranger |

É o grupo mais mecânico: a busca textual encontra quase tudo. Confira cada ocorrência no contexto antes de propor ("só" dentro de citação literal fica).

**Não agir quando:** o gênero admite registro menos formal (texto de divulgação, apresentação oral transcrita), ou a palavra está em citação literal.

## Não é fragilidade

Liste estes casos na seção "O que deixei de fora de propósito" do relatório, com o motivo.

- **Contrações "num", "numa", "dum":** aceitas na norma escrita formal; trocá-las pesa o texto sem ganho de precisão.
- **Convenções de gênero textual:** escalas de proficiência de currículo ("compreende bem", "fala razoavelmente"), fórmulas de carta e de ofício, estrutura obrigatória de edital (ver `generos.md`).
- **Termos de documento de referência:** categorias e redação de termo de referência, edital, norma ou contrato ("atende totalmente"), que o texto deve reproduzir, inclusive qualificadores que vêm de lá.
- **Locuções consagradas do registro técnico, jurídico ou contratual:** "nos termos de", "no âmbito de", "a título de", "em caráter", quando são a forma usual do gênero; parafraseá-las não ganha precisão.
- **Citação literal:** o trecho entre aspas preserva a forma da fonte.
- **Termo técnico que parece metáfora ou jargão:** "estabilidade" e "replicabilidade" (confiabilidade em análise de conteúdo), "matriz", "livro de códigos", "robusto" (estatística), "alavancagem" (finanças), quando são o nome técnico em uso no campo. Jargão de gestão sem sentido técnico ("janela de oportunidade", "gargalo" fora de filas) é imagem e vai para G1, ou jargão e vai para G7.
- **Nominalização que nomeia conceito** ou retoma a frase anterior (G8).
- **Passiva e "-se" legítimos:** em métodos, com agente óbvio ou irrelevante, ou onde o gênero exige impessoalidade (G8).
- **Ressalva proporcional à evidência** (G5).
- **Repetição deliberada de termo:** em texto técnico, o mesmo conceito tem o mesmo nome (G3).
