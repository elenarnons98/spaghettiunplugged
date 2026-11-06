# Spaghetti Unplugged 2027

Sito one-page in sviluppo, basato sul progetto Figma **SITO SPAGHETTi 2027**.

## Struttura del progetto

- `index.html` — documento HTML5 e punto d'ingresso; contiene la Hero video, la navbar desktop e il menu mobile con JavaScript puro inline.
- `style.css` — stili della Hero, navbar e menu responsive; include i font personalizzati e le animazioni CSS.
- `font/` — file NewEdge 666 Rounded Regular e Light in formato OTF e TTF.
- `img/tappo generico.mp4` — video orizzontale utilizzato nella Hero.
- `img/eventi/`, `img/artisti/`, `img/partner/` — cartelle predisposte per le immagini delle sezioni future.

Il logo originale non è ancora stato aggiunto. Le sezioni Eventi, Chi siamo e Info non sono ancora implementate; i link del menu puntano ai rispettivi ID previsti.

## Hero e navigazione

- La Hero usa il video `img/tappo generico.mp4` in autoplay, muto e in loop. Su Mobile il video riempie la Hero con `object-fit: cover` e viene ritagliato ai lati.
- La navbar desktop è sovrapposta al video e usa `mix-blend-mode: difference`.
- Su Mobile un unico pulsante apre e chiude il pannello bianco a schermo intero. Le due linee dell'icona si incrociano in una X mentre il pannello scorre da destra.
- Il menu supporta Escape, navigazione da tastiera, gestione del focus, chiusura alla selezione di un link, blocco dello scroll e `prefers-reduced-motion`.
- I testi del menu Mobile sono impostati a 30px.

## Tecnologie

- HTML5
- CSS3
- Bootstrap 5.3.8 tramite CDN jsDelivr
- JavaScript puro, senza librerie aggiuntive

## Anteprima locale

Dalla cartella del progetto apri la pagina nel browser predefinito:

```powershell
start index.html
```
