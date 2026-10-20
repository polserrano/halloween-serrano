# Bloc 1: Invocació del Repositori i Línia Base

## Acció 3.1 — Creació del repositori local

S'ha creat el directori `server-room-horror` i s'ha inicialitzat el repositori Git amb la branca principal `main`.

```bash
mkdir server-room-horror
cd server-room-horror
git init -b main
git status
```

**Evidència — Captura 3-1**

![Captura 3-1: inicialització del repositori](capturas/3-1.png)

## Acció 3.2 — Configuració de la identitat

S'ha configurat el nom i el correu de l'autor per identificar els commits.

```bash
git config --global user.name "Tu Nombre"
git config --global user.email "tu.correo@example.com"
git config --global --list
```

**Evidència — Captura 3-2**

![Captura 3-2: configuració de Git](capturas/3-2.png)

## Acció 3.3 — Primer commit

S'ha creat `main.js` amb el codi inicial del sistema de seguretat i s'ha registrat la primera versió.

```bash
git add main.js
git commit -m "feat: initialize building security system"
git log --oneline -1
```

**Evidència — Captura 3-3**

![Captura 3-3: primer commit](capturas/3-3.png)

## Acció 3.4 — Segon i tercer commit

S'ha activat l'alarma i, en una modificació posterior, s'ha establert el mode normal de seguretat. Cada canvi s'ha enregistrat en un commit separat.

```bash
git add main.js
git commit -m "feat: enable building security alarm"

git add main.js
git commit -m "feat: establish normal security mode"
git log --oneline -3
```

**Evidència — Captures 3-4a i 3-4**

![Captura 3-4a: segon commit](capturas/3-4a.png)

![Captura 3-4: tercer commit i historial](capturas/3-4.png)

## Acció 3.5 — Consulta de l'historial

S'ha consultat l'historial simplificat i s'ha comprovat que la línia base és estable i no conté canvis pendents.

```bash
git log --oneline
git status
```

**Evidència — Captura 3-5**

![Captura 3-5: historial inicial i estat del repositori](capturas/3-5.png)