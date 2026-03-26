# Changelog — AdminHub

## [v01.04.02] — 2026-03-26
### Removido
- **`_headers`**: arquivo removido — admins não precisam de CSP nem controles de cache (Cloudflare Access protege o app). Cache gerenciado nativamente pelo Cloudflare.

## [v01.04.01] — 2026-03-24
### Alterado
- `public/_headers` atualizado para política CSP estável em runtime (`script-src` com `'unsafe-inline'`), eliminando dependência de hash inline volátil.
- Workflow de deploy ajustado para compatibilidade com Wrangler 4.77+ (`pages deploy` sem flags legadas `--functions` e `--config`).

### Corrigido
- Falha de deploy no GitHub Actions causada por flags removidas no Wrangler 4.77+.
- Bloqueio de script inline por CSP após deploy.

## [v01.04.00] — 2026-03-24
### Alterado
- Arquitetura de leitura migrada para API local `GET /api/config` via Cloudflare Pages Functions.
- Leitura agora usa binding D1 nativo (`BIGDATA_DB`) direto na `bigdata_db`, sem chamada a `admin.lcv.app.br`.
- `public/app.js` atualizado para consumir endpoint local (`/api/config`) com fallback para `cards.json`.
- Deploy atualizado para publicar `functions/` com `wrangler.json` e binding D1.
- CSP ajustada para reduzir ruído de inline script no navegador.

## [v01.03.00] — 2026-03-24
### Alterado
- Migração de configurações para bigdata_db centralizado
- Cards agora carregam do endpoint `/api/adminhub/config` em admin-app com fallback para local
- Adicionadas funções `loadCardsFromApi()` e `loadCardsFromLocal()` com strategy de retry

## [v01.02.00] — 2026-03-22
### Alterado
- Inclusão do card **Itaú Calculadora Admin** apontando para `https://admin-itau.lcv.app.br`

## [v01.01.00] — 2026-03-22
### Alterado
- Padronização do sistema de versão para formato APP v00.00.00
- Cabeçalho de código adicionado (app.js)
- Rodapé simplificado — versão via variável APP_VERSION

## [v01.00.00] — Anterior
### Histórico
- Catálogo administrativo de apps com acesso restrito
