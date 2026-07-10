# Drivr — Quiz Patente B

Web app per esercitarsi ai quiz della patente B in stile "Tinder": **freccia destra = VERO**, **freccia sinistra = FALSO** (funziona con tastiera, mouse e swipe da telefono).

Interfaccia "liquid glass", tab bar in basso, tema chiaro/scuro, grafici (Apache ECharts), icone (Eva Icons), sezione Capitoli per argomento ministeriale.

## Funzioni
- Schede a swipe (destra = VERO / sinistra = FALSO) con animazione; su **mobile** il menu è una **tab bar** in basso
- Spiegazione ad ogni errore, con etichetta della fonte (📘 ministeriale / 🤖 AI)
- Sezione **Progressi** con due tab: **Stats** (storico test cronologico) e **Sbagliate**
- Blocchi da **30 domande**, esito **≤3 errori = Promosso**
- Dati salvati in locale nel browser (nessun server)
- **Impostazioni**: attiva/disattiva le domande precaricate, attiva/disattiva le domande AI, importa altri JSON (che si **aggiungono** ai precedenti), **Danger zone** per azzerare i risultati
- Pacchetto **Novità 2026 (AI)**: angoli ciechi, ADAS, monopattini, smartphone, neopatentati (non ufficiale, solo ripasso)

## Domande incluse
- **101 domande ministeriali** di prova (solo testo) già dentro l'app — usate come fallback offline
- **28 domande "Novità 2026"** scritte da me con l'AI (chiaramente etichettate, non ufficiali)
- **Archivio completo (~7.139 domande, con immagini): si carica DA SOLO al primo avvio**
  scaricandolo da GitHub e mettendolo in cache (funziona poi anche offline). Nessun import manuale.

### Come vuole caricare le domande (in ordine di priorità)
1. Se in localStorage c'è già un archivio salvato → usa quello (istantaneo, offline).
2. Se nella cartella del sito c'è un file **`domande.json`** → usa quello (utile per una copia 100% offline: scarica
   [quizPatenteB2023.json](https://raw.githubusercontent.com/Ed0ardo/QuizPatenteB/master/quizPatenteB2023.json)
   e rinominalo `domande.json` nella cartella).
3. Altrimenti scarica l'archivio completo da **GitHub raw** al primo avvio.
4. Se sei offline / apri il file da disco con doppio clic → resta sul set di prova (101 + 28).

> Nota: il caricamento automatico da GitHub funziona quando l'app è servita via **http/https** (es. GitHub Pages).
> Aprendo `index.html` con un doppio clic (protocollo `file://`) il browser blocca il fetch: in quel caso usa
> l'import manuale o il file `domande.json`.

## Pubblicare su GitHub Pages
1. Crea un repository su GitHub (es. `quiz-patente-b`).
2. Carica **tutti i file di questa cartella** nella radice del repo (`index.html`, `README.md`, `.nojekyll`).
3. Vai su **Settings → Pages**.
4. In *Source* scegli il branch `main` e cartella `/ (root)`, poi **Save**.
5. Dopo qualche minuto l'app sarà online su `https://<tuo-utente>.github.io/quiz-patente-b/`.

Il file `.nojekyll` serve a dire a GitHub Pages di pubblicare i file così come sono.

## Note
Le domande "Novità 2026" sono una rielaborazione fedele del nuovo Codice della Strada (in vigore dal 14/12/2024) fatta con l'AI: utili per ripassare i temi nuovi, ma **non** sono estratti certificati dell'archivio ministeriale. Fonte del dataset ministeriale: [Ed0ardo/QuizPatenteB](https://github.com/Ed0ardo/QuizPatenteB).
