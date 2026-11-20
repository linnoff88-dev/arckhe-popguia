# popguia

<div align="center">
  <img src="capa/logo.svg" alt="Arckhé AI" height="48" />
  <p><strong>Arckhé AI</strong></p>
</div>


[![popguia](guia/assets/banner.jpg)](https://inematds.github.io/popguia/guia/)

**ðŸ‡§ðŸ‡· [PortuguÃªs](README.md) Â· ðŸ‡ºðŸ‡¸ [English](README.en.md) Â· ðŸ‡ªðŸ‡¸ [EspaÃ±ol](README.es.md)**

## O que Ã©

O popguia Ã© um projeto open source para criar popups que conversam com o visitante: em vez de pedir o e-mail logo de cara, ele faz duas ou trÃªs perguntas, ensina algo Ãºtil e indica o produto, curso ou conteÃºdo certo. Serve para quem tem um site (HTML, Next.js, Astro, WordPress) e usa um agente de cÃ³digo como Claude Code, Codex ou Cursor: o agente instala, escreve as jornadas e acompanha os resultados. Ã‰ grÃ¡tis, com licenÃ§a MIT, sem mensalidade e sem servidor nosso. Hoje o repositÃ³rio tem a pesquisa e o plano; o cÃ³digo ainda vai ser escrito.

## ðŸ“– Guia de uso

Guia completo (landing + passo a passo): **https://inematds.github.io/popguia/guia/**

**Popups e jornadas inteligentes que o agente de cÃ³digo do dono do site instala e configura sozinho.**

O dono de um site (HTML, Next.js, WordPressâ€¦) diz ao seu Claude Code / Codex / Cursor: *"instala o popguia e cria um quiz que recomende o curso certo"*. O agente instala o snippet, escreve as jornadas como arquivos JSON no repo, gera variantes, valida acessibilidade/LGPD/SEO e publica. Depois, o prÃ³prio sistema mede com grupo de controle, roda A/B e evolui para bandit â€” sem backend obrigatÃ³rio nosso e sem cobranÃ§a por pageview.

InspiraÃ§Ã£o: Alia Popups (jornadas interativas, zero-party, Prism AI). DiferenÃ§a: open source (MIT), multi-plataforma, estado em arquivos, instalaÃ§Ã£o por agente, guard-rails por padrÃ£o.

## O que entrega

- **Jornadas**: diagnÃ³stico/quiz educativo, Learn & Earn, microcompromissos, newsletter em 2 etapas, recomendaÃ§Ã£o por catÃ¡logo.
- **Smart triggering**: tempo, scroll, exit intent (desktop/mobile), inatividade, clique, adaptativo; caps de frequÃªncia; cooldown global.
- **PersonalizaÃ§Ã£o por contexto**: pÃ¡gina, UTM, dispositivo, novo/recorrente, respostas anteriores (zero-party no `localStorage`).
- **OtimizaÃ§Ã£o**: holdout permanente â†’ A/B (SRM, sequencial) â†’ Thompson por segmento â†’ contextual.
- **InstalaÃ§Ã£o pela IA**: `npx popguia init`, MCP local (`npx -y @popguia/mcp`), `SKILL.md`, `setup.md`, `llms.txt`, prompt copiÃ¡vel.
- **GeraÃ§Ã£o por IA sem custo nosso**: o MCP devolve brief + schema; o agente do cliente escreve; provedor opcional configurado pelo cliente (Ollama incluÃ­do).
- **Conformidade embutida**: `<dialog>` acessÃ­vel, CLS 0, â‰¤ 20 KB gz, modos de consentimento, sem dark patterns, sem roleta aleatÃ³ria por padrÃ£o.

## Estado

**Pesquisa e planejamento concluÃ­dos em 10/10/2026. Nenhum cÃ³digo de produto escrito.** PrÃ³ximo passo: decisÃµes do Nei (`PLANO.md Â§3`) e Fase 0.

## Documentos

| Arquivo | ConteÃºdo |
|---|---|
| [docs/00-referencia-alia.md](docs/00-referencia-alia.md) | Insumo inicial trazido pelo Nei |
| [docs/01-pesquisa-mercado.md](docs/01-pesquisa-mercado.md) | Alia em profundidade (entidades, gatilhos, reexibiÃ§Ã£o, Prism) + 9 concorrentes (tabela) + reclamaÃ§Ãµes |
| [docs/02-open-source-github.md](docs/02-open-source-github.md) | 37 repos com estrelas/licenÃ§a/Ãºltimo push; veredito: construir do zero com referÃªncias |
| [docs/03-instalacao-pela-ia.md](docs/03-instalacao-pela-ia.md) | Estado da arte (shadcn, Sentry, PostHog, Supabase, Stripe, Vercel, Clerkâ€¦) e desenho CLI + MCP + skill + llms.txt |
| [docs/04-arquitetura.md](docs/04-arquitetura.md) | Componentes, diagrama mermaid, modelo de dados, stack, peso-alvo |
| [docs/05-algoritmos-e-metricas.md](docs/05-algoritmos-e-metricas.md) | Triggering, A/B com holdout, Thompson/LinUCB, volume mÃ­nimo, mÃ©tricas, guard-rails |
| [docs/06-conformidade.md](docs/06-conformidade.md) | LGPD/GDPR, WCAG 2.2, Google interstitials, CWV, dark patterns, roleta (Lei 5.768/71); checklist de 25 itens |
| [PLANO.md](PLANO.md) | Fases 0â€“5 com critÃ©rios `comando â†’ saÃ­da`, sites de demonstraÃ§Ã£o, decisÃµes fechadas e 7 em aberto |
| [CLAUDE.md](CLAUDE.md) | InstruÃ§Ãµes do repo para agentes |

## DemonstraÃ§Ã£o

NÃ£o hÃ¡ piloto em site real: o popguia Ã© para outras pessoas instalarem nos prÃ³prios sites. A validaÃ§Ã£o usa 3 sites fictÃ­cios em `exemplos/` (escola em HTML, loja em Next.js, blog em Astro), publicados no GitHub Pages. Detalhes em `PLANO.md Â§2`.

## LicenÃ§a

MIT, grÃ¡tis, sem SaaS: cada usuÃ¡rio hospeda o prÃ³prio coletor (ou usa o analytics que jÃ¡ tem).

---

<div align="center">
  <img src="capa/logo.svg" alt="Arckhé AI" height="32" />
  <p><strong>Arckhé AI</strong></p>
</div>