# MySports-data

Dati pubblicati dell'app MySports: file JSON statici sul branch `gh-pages`, serviti da GitHub Pages su
`https://kingdany.github.io/MySports-data/` (`meta.json`, `{competizione}/{stagione}.json`).

Il branch `main` contiene solo il workflow "Aggiorna dati" (`.github/workflows/update-data.yml`): scarica il codice dal
repository privato `MySports`, esegue l'importatore e pubblica qui. Gira in questo repository, pubblico, perché i minuti
di GitHub Actions sono illimitati. Lo avvia cron-job.org (istruzioni nel README di `MySports`); da qui si lancia anche a
mano: **Actions → Aggiorna dati → Run workflow**, con le opzioni per le stagioni passate e il recupero dei video.

Secret necessari: `MYSPORTS_DEPLOY_KEY` (chiave privata della deploy key di sola lettura di `MySports`),
`YOUTUBE_API_KEY`, `FOOTBALL_DATA_API_KEY`.
