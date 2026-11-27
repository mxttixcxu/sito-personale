# Sito Personale — Laboratorio di Tecnologie Web

Progetto pratico realizzato per le attività di laboratorio del corso di **Tecnologie Web** (A.A. 2026/2027).  
Il sito ha l'obiettivo di sperimentare la strutturazione semantica di pagine web tramite **HTML5**, la formattazione tipografica, il posizionamento degli elementi e la creazione di layout flessibili e responsive con **CSS3** e **Bootstrap 5**.

---

## 📁 Struttura del Progetto

```text
├── html + css/
│   ├── index.html        # Home page di presentazione del progetto e obiettivi
│   ├── about.html        # Sezione biografia, film, musica, hobby e galleria fotografica
│   ├── contacts.html     # Modulo di contatto e recapiti (con Bootstrap 5)
│   ├── style/
│   │   └── style.css     # Foglio di stile CSS personalizzato scritto a mano
│   └── img/              # Immagini e fotografie del sito
└── README.md             # Documentazione del repository
```

---

## 🛠️ Tecnologie Utilizzate & Requisiti Soddisfatti

Il progetto copre progressivamente tutti i concetti e i requisiti affrontati nelle esercitazioni di laboratorio (Esercizi 5–9):

### 1. Tipografia e Unità Relative (Esercizio 5)
* **Root font-size**: impostato `html { font-size: 16px; }` per il calcolo uniforme di tutte le dimensioni in `rem`.
* **Gerarchia scalare**: titoli (`h1: 2rem`, `h2: 1.5rem`, `h3: 1.2rem`, `h4: 1rem`) e paragrafi (`1rem`) dimensionati in `rem` per garantire scalabilità e accessibilità.
* **Leggibilità**: definizione di `line-height: 1.5`, pesi font differenziati (`font-weight: bold / normal`) e fallback universale con `Arial, Helvetica, sans-serif`.
* **Viewport Units (vh, vw)**: impiego di `min-height: 100vh` sul `body`, padding viewport su header (`3vh 2vw`) e sezioni (`2vh 2vw`), e larghezza dell'indice ancorata alla viewport (`60vw` su desktop e `90vw` su mobile).

### 2. Posizionamento (Esercizio 6)
* **Navbar Sticky**: la barra di navigazione principale adotta `position: sticky; top: 0; z-index: 100;` per rimanere visibile e ancorata in cima durante lo scorrimento della pagina.
* **Didascalia Absolute su Relative**: nella galleria di `about.html`, ogni elemento fotografico è un blocco `.gallery-item` in `position: relative`, mentre la relativa didascalia `<figcaption>` è posizionata in `position: absolute; bottom: 0; left: 0; right: 0;` sovrapposta all'immagine.

### 3. Layout Flessibile con Flexbox (Esercizio 7)
* **Blocchi e Articoli**: le sezioni di `index.html` e `about.html` sono flex items (`flex: 1 1 300px;`) all'interno di container flessibili (`display: flex; flex-wrap: wrap;`), che si affiancano su schermi ampi e si riposizionano automaticamente quando lo spazio diminuisce.
* **Galleria Fotografica Fluida**: in `about.html`, le immagini non usano tabelle statiche ma un contenitore flessibile `.gallery-container` con `flex-wrap: wrap;`.
* **Breakpoint Mobile**: tramite `@media (max-width: 600px)`, gli elementi della galleria passano automaticamente a **una sola colonna** (`flex: 1 1 100%`) sugli schermi stretti.

### 4. Framework Bootstrap 5 (Esercizio 8)
Integrato all'interno della pagina `contacts.html`:
* **Navbar Bootstrap 5**: componente `<nav class="navbar navbar-expand-md sticky-top">` dotato di hamburger toggle interattivo per la navigazione mobile.
* **Griglia Responsive `container / row / col-*`**:
  * Utilizzo di classi responsive con breakpoint progressivi (`col-12 col-sm-6 col-lg-4`):
    * 📱 **Mobile (< 576px)**: 1 colonna a tutta larghezza (`col-12`)
    * 💻 **Tablet (≥ 576px)**: 2 colonne affiancate (`col-sm-6`)
    * 🖥️ **Desktop (≥ 992px)**: 3 colonne affiancate (`col-lg-4`)
* **Classi Form di Bootstrap**: il form adotta classi standard (`form-label`, `form-control`, `row g-3`, `mb-3`).
* **Integrazione con CSS custom**: Bootstrap è combinato e armonizzato con il CSS scritto a mano (`style.css`), preservando la palette cromatica e lo stile d'insieme del sito.

### 5. Layout Coerente & Responsive (Esercizio 9)
* **Coerenza grafica**: tutte le pagine condividono lo stesso `<header>`, la stessa barra di navigazione con indicatori di pagina attiva, e lo stesso `<footer>`.
* **Nessuno stile inline**: tutti gli stili sono interamente centralizzati nel foglio `style/style.css`.
* **Mobile-friendly**: testato con tag `<meta name="viewport" content="width=device-width, initial-scale=1.0">`, privo di barre di scorrimento orizzontali anomale.

### 6. Animazioni & Transizioni CSS (Esercizio 9)
* **Transizioni (Hover Effects)**:
  * Ingrandimento fluido delle foto della galleria tramite `transform: scale(1.05)` con `transition: transform 0.25s ease`.
  * Transizione morbida di colore e background sui pulsanti e sui link di navigazione (`transition: background-color 0.3s ease`).
* **Animazione `@keyframes`**: implementata l'animazione `@keyframes fadeInUp` con `animation: fadeInUp 0.5s ease-out;` applicata ai blocchi informativi, per consentire un ingresso morbido dei contenuti all'apertura delle pagine.

---

## 👤 Autore
* **Mattia (Mxttix)**
* Corso di Laurea in Informatica — Università di Bologna
* Attività di laboratorio del corso di **Tecnologie Web**
