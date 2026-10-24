# 🎃 Halloween Git Rescue — Sistema de Seguretat i Auditoria Git

Repositori corresponent a la pràctica de recuperació, gestió de branques, resolució de conflictes i viatges temporals en Git.

---

## 📁 Estructura del Projecte

A continuació es detalla la documentació completa dividida per blocs de treball i la carpeta de captures d'evidència:

*   📂 **[Carpeta de Captures](capturas/)**: Col·lecció amb totes les imatges d'evidència de les comandes executades.
*   📄 **[Bloc 1: Invocació del Repositori i Línia Base](bloc1.md)**: Inicialització, configuració i desenvolupament inicial a `main`.
*   📄 **[Bloc 2: Les Branques del Més Enllà i Resolució del Conflicte](bloc2.md)**: Creació de branques, desenvolupament paral·lel i resolució manual de conflictes de fusió.
*   📄 **[Bloc 3: Viatge Temporal, Exorcisme del Codi i Publicació Remota](bloc3.md)**: Injecció i inspecció d'errors, reculada en el temps amb `git reset --hard` i publicació final a GitHub.

---

## 🛠️ Resum Tecnològic i Comandes Clau

1. **Línia base:** `git init -b main`, `git add`, `git commit`, `git status`, `git log`.
2. **Treball amb branques:** `git branch`, `git switch`, `git merge --no-ff`.
3. **Resolució de conflictes:** `git diff --check`, neteja de marques de conflicte (`<<<<<<<`, `=======`, `>>>>>>>`).
4. **Viatge temporal i neteja:** `git diff HEAD~1 HEAD`, `git reset --hard HEAD~1`.
5. **Sincronització remota:** `git remote add origin`, `git push -u origin --all`.

---

👤 **Autor:** Pol Serrano  
🔗 **Repositori Públic:** [https://github.com/polserrano/halloween-serrano](https://github.com/polserrano/halloween-serrano)