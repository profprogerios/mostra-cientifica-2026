# Mostra Científica 2026 — Data Driven

Experiência interativa coletiva de letramento em dados, com três interfaces:

- [Participantes](participantes.html) — acesso do público via celular;
- [Professor](professor.html) — condução das etapas mediante autenticação;
- [Telão](telao.html) — projeção e QR Code de entrada.

## Publicação

O fluxo GitHub Actions em `.github/workflows/publicar-pages.yml` publica a branch `main` no GitHub Pages.
Se a publicação não iniciar, abra **Settings > Pages** e configure **Source: GitHub Actions**.

Endereço público previsto:
https://profprogerios.github.io/mostra-cientifica-2026/participantes.html

O QR Code do telão detecta automaticamente esse endereço quando o telão é acessado pelo GitHub Pages.

## Banco

As três interfaces preservam a configuração do Supabase `missao9-data-driven-v2`.
Chave `publishable` é pública; **nunca** adicione `service_role` ou segredo do banco ao HTML.
O professor deve utilizar o PIN de controle existente, validado por política do banco.

## Uso

1. Abrir `professor.html` no computador do responsável.
2. Projetar `telao.html` e orientar o acesso dos participantes pelo QR Code.
3. Testar uma rodada completa em múltiplos aparelhos antes do evento.

Se o QR mostrar mensagem de configuração, confira se o telão foi aberto pelo endereço HTTPS publicado, e não pelo arquivo local.
