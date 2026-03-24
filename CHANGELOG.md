# Changelog — AdminHub

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
