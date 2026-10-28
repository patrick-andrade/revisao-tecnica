# Validação

Linha de base de cada versão, para comparar depois de uma mudança na skill. Cada execução usa um agente novo, que recebe só o pedido do usuário e os arquivos da skill. Os relatórios não entram no repositório.

## 1.0.0 — 2026-10-28

| Cenário | Resultado |
|---|---|
| Sensibilidade (`sintetico.md`) | Os 27 itens plantados encontrados, em grupo ou em "Dados a pedir ao autor"; nenhuma armadilha marcada. Cerca de 21 itens e 15 dados a pedir. |
| Regressão (documento privado do autor) | 48 de 80 mudanças de estilo aprovadas foram encontradas, mais 4 parciais. Extras: 12 plausíveis, 6 troca de gosto, 0 piora. O que ficou de fora é, na maior parte, elevação de registro (mudar → alterar), que a skill deixa com o autor por decisão de projeto. |
| Aplicação (`.md` e `.docx`) | Itens aprovados aplicados com texto idêntico nos dois formatos; no `.docx`, estilos e numeração preservados; a nova busca saiu limpa. |

Calibragem (documentos de `cenarios.md`):

| Nº | Gênero | Itens | Por mil palavras | Dados a pedir |
|---|---|---|---|---|
| 01 | Relatório técnico | 32 | 11 | 11 |
| 02 | Comunicado institucional | 15 | 7 | 12 |
| 03 | Nota técnica (boxe) | 21 | 7 | 8 |
| 05 | Parecer (voto) | 16 | 8 | 0 |
| 07 | Artigo acadêmico | 41 | 22 | 9 |

O artigo 07 tem mais itens porque traz adjetivação promocional e impropriedades reais, conferidas por amostra. Os documentos 04 e 06 só foram testados antes das correções de calibragem.

**Não testado:** invocação em chat novo no Claude Code e no Codex (depende da instalação).
