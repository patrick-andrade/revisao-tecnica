# Manutenção de revisao-tecnica

Este repositório contém uma skill de revisão de redação técnica e acadêmica em português.

- O pacote instalável está em `skills/revisao-tecnica/`. Documentação de manutenção e testes ficam fora dele.
- Mantenha os passos e o teste de parada em `SKILL.md`, os tipos de fragilidade em `references/catalogo.md` e as convenções por gênero em `references/generos.md`. As formas típicas de cada tipo existem só no catálogo.
- Os códigos G1 a G13 são estáveis: tipo novo entra no fim ou em versão maior, com nota no `CHANGELOG.md`. Cada tipo tem O que é, Teste, Formas típicas, exemplos e Não agir quando.
- Exemplo novo entra marcado *ilustrativo*; a marca sai quando o exemplo for aprovado numa revisão real.
- Preserve a invocação explícita (`disable-model-invocation: true` e `allow_implicit_invocation: false`) e o gate de aprovação antes de aplicar.
- A skill traz regras e padrões, sem scripts: a busca textual fica com o agente que a executa.
- **Anonimato:** exemplos, testes e documentação não podem identificar documentos, clientes ou projetos de origem. Adapte o domínio, os nomes, os valores e as datas de todo exemplo tirado de revisão real. Antes de cada commit, releia os exemplos novos e busque no repositório os nomes do documento de origem (instituição, projeto, lugares, valores); a busca deve voltar vazia.
- Textos de teste baixados ficam em `tests/corpus/`, ignorado pelo Git; baixe-os de novo pelos links de `tests/cenarios.md` quando for testar. No repositório entram só link, licença e localizador.
- Valide mudanças conforme `tests/cenarios.md` e registre a nova linha de base em `tests/validacao.md`, com uma seção por versão.
- Antes de publicar, confira arquivos versionados, licença, versão no frontmatter e no `CHANGELOG.md`, e estado remoto. Nunca altere identidade Git global.
