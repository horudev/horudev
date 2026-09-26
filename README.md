# Horudev

Sito statico in italiano: Home, Progetti, Store, Contatti e Termini/privacy.

Per l'anteprima locale: `python -m http.server 4173 --directory dist`.

Nessuna dipendenza di compilazione. HTML, CSS e JavaScript; font serviti localmente.

Da completare prima del lancio pubblico:
- Inserire il link reale dello store Gumroad in `dist/app.js` (elemento store-link), aggiornando anche la nota sottostante.
- Contatti e newsletter preparano email tramite mailto, senza invio server o iscrizioni automatiche. Collegare un servizio dedicato se desiderato.
- Completare termini/privacy con i dati del titolare e dei servizi effettivamente adottati.
- Il mockup Toodo è un concept grafico, non uno screenshot del prodotto.

Tema e preferenza cookie sono salvati in localStorage. Non sono presenti analytics o cookie pubblicitari. Le animazioni rispettano prefers-reduced-motion.
