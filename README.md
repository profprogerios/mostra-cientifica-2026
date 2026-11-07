# Mostra Científica 2026 — Data Driven

Aplicação interativa da Mostra Científica 2026, com três páginas independentes:

- [Participantes](participantes.html) — entrada de visitantes pelo celular;
- [Professor](professor.html) — painel de condução e controle das etapas;
- [Telão](telao.html) — apresentação coletiva e QR Code de entrada.

## Como ativar o site (GitHub Pages)

1. Na conta `profprogerios`, abra **Settings → Pages** deste repositório.
2. Em **Build and deployment → Source**, selecione **Deploy from a branch**.
3. Em **Branch**, escolha **main** e a pasta **/(root)**.
4. Clique em **Save**.
5. Aguarde o GitHub indicar **Your site is live** e teste os endereços abaixo.

A aplicação é HTML/CSS/JavaScript estático, portanto não precisa de um workflow personalizado GitHub Actions. O fluxo antigo foi removido após apresentar um erro de autorização ao tentar ativar o Pages automaticamente.

## Endereços (depois da ativação)

- Participantes: https://profprogerios.github.io/mostra-cientifica-2026/participantes.html
- Professor: https://profprogerios.github.io/mostra-cientifica-2026/professor.html
- Telão: https://profprogerios.github.io/mostra-cientifica-2026/telao.html

O QR Code exibido no telão aponta para **participantes.html** no endereço acima.

## Banco de dados e segurança

Os arquivos continuam configurados para o projeto Supabase existente, usando as tabelas `mc_*`.
A liberação dos controles do professor deve ser validada no Supabase.
Não coloque credenciais privadas do banco ou outros segredos no HTML público.

## Teste antes do evento

Verifique a entrada via QR Code em vários celulares, a sincronização com o painel do professor, a atualização do telão e os bloqueios das etapas. Um arquivo publicado não garante, isoladamente, que a rodada coletiva esteja funcional.
