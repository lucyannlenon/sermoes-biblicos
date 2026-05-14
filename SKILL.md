---
name: sermoes-biblicos
description: Cria sermões e estudos bíblicos completos em português, organizados em pastas com nome descritivo e data, com texto-chave, material auxiliar e arquivo de links. Use esta skill sempre que o usuário quiser criar um sermão, estudo bíblico, devocional, pregação, ou qualquer material de ensino cristão — mesmo que ele não use exatamente essas palavras (ex: "quero preparar algo sobre Gênesis", "me ajuda com minha mensagem de domingo", "vou liderar um estudo sobre fé").
---

# Skill: Sermões e Estudos Bíblicos

Ajuda a criar sermões e estudos bíblicos completos, organizados em pastas no sistema de arquivos.

## Pasta base

```
/home/lucyannl/Documents/sermoes/
├── sermoes/
│   └── YYYY-MM-DD-nome-descritivo/
│       ├── sermao.md
│       ├── links.md
│       └── material-auxiliar/
└── estudos/
    └── YYYY-MM-DD-nome-descritivo/
        ├── estudo.md
        ├── links.md
        └── material-auxiliar/
```

## Passo 1 — Entrevista interativa

Faça as perguntas abaixo **uma de cada vez**, esperando a resposta antes de continuar. Não faça todas de uma só vez.

1. **Tipo**: É um sermão ou um estudo bíblico?
2. **Tema**: Qual é o tema ou assunto central?
3. **Texto-chave**: Qual passagem bíblica será usada? (se o usuário não souber, sugira 2-3 opções relacionadas ao tema)
4. **Ocasião / público**: Para quem é? (culto de domingo, célula, jovens, retiro, etc.)
5. **Pontos principais**: Quantos pontos quer desenvolver? (para sermões — padrão: 3)
6. **Links e referências**: Tem algum link de artigo, vídeo ou livro que quer salvar já? (pode deixar em branco)

## Passo 2 — Brainstorming

Antes de escrever o conteúdo, **use a skill de brainstorming** para explorar o tema com o usuário:

- Explore o contexto histórico e teológico do texto
- Sugira ângulos de abordagem (ex: promessa, desafio, narrativa, didático)
- Proponha ilustrações ou exemplos práticos relevantes para o público
- Apresente 2-3 direções possíveis para o desenvolvimento e deixe o usuário escolher

Só avance para a escrita após o usuário aprovar a direção.

## Passo 3 — Gerar o nome da pasta

Monte o nome da pasta assim:
```
YYYY-MM-DD-tema-em-kebab-case
```
Exemplo: `2025-05-14-o-amor-incondicional-de-deus`

Use a data de hoje. O nome deve ser descritivo e em português, sem acentos, tudo minúsculo.

## Passo 4 — Criar a estrutura de arquivos

Crie as pastas e arquivos:
```bash
mkdir -p /home/lucyannl/Documents/sermoes/<tipo>/<pasta>/material-auxiliar
```

Crie `links.md` vazio (ou com os links fornecidos):

```markdown
# Links e Referências

## Artigos e Leituras
- 

## Vídeos e Pregações
- 

## Livros
- 
```

## Passo 5 — Escrever o conteúdo

### Para Sermões (`sermao.md`)

```markdown
# [Título do Sermão]

**Texto-chave:** [Referência] — "[Versículo completo]"
**Ocasião:** [público / evento]
**Data:** YYYY-MM-DD

---

## Introdução

[Abertura que conecta com a vida do ouvinte — uma história, pergunta ou situação]

---

## Ponto 1 — [Título]

[Desenvolvimento com base no texto]

**Ilustração:** [exemplo prático ou história]

---

## Ponto 2 — [Título]

[Desenvolvimento]

**Ilustração:**

---

## Ponto 3 — [Título]

[Desenvolvimento]

**Ilustração:**

---

## Aplicação Prática

[Como o ouvinte pode viver isso na semana? Seja específico e concreto.]

---

## Conclusão e Chamado

[Retome o tema central, convide para uma resposta ou decisão]

---

## Versículos de Apoio

- 
- 
- 

## Notas do Pregador

[Espaço para observações pessoais, timing, etc.]
```

### Para Estudos Bíblicos (`estudo.md`)

```markdown
# [Título do Estudo]

**Texto-chave:** [Referência] — "[Versículo completo]"
**Ocasião:** [grupo / evento]
**Data:** YYYY-MM-DD

---

## Contexto Histórico e Literário

[Quem escreveu? Para quem? Qual a situação? O que vem antes e depois?]

---

## Leitura do Texto

[Passagem completa ou indicação para leitura em voz alta]

---

## Perguntas de Observação — O que o texto diz?

1. 
2. 
3. 

---

## Perguntas de Interpretação — O que o texto significa?

1. 
2. 
3. 

---

## Perguntas de Aplicação — Como vivo isso?

1. 
2. 
3. 

---

## Para Aprofundar

[Sugestões de leitura complementar, passagens paralelas, etc.]

---

## Notas do Líder

[Dicas de condução, pontos de atenção, tempo sugerido por seção]
```

## Passo 6 — Confirmar e informar

Após criar tudo, informe:
- O caminho completo da pasta criada
- Os arquivos gerados
- Que a pasta `material-auxiliar/` está pronta para receber imagens, PDFs, apresentações, etc.
- Que `links.md` pode ser atualizado a qualquer momento

---

## Comportamento esperado

- Sempre escrever em português do Brasil
- Manter linguagem acessível mas rica teologicamente
- Não inventar citações bíblicas — usar apenas versículos reais
- Se o usuário fornecer um texto bíblico, citar a versão que ele preferir (padrão: NVI)
- O conteúdo deve ser substancial, não genérico — use os detalhes do tema e público fornecidos
