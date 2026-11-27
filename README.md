# Sito Personale

Progetto per il laboratorio di Tecnologie Web (A.A. 2026/2027), Università di Bologna.

## Struttura della cartella

```text
├── index.html        # Home page con obiettivi del progetto
├── about.html        # Chi sono, hobby e galleria fotografica
├── contacts.html     # Modulo di contatto (Bootstrap 5)
├── style/
│   └── style.css     # Foglio di stile
├── img/              # Immagini utilizzate nel sito
└── README.md         # Documentazione del progetto
```

## Caratteristiche principali

- **HTML5 e CSS**: struttura semantica (`header`, `nav`, `section`, `article`, `figure`, `footer`) con foglio di stile esterno (`style/style.css`) e zero stili inline.
- **Tipografia e viewport**: dimensioni del testo in `rem`, con uso di `vh` e `vw` per altezze e spaziature fluide.
- **Posizionamento**: barra di navigazione `sticky` in cima alla pagina e didascalie in `absolute` sopra le foto.
- **Flexbox**: articoli disposti in righe con wrap automatico e galleria che passa a colonna singola su schermi stretti (sotto i 600px).
- **Bootstrap 5**: utilizzato nella pagina contatti per la navbar con hamburger menu e la griglia responsive a colonne.
- **Animazioni**: effetti di hover con `transition` (immagini, bottoni, link) e animazione `fadeInUp` al caricamento dei blocchi.

## Autore

Mattia (Mxttix) — Università di Bologna
