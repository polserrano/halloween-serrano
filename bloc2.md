# Bloc 2: Les Branques del Més Enllà i Resolució del Conflicte

## Acció 3.6 — Creació de les branques

S'han creat dues branques a partir de la línia base de `main`. Aquesta topologia permet desenvolupar solucions independents i provocar un conflicte controlat durant la fusió.

```bash
git switch main
git branch feature-nightmare
git branch feature-sanctuary
git branch
```

**Evidència — Captura 3-6**

![Captura 3-6: branques del repositori](capturas/3-6.png)

## Acció 3.7 — Desenvolupament de la branca nightmare

S'ha modificat el mode de seguretat a `NIGHTMARE` i s'ha registrat el canvi en un commit independent.

```bash
git switch feature-nightmare
git add main.js
git commit -m "feat: inject nightmare security mode"
git log --oneline -2
```

**Evidència — Captura 3-7**

![Captura 3-7: commit nightmare](capturas/3-7.png)

## Acció 3.8 — Desenvolupament de la branca sanctuary

S'ha modificat la mateixa línia de codi per establir el mode `SANCTUARY`, mantenint la independència entre les dues branques.

```bash
git switch feature-sanctuary
git add main.js
git commit -m "feat: implement sanctuary security mode"
git log --oneline -2
```

**Evidència — Captura 3-8**

![Captura 3-8: commit sanctuary](capturas/3-8.png)

## Acció 3.9 — Integració de les branques

La branca `feature-nightmare` s'ha integrat primer a `main`. En intentar integrar `feature-sanctuary`, Git ha detectat canvis incompatibles a la mateixa línia.

```bash
git switch main
git merge --no-ff feature-nightmare -m "merge: integrate nightmare timeline"
git merge --no-ff feature-sanctuary
git status
```

**Evidència — Captura 3-9**

![Captura 3-9: conflicte de fusió](capturas/3-9.png)

## Acció 3.10 — Resolució manual del conflicte

S'han eliminat les marques de conflicte i s'ha seleccionat manualment el mode de protecció `SANCTUARY`, juntament amb una variable de contenció de l'amenaça. Finalment, s'ha enregistrat la fusió.

```bash
git diff
git diff --check
git status
git add main.js
git commit -m "merge: resolve nightmare and sanctuary conflict"
git log --oneline --graph --decorate --all
```

**Evidència — Captura 3-10a**

![Captura 3-10a: inspecció del conflicte](capturas/3-10a.png)

**Evidència — Captura 3-10**

![Captura 3-10: fusió completada i historial gràfic](capturas/3-10.png)