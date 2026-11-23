# Tobeer Fraternity House — sito

Sito statico di https://tobeerfraternityhouse.it (hosting SiteGround).

## Come si aggiorna
1. Si modificano i file dentro `sito/`.
2. Si fa commit e push su `main`.
3. La GitHub Action "Pubblica su SiteGround" carica via FTP solo i file cambiati (1–2 minuti).

Niente più FileZilla. La password FTP è salvata nei Secrets del repository (`FTP_PASSWORD`).

## Anteprima in locale
Apri `sito/index.html` nel browser, oppure dalla cartella `sito/`: `python3 -m http.server 8000` e vai su http://localhost:8000

## Pagine
- `index.html` — home
- `food.html` — menù cucina
- `drinks.html` — menù bevande
- `sanremo-delivery/` — pagina delivery
