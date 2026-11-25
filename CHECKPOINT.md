# Keli Vida — checkpoint (2026-11-25)

**Estado:** publicado e validado. https://g444444444bi.github.io/keli-vida/ (repo g444444444bi/keli-vida, branch `main`, Pages na raiz).

## Infraestrutura (independente de qualquer outro app)
- Firebase `keli-vida`, plano Spark. Firestore (modo produção) + Authentication e-mail/senha. Domínio autorizado: g444444444bi.github.io.
- Regras: só `users/{uid}/**` com `request.auth.uid == uid`; leitura/escrita sem login, ou fora de `users`, retorna 403 (testado por REST).
- Usuário da titular criado direto no console; o primeiro login é feito por ela. Nenhuma senha em código, arquivos ou relatórios.
- Sem Storage e sem backups agendados do Firestore (exigem Blaze, não contratado). Backup JSON do app funciona.

## Código
- App de página única (`index.html`). Sem seeds, sem dados pessoais, sem catálogo de demonstrações.
- Armazenamento local: `kv.*`, `kelivida-files`, `kelivida-demos`.
- Módulo Apartamento usa rótulos genéricos "Construtora" e "Financiamento"; os nomes são personalizáveis em Configurações › Perfil (`settings.lblB`, `settings.lblF`), aplicados ao texto visível por `applyLabels()`.
- Visual azul-petróleo (tokens `--roxo/--bl*` ≈ #0E7C86; ações #0A5A63).

## Validações feitas (ambiente isolado: localhost + backend falso, sem tocar na conta oficial)
- 12 módulos renderizam sem erro e iniciam zerados; cadastro de teste aparece; rótulos personalizados funcionam.
- Sincronização entre dois aparelhos simulados (push/pull/mesclagem) OK.
- Celular (375 px) sem rolagem horizontal; computador OK.
- Histórico do Git sem dados pessoais; autoria via e-mail noreply do GitHub.

## Pendências
- Primeiro login real e teste de sincronização feitos pela própria usuária.
