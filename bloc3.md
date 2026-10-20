# Bloc 3: Viatge Temporal, Exorcisme del Codi i Publicació Remota

## Acció 3.11 — Creació del commit infectat

S'ha introduït una excepció no controlada al fitxer principal per simular una modificació maliciosa i s'ha registrat amb el missatge indicat a l'enunciat.

```bash
git add main.js
git commit -m "feat: unhandled spectral exception"
```

**Captura de pantalla**

![Captura 3.11](capturas/3-11.png)

## Acció 3.12 — Inspecció de les diferències

S'ha comparat el commit infectat amb el seu pare immediat per identificar el canvi exacte que ha introduït l'error.

```bash
git diff HEAD~1 HEAD -- main.js
```

**Captura de pantalla**

![Captura 3.12](capturas/3-12.png)

## Acció 3.13 — Recuperació de l'estat segur

S'ha utilitzat `git reset --hard HEAD~1` per tornar al commit anterior i restaurar el contingut del directori de treball. Així, el commit infectat deixa de formar part de l'historial actual de `main`.

```bash
git reset --hard HEAD~1
git status
git log --oneline -5
git diff
```

**Captura de pantalla**

![Captura 3.13](capturas/3-13.png)

## Acció 3.14 — Inspecció gràfica de la topologia

S'ha visualitzat l'historial amb les branques i els commits de fusió per verificar la recuperació de la línia principal.

```bash
git log --oneline --graph --decorate --all
git branch -avv
```

**Captura de pantalla**

![Captura 3.14](capturas/3-14.png)

## Acció 3.15 — Publicació a GitHub

S'ha creat un repositori públic anomenat `halloween-git-rescue` i s'hi ha vinculat el repositori local. S'han publicat les branques i els fitxers Markdown per facilitar l'auditoria del projecte.

```bash
git remote add origin https://github.com/EL_TEU_USUARI/halloween-git-rescue.git
git remote -v
git push -u origin --all
```

**Captura de pantalla**

![Captura 3.15](capturas/3-15.png)

**Enllaç al repositori públic:** [halloween-git-rescue](https://github.com/EL_TEU_USUARI/halloween-git-rescue)