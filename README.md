# Sermões e Estudos Bíblicos — Skill para Claude Code

Skill para o [Claude Code](https://claude.ai/code) que ajuda a criar sermões e estudos bíblicos completos, organizados em pastas com estrutura padronizada.

## O que ela faz

- Conduz uma **entrevista interativa** para entender tema, texto bíblico, público e ocasião
- Usa **brainstorming** para explorar ângulos, ilustrações e direções antes de escrever
- Cria uma **estrutura de pastas organizada** com data e nome descritivo
- Gera o **conteúdo completo** em Markdown, pronto para converter em PDF ou apresentação

## Estrutura gerada

```
sermoes/
├── sermoes/
│   └── 2025-05-14-o-amor-de-deus/
│       ├── sermao.md          # Sermão completo
│       ├── links.md           # Links e referências
│       └── material-auxiliar/ # Imagens, PDFs, slides
└── estudos/
    └── 2025-05-14-fe-e-obras/
        ├── estudo.md          # Estudo bíblico com perguntas em 3 níveis
        ├── links.md
        └── material-auxiliar/
```

### Sermão (`sermao.md`)
Introdução · Pontos desenvolvidos com ilustrações · Aplicação prática · Conclusão e chamado · Versículos de apoio · Notas do pregador

### Estudo Bíblico (`estudo.md`)
Contexto histórico · Perguntas de observação · Perguntas de interpretação · Perguntas de aplicação · Sugestões para aprofundar · Notas do líder

## Como usar

No Claude Code, basta descrever o que você quer:

```
quero criar um sermão sobre graça para o culto de domingo, vou usar Efésios 2:8-9
```

```
me ajuda a preparar um estudo bíblico sobre fé e obras para minha célula de jovens
```

A skill faz as perguntas necessárias antes de gerar o conteúdo.

## Instalação

```bash
claude mcp install lucyannlenon/sermoes-biblicos
```

Ou copie o arquivo `SKILL.md` para a pasta de skills do seu Claude Code.
