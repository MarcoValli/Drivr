# Drivr — Quiz Patente B

Web app per esercitarsi ai quiz della patente B in stile "Tinder": **freccia destra = VERO**, **freccia sinistra = FALSO** (funziona con tastiera, mouse e swipe da telefono).


## Funzioni
- Schede a swipe (destra = VERO / sinistra = FALSO) con animazione;
- Sezione **Progressi** con due tab: **Stats** (storico test cronologico) e **Sbagliate**
- Blocchi da **30 domande**, esito **≤3 errori = Promosso**
- Dati salvati in locale nel browser (nessun server)
- **Impostazioni**: attiva/disattiva le domande precaricate, attiva/disattiva le domande AI, importa altri JSON (che si **aggiungono** ai precedenti), **Danger zone** per azzerare i risultati
- Pacchetto **Novità 2026 (AI)**: angoli ciechi, ADAS, monopattini, smartphone, neopatentati (non ufficiale, solo ripasso)

## Domande incluse
- **28 domande "Novità 2026"** scritte da me con l'AI (chiaramente etichettate, non ufficiali)
- **Archivio completo (~7.139 domande, con immagini): si carica DA SOLO al primo avvio**
  scaricandolo da GitHub e mettendolo in cache (funziona poi anche offline). Nessun import manuale.


## Note
Le domande "Novità 2026" sono una rielaborazione fedele del nuovo Codice della Strada (in vigore dal 14/12/2024) fatta con l'AI: utili per ripassare i temi nuovi, ma **non** sono estratti certificati dell'archivio ministeriale. Fonte del dataset ministeriale: [Ed0ardo/QuizPatenteB](https://github.com/Ed0ardo/QuizPatenteB).
