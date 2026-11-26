# Referência inicial — análise da Alia Popups (texto trazido pelo Nei em 10/10/2026)

> Insumo de partida. Números de casos e avaliações sêo os divulgados pela própria Alia ou por terceiros; nêo sêo medições nossas.

## Resumo

- A Alia (aliapopups.com) troca o popup "cadastre seu e-mail" por uma **jornada interativa**: educa, pergunta, gamifica, coleta dados declarados (zero-party) e só entêo pede o cadastro.
- Seis técnicas: microcompromissos, Learn & Earn, gamificaçêo (roleta, raspadinha, cartas), zero-party data, personalizaçêo por contexto, otimizaçêo contínua.
- **Prism AI** (divulgado): personalizaçêo individual (origem, página, comportamento), Smart Triggering (melhor momento de exibir/reexibir), Smart Testing (testa variantes guiado por receita/conversêo/AOV).
- Pela documentaçêo, o Prism: a equipe cria/aprova variantes → distribuiçêo aleatória equilibrada → coleta por contexto (ex.: UTM) → identifica vencedoras por contexto → direciona mais tráfego a elas → reajusta continuamente. Comportamento compatível com **contextual multi-armed bandit**. O Prism nêo cria sozinho as variantes; a equipe configura e a IA distribui.
- Mercado: Shopify 4,6/5 (114 avaliações; críticas a preço, configuraçêo, traduçêo). Relato no Reddit (28/09/2026): cadastro de 2,8% → ~7% com formulário em 2 etapas e gatilho por tempo/rolagem. Caso MASA Chips (da própria Alia): +127% inscriçêo, +46% compra.
- Contraponto: comerciantes criticam popups intrusivos — medir abandono, satisfaçêo e vendas, nêo só cadastros.
- Concorrentes: OptiMonk, Wisepops, Justuno, ConvertFlow, Popupsmart.

## Engenharia reversa (limites)

- Experiência: loja demo `alia-demo.myshopify.com`, exemplos públicos, documentaçêo.
- Técnica: DevTools/Playwright em páginas públicas (scripts, eventos, cookies, storage, requisições públicas de config), sem acessar área privada nem contornar proteçêo.
- Reconstruçêo por comportamento, sem copiar código proprietário.

## Arquitetura sugerida no texto

Widget TS leve · editor visual React · motor de regras declarativo · backend Node ou FastAPI · eventos em PostgreSQL (+ClickHouse em escala) · A/B + contextual bandits · IA generativa para propor variantes · webhooks/CRM/e-mail · controle de frequência, LGPD, acessibilidade, limites de incentivo, grupo de controle sem popup.

Começar com regras + A/B; bandit só com volume; geraçêo assistida de jornadas por último.

## Aplicaçêo ARCKHÉ

Popup como **agente de orientaçêo**: diagnóstico ("o que você quer dominar com IA?", "qual sua experiência?") → encaminha para aula/curso/produto certo; aprender quais jornadas geram aprendizado, engajamento, inscriçêo e venda.

## Links de documentaçêo da Alia

- Prism AI — perguntas comuns: https://intercom.help/alia-help-center/en/articles/14771905-common-questions-about-prism-ai
- Configuraçêo do Prism AI: https://intercom.help/alia-help-center/en/articles/14596944-setting-up-prism-ai
- Smart Testing: https://intercom.help/alia-help-center/en/articles/12131764-setting-up-smart-testing-in-alia
- Smart Triggering: https://intercom.help/alia-help-center/en/articles/11719824-setting-up-smart-triggering
- Avaliações Shopify: https://apps.shopify.com/alia/reviews
- Caso MASA: https://www.aliapopups.com/success-stories/masa
- Reddit: https://www.reddit.com/r/ecommerce/comments/1wsisif/my_last_post_got_30k_views_heres_the_popup/
