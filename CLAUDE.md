# CLAUDE.md — KATYLENE

Site gerado pelo **SF (Site Factory)** em 15/04/2026.

## Contexto do Site

**Nome:** KATYLENE
**Nicho:** Moda e Beleza
**Keywords:** Tudo pela moda O amor pela moda e as passarelas fez com
**Paleta de cores:** slate | **Fonte:** outfit

Tudo pela moda. O amor pela moda e as passarelas fez com que eu, Katylene, criasse esse site...por muito tempo ele não foi movimentado, criei ele quanto tinha 17 anos. Agora mais velha venho trazendo conteúdo focado no mundo da moda. Além de outros amantes do mundo da moda. Conheça nosso blog. Quem somos? blogger-about-staff2 Henrique Hanriot Estilista Encontrei na profissão de estilista uma realização que acredito ser de outras vidas. Venho pelos posts desse blog compartilhar noticias das passarelas, dicas e entrevistas com modelos e muito mais relacionado ao mundo da alta moda. blogger-about-staff3 Katy Lene Designer de Moda Amante de moda, criei esse blog pra um dia promover meu trabalho. Até lá venho falando sobre tendências, looks inspirações e muitos outros assuntos relacionados .



## Componentes visuais usados

| Seção | Variante |
|-------|----------|
| Header | Header-A |
| Hero | Hero-H |
| Features | Features-I |
| About Section | About-A |
| Posts | Posts-C |
| Footer | Footer-H |
| Página Sobre | Sobre-E |
| Página Contato | Contato-G |

## Estrutura do projeto

```
src/
  sections/        # Layout escolhido pelo SF — Header, Hero, Features, About, Posts, Footer, Sobre, Contato
  data/            # JSONs com todo o conteúdo editável
  content/blog/    # Posts em Markdown
  pages/           # Rotas Astro (index, sobre, contato, blog, privacidade, termos)
  layouts/         # BaseLayout com fonte e cores dinâmicas
  styles/          # global.css com variáveis CSS de cor
public/
  images/          # hero.jpg, about.jpg, blog/*.jpg — inseridos automaticamente via Pexels
```

## O que editar

### Textos e conteúdo
- **`src/data/home.json`** — hero (título, subtítulo, botão), features (título, items), about section (título, desc, stats), posts
- **`src/data/sobre.json`** — conteúdo completo da página Sobre (hero, texto, missão)
- **`src/data/contato.json`** — título, subtítulo, email, tempo de resposta
- **`src/data/siteConfig.json`** — nome, slug, email, redes sociais, menu

### Imagens
Imagens já estão em `public/images/` (via Pexels). Para substituir, mantenha os mesmos nomes de arquivo:
- `hero.jpg` — imagem de fundo do Hero
- `about.jpg` — imagem da seção About (home)
- `sobre.jpg` — imagem de fundo da página Sobre
- `blog/{slug}.jpg` — imagens dos posts

### Posts do blog
Arquivos em `src/content/blog/`. Ajuste o tom de voz, adicione dados específicos do nicho e personalize conforme a identidade do site.

### Cores
Variáveis em `src/styles/global.css`: `--color-primary`, `--color-accent`, `--color-dark`.

## Deploy

```bash
bun install
bun run build
# Faça upload da pasta dist/ para Netlify, Vercel ou hosting estático
```
