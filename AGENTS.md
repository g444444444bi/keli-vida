# Keli Vida — instruções para agentes (fonte única; CLAUDE.md aponta para cá)

- Aplicativo: https://g444444444bi.github.io/keli-vida/ · Repositório: g444444444bi/keli-vida (branch `main`)
- Projeto independente: Firebase `keli-vida` (plano Spark, sem cobrança). Não usar nem alterar nenhum outro projeto/app.
- Código vai para o GitHub; dados pessoais vão só para o app/Firestore. Nunca gravar e-mail, senha, chaves privadas ou dados reais no código ou em commits.
- Armazenamento local próprio: `kv.*` (localStorage), `kelivida-files` e `kelivida-demos` (IndexedDB). Nunca reutilizar chaves de outros apps.
- Regras do Firestore: somente `users/{uid}/**` com `request.auth.uid == uid`.
- Identidade visual: azul-petróleo (ver DESIGN-SYSTEM.md). Mudanças de design só com pedido explícito.
- Fluxo: alterar `index.html` → testar → commit → push → conferir o endereço publicado.
