# Horudev

Sito statico in italiano: Home, Progetti, Toodo, Store, Contatti e Termini/privacy.
Nessuna installazione o compilazione: HTML, CSS, JavaScript e font locali.

## Pubblicare su GitHub Pages

1. Crea un repository GitHub, per esempio `horudev`, con branch `main`.
2. Carica il contenuto di questa cartella nella radice del repository: `.github/`, `dist/` e questo README. Non caricare la cartella esterna `horudev` come ulteriore livello. Verifica che `.github/workflows/pages.yml` sia presente, anche se il sistema nasconde le cartelle con il punto.
3. In **Settings → Pages → Build and deployment → Source**, scegli **GitHub Actions**.
4. In **Actions → Publish Horudev to GitHub Pages**, seleziona **Run workflow** sul branch `main`. I successivi push su `main` aggiorneranno il sito automaticamente.
5. Il link sarà indicato in Settings → Pages e nell'esecuzione del workflow. Un repository di progetto usa normalmente `https://NOMEUTENTE.github.io/horudev/`.

Il workflow pubblica solo `dist/`; non include file di lavoro, `.git`, `.openai` o il logo originale di archivio. Non servono token personali o servizi Sites. Il repository deve poter utilizzare Pages con il piano GitHub scelto; un repository pubblico è l'opzione disponibile anche sul piano gratuito.

I collegamenti, i font e le immagini funzionano anche quando il sito è ospitato in una sottocartella. Ogni pagina ha il proprio `index.html`, quindi i link diretti e l'aggiornamento della pagina funzionano senza regole di riscrittura.

Documentazione ufficiale: https://docs.github.com/en/pages/getting-started-with-github-pages/using-custom-workflows-with-github-pages

## Anteprima locale

Dalla cartella del progetto:

```sh
python -m http.server 4173 --directory dist
```

Apri `http://localhost:4173`. Puoi anche aprire `dist/index.html` direttamente nel browser.

## Contenuti e limiti attuali

- Store collegato direttamente a https://horudev.gumroad.com.
- Contatti, newsletter e richiesta Closed Alpha preparano email; il visitatore completa l'invio dal proprio programma di posta. Nessuna iscrizione o ammissione automatica.
- Completare termini/privacy con i dati del titolare e dei servizi effettivamente adottati prima del lancio pubblico.
- Il mockup Toodo è un concept grafico, non uno screenshot del prodotto.
- Tema e preferenza cookie sono salvati in localStorage. Nessun analytics o cookie pubblicitario.
- Il logo originale viene visualizzato con un filtro che rende trasparente il fondo scuro senza ridisegnarlo. Le animazioni rispettano prefers-reduced-motion.

Per aggiungere una pagina, usa i percorsi relativi del documento e indica la sua chiave nell'attributo `data-page` di `<html>`; registra il relativo contenuto nella mappa `pages` in `dist/app.js`.
