# Spaghetti Unplugged 2027

Sito one-page in sviluppo, basato sul progetto Figma **SITO SPAGHETTi 2027**.

## Struttura del progetto

- `index.html` — documento HTML5 e punto d'ingresso; contiene la Hero video, la navbar desktop, il menu mobile e la sezione Prossimi eventi.
- `style.css` — stili della Hero, navbar, menu responsive e sezioni; include i font personalizzati e le animazioni CSS.
- `font/` — file NewEdge 666 Rounded Regular e Light in formato OTF e TTF.
- `img/tappo generico.mp4` — video orizzontale utilizzato nella Hero.
- `img/eventi/`, `img/artisti/`, `img/partner/` — cartelle predisposte per le immagini del sito.

Il logo originale non è ancora stato aggiunto. Le sezioni Chi siamo e Info utili non sono ancora implementate; i link del menu puntano ai rispettivi ID previsti.

## Hero e navigazione

- La Hero usa il video `img/tappo generico.mp4` in autoplay, muto e in loop. Su Mobile il video riempie la Hero con `object-fit: cover` e viene ritagliato ai lati.
- La navbar desktop è sovrapposta al video e usa `mix-blend-mode: difference`.
- Su Mobile un unico pulsante apre e chiude il pannello bianco a schermo intero. Le due linee dell'icona si incrociano in una X mentre il pannello scorre da destra.
- Il menu supporta Escape, navigazione da tastiera, gestione del focus, chiusura alla selezione di un link, blocco dello scroll e `prefers-reduced-motion`.
- I testi del menu Mobile sono impostati a 30px.

## Fascia marquee

- Subito dopo la Hero compare la fascia verde fluo con la frase “SCEGLI TU LA MUSICA DI DOMANI”, ripetuta per creare una sequenza continua.
- La fascia è alta 26px e usa il font NewEdge 666 Rounded, testo nero e animazione CSS orizzontale regolabile tramite `--music-marquee-duration` in `style.css`.
- La frase viene esposta una sola volta agli screen reader; con `prefers-reduced-motion` l'animazione viene disattivata e il contenuto resta visibile.

## Prossimi eventi

- La sezione `#eventi` contiene due placeholder neutri per Roma e Milano; le locandine originali potranno essere inserite in `img/eventi/`.
- Ogni locandina e fascia marquee formano un blocco quadrato responsive. Su Mobile le card scorrono orizzontalmente.
- Le fasce evento riutilizzano l'animazione CSS della marquee principale. Le barre “Acquista biglietto” sono predisposte visivamente; i collegamenti saranno aggiunti quando saranno disponibili gli URL.
- L'icona freccia usa Bootstrap Icons via CDN.

## Tecnologie

- HTML5
- CSS3
- Bootstrap 5.3.8 tramite CDN jsDelivr
- Bootstrap Icons tramite CDN jsDelivr
- JavaScript puro, senza librerie aggiuntive

## Anteprima locale

Dalla cartella del progetto apri la pagina nel browser predefinito:

```powershell
start index.html
```
