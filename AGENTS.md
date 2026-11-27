# AGENTS.md — Tobeer Fraternity House (sito)

Istruzioni per gli agenti (Claude, Codex). `CLAUDE.md` importa questo file.

## Cos'è
Sito statico di https://tobeerfraternityhouse.it, in `sito/`. Pagine: `index.html` (home), `food.html` (menù cucina), `drinks.html` (menù bevande), `sanremo-delivery/` (delivery). Stili in `sito/css/`, font in `sito/font/`, immagini in `sito/immagini/`. Nessun build, nessuna dipendenza.

## Anteprima
Aprire `sito/index.html` nel browser, oppure da `sito/`: `python3 -m http.server 8000` e andare su http://localhost:8000. Controllare desktop e mobile.

## Attenzione: il merge pubblica il sito
`.github/workflows/deploy.yml` carica via FTP i file cambiati in `sito/` a ogni push su `main`. Quindi **unire una PR su `main` significa andare online**. Per questo:
- le modifiche passano sempre da un ramo e da una pull request;
- la PR la unisce solo Francesco, dopo aver visto l'anteprima.

## Regole
- Il repository è **pubblico**: nessun segreto, password, token o dato personale. La password FTP sta nei Secrets di GitHub (`FTP_PASSWORD`), mai nel codice.
- Non modificare `.github/workflows/deploy.yml` senza motivo e senza dirlo nella PR.
- Immagini e GIF leggere: il sito è stato appena alleggerito per tablet e desktop, non reintrodurre file pesanti.

## Collaborazione Claude + Codex
- Un ramo per compito: `claude/<tema>` o `codex/<tema>`. Mai commit diretti su `main`.
- Commit piccoli, messaggi in italiano, imperativo breve.
