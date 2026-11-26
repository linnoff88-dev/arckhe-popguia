ï»¿# popguia

<div align="center">
  <img src="capa/logo.svg" alt="Arckhé AI" height="48" />
  <p><strong>Arckhé AI</strong></p>
</div>


[![popguia](guia/assets/banner.jpg)](https://inematds.github.io/popguia/guia/)

**ê°Å¸â¡Â§ê°Å¸â¡Â· [PortuguêÂªs](README.md) êÂ· ê°Å¸â¡Âºê°Å¸â¡Â¸ [English](README.en.md) êÂ· ê°Å¸â¡Âªê°Å¸â¡Â¸ [EspaêÂ±ol](README.es.md)**

## O que êÂ©

O popguia êÂ© um projeto open source para criar popups que conversam com o visitante: em vez de pedir o e-mail logo de cara, ele faz duas ou trêÂªs perguntas, ensina algo êÂºtil e indica o produto, curso ou conteêÂºdo certo. Serve para quem tem um site (HTML, Next.js, Astro, WordPress) e usa um agente de cêÂ³digo como Claude Code, Codex ou Cursor: o agente instala, escreve as jornadas e acompanha os resultados. êâ° grêÂ¡tis, com licenêÂ§a MIT, sem mensalidade e sem servidor nosso. Hoje o repositêÂ³rio tem a pesquisa e o plano; o cêÂ³digo ainda vai ser escrito.

## ê°Å¸ââ Guia de uso

Guia completo (landing + passo a passo): **https://inematds.github.io/popguia/guia/**

**Popups e jornadas inteligentes que o agente de cêÂ³digo do dono do site instala e configura sozinho.**

O dono de um site (HTML, Next.js, WordPressê¢â¬Â¦) diz ao seu Claude Code / Codex / Cursor: *"instala o popguia e cria um quiz que recomende o curso certo"*. O agente instala o snippet, escreve as jornadas como arquivos JSON no repo, gera variantes, valida acessibilidade/LGPD/SEO e publica. Depois, o prêÂ³prio sistema mede com grupo de controle, roda A/B e evolui para bandit ê¢â¬â sem backend obrigatêÂ³rio nosso e sem cobranêÂ§a por pageview.

InspiraêÂ§êÂ£o: Alia Popups (jornadas interativas, zero-party, Prism AI). DiferenêÂ§a: open source (MIT), multi-plataforma, estado em arquivos, instalaêÂ§êÂ£o por agente, guard-rails por padrêÂ£o.

## O que entrega

- **Jornadas**: diagnêÂ³stico/quiz educativo, Learn & Earn, microcompromissos, newsletter em 2 etapas, recomendaêÂ§êÂ£o por catêÂ¡logo.
- **Smart triggering**: tempo, scroll, exit intent (desktop/mobile), inatividade, clique, adaptativo; caps de frequêÂªncia; cooldown global.
- **PersonalizaêÂ§êÂ£o por contexto**: pêÂ¡gina, UTM, dispositivo, novo/recorrente, respostas anteriores (zero-party no `localStorage`).
- **OtimizaêÂ§êÂ£o**: holdout permanente ê¢â â A/B (SRM, sequencial) ê¢â â Thompson por segmento ê¢â â contextual.
- **InstalaêÂ§êÂ£o pela IA**: `npx popguia init`, MCP local (`npx -y @popguia/mcp`), `SKILL.md`, `setup.md`, `llms.txt`, prompt copiêÂ¡vel.
- **GeraêÂ§êÂ£o por IA sem custo nosso**: o MCP devolve brief + schema; o agente do cliente escreve; provedor opcional configurado pelo cliente (Ollama incluêÂ­do).
- **Conformidade embutida**: `<dialog>` acessêÂ­vel, CLS 0, ê¢â°Â¤ 20 KB gz, modos de consentimento, sem dark patterns, sem roleta aleatêÂ³ria por padrêÂ£o.

## Estado

**Pesquisa e planejamento concluêÂ­dos em 10/10/2026. Nenhum cêÂ³digo de produto escrito.** PrêÂ³ximo passo: decisêÂµes do Nei (`PLANO.md êÂ§3`) e Fase 0.

## Documentos

| Arquivo | ConteêÂºdo |
|---|---|
| [docs/00-referencia-alia.md](docs/00-referencia-alia.md) | Insumo inicial trazido pelo Nei |
| [docs/01-pesquisa-mercado.md](docs/01-pesquisa-mercado.md) | Alia em profundidade (entidades, gatilhos, reexibiêÂ§êÂ£o, Prism) + 9 concorrentes (tabela) + reclamaêÂ§êÂµes |
| [docs/02-open-source-github.md](docs/02-open-source-github.md) | 37 repos com estrelas/licenêÂ§a/êÂºltimo push; veredito: construir do zero com referêÂªncias |
| [docs/03-instalacao-pela-ia.md](docs/03-instalacao-pela-ia.md) | Estado da arte (shadcn, Sentry, PostHog, Supabase, Stripe, Vercel, Clerkê¢â¬Â¦) e desenho CLI + MCP + skill + llms.txt |
| [docs/04-arquitetura.md](docs/04-arquitetura.md) | Componentes, diagrama mermaid, modelo de dados, stack, peso-alvo |
| [docs/05-algoritmos-e-metricas.md](docs/05-algoritmos-e-metricas.md) | Triggering, A/B com holdout, Thompson/LinUCB, volume mêÂ­nimo, mêÂ©tricas, guard-rails |
| [docs/06-conformidade.md](docs/06-conformidade.md) | LGPD/GDPR, WCAG 2.2, Google interstitials, CWV, dark patterns, roleta (Lei 5.768/71); checklist de 25 itens |
| [PLANO.md](PLANO.md) | Fases 0ê¢â¬â5 com critêÂ©rios `comando ê¢â â saêÂ­da`, sites de demonstraêÂ§êÂ£o, decisêÂµes fechadas e 7 em aberto |
| [CLAUDE.md](CLAUDE.md) | InstruêÂ§êÂµes do repo para agentes |

## DemonstraêÂ§êÂ£o

NêÂ£o hêÂ¡ piloto em site real: o popguia êÂ© para outras pessoas instalarem nos prêÂ³prios sites. A validaêÂ§êÂ£o usa 3 sites fictêÂ­cios em `exemplos/` (escola em HTML, loja em Next.js, blog em Astro), publicados no GitHub Pages. Detalhes em `PLANO.md êÂ§2`.

## LicenêÂ§a

MIT, grêÂ¡tis, sem SaaS: cada usuêÂ¡rio hospeda o prêÂ³prio coletor (ou usa o analytics que jêÂ¡ tem).

---

<div align="center">
  <img src="capa/logo.svg" alt="Arckhé AI" height="32" />
  <p><strong>Arckhé AI</strong></p>
</div>