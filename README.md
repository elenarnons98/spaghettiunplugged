# Spaghetti Unplugged 2027

Sito one-page in sviluppo, basato sul progetto Figma **SITO SPAGHETTi 2027**.

## Struttura del progetto

- `index.html` — documento HTML5 e punto d'ingresso, con titolo pagina “Spaghetti Unplugged”; contiene Hero video, navigazione, Prossimi eventi, banner Open Mic, Chi siamo, Info utili, FAQ e footer.
- `style.css` — stili delle sezioni e dei menu responsive, font personalizzati e animazioni CSS.
- `font/` — file NewEdge 666 Rounded Regular e Light in formato OTF e TTF.
- `img/tappo generico.mp4` — video Hero per Desktop.
- `img/video home mobile.mp4` — video Hero per Mobile.
- `img/favicon-spaghetti-unplugged/` — favicon ICO/SVG, icona Apple, icone PNG e manifest installabile.
- `img/eventi/`, `img/artisti/`, `img/partner/` — cartelle predisposte per le immagini del sito.

Il logo originale non è ancora presente negli asset: il footer usa un wordmark testuale provvisorio, sostituibile con il file definitivo. Le fasce animate dei partner e degli artisti restano da inserire.

## Hero e navigazione

- La Hero seleziona `img/video home mobile.mp4` sui viewport fino a 767.98px e `img/tappo generico.mp4` sugli schermi più larghi. Entrambi i video sono configurati in autoplay, muto, in loop e con riproduzione inline.
- Il video riempie la Hero con `object-fit: cover`; il video orizzontale Desktop viene ritagliato ai lati sui viewport verticali.
- La navbar Desktop e il marchio Mobile sono fissi in alto durante lo scorrimento, sovrapposti alla pagina e usano `mix-blend-mode: difference`.
- Su Desktop, la pagina è centrata e limitata a 1920px; la navbar fissa è centrata e allineata alla larghezza della pagina.
- Le favicon sono collegate dall'`<head>` e il manifest usa percorsi relativi alle icone nella propria cartella; il colore del tema è `#BEFF00`.
- Su Mobile il pulsante hamburger è fisso in alto. Apre e chiude il pannello bianco a schermo intero; le due linee si incrociano in una X mentre il pannello scorre da destra.
- Il menu supporta Escape, navigazione da tastiera, gestione del focus, chiusura alla selezione di un link, blocco dello scroll e `prefers-reduced-motion`.

## Fascia marquee

- Subito dopo la Hero compare la fascia verde con la frase “SCEGLI TU LA MUSICA DI DOMANI”, ripetuta per creare una sequenza continua.
- La fascia è alta 32px su Desktop e Mobile e usa il font NewEdge 666 Rounded, testo nero e animazione CSS orizzontale regolabile tramite `--music-marquee-duration` in `style.css`.
- La frase viene esposta una sola volta agli screen reader; con `prefers-reduced-motion` l'animazione viene disattivata e il contenuto resta visibile.

## Prossimi eventi

- La sezione `#eventi` mostra le locandine definitive: `IMG_8024.JPEG` per Roma e `IMG_8023.JPEG` per Milano, salvate in `img/eventi/`.
- Le locandine sono mostrate come immagini di sfondo con `background-size: cover`; il contenitore è quadrato su Desktop e Mobile. Su Mobile le card scorrono orizzontalmente; da 1200px la griglia Desktop dispone le card su due colonne.
- Le barre “Acquista biglietto” collegano alle rispettive pagine DICE in una nuova scheda. Mantengono altezza 52px su Desktop e 38px su Mobile.
- Il collegamento “Vedi tutti” è temporaneamente nascosto.
- Le icone freccia usano Bootstrap Icons via CDN.

## Iscrizione Open Mic

- Dopo `#eventi` compare il banner blu “Iscriviti all'Open Mic”, con tipografia NewEdge 666 e icona Bootstrap Icons.
- Il banner apre `https://hatmusic.onelink.me/1oIL/ru3bu1ni` in una nuova scheda. Altezza Desktop attuale: 103px.

## Chi siamo

- La sezione `#chi-siamo` segue il banner Open Mic e contiene titolo e due paragrafi testuali.
- Da Desktop il layout usa due colonne uguali (50% titolo, 50% testi); su Mobile titolo e testi restano impilati.
- Il titolo è 50px e il primo paragrafo 30px su Desktop e Mobile; il secondo paragrafo è 25px su Desktop e 16.81px su Mobile.
- Entrambi i paragrafi sono giustificati.
- La galleria contiene dieci placeholder grigio chiaro. Su Desktop scorrono in orizzontale, sono larghi 513px e hanno un'altezza minima di 19rem; su Mobile scorrono con swipe e misurano 324 × 324px.
- La scrollbar è nascosta; su Desktop è possibile trascinare la galleria con il mouse, mentre su Mobile rimane attivo lo scorrimento touch. Non è previsto scorrimento automatico.
- Testi, proporzioni e spaziature della sezione sono ancora soggetti ad approvazione e verifica con Figma.

## Info utili

- La sezione `#info` segue «Chi siamo?» e presenta il titolo «Info utili» insieme al «Regolamento Open mic».
- Usa sfondo blu `#0b2cff`, testo bianco e font NewEdge 666 Rounded.
- Desktop: titolo 50px, intestazione 40px e paragrafo 30px. Mobile: titolo 50px, intestazione 30px e paragrafo 20px.
- Il regolamento è articolato in quattro paragrafi sul funzionamento e sulle finalità dell'Open Mic. I paragrafi sono giustificati su Desktop e Mobile, con una spaziatura di `1em` tra l'uno e l'altro.

## FAQ

- La sezione `#faq` segue «Info utili» e usa un accordion Bootstrap 5.3.8 accessibile e utilizzabile da tastiera.
- La prima domanda è aperta inizialmente; la seconda e la terza sono chiuse. Le risposte descrivono iscrizione, premio e modalità di vittoria, e compaiono solo quando viene aperta la relativa domanda.
- Le risposte possono contenere più paragrafi, separati da uno spazio di `1em`.
- I simboli `+` e `−` indicano lo stato delle domande. Il testo delle risposte è giustificato su Desktop e Mobile.
- Il titolo FAQ è 50px e le domande sono 40px su Desktop e Mobile. Le risposte sono 30px su Desktop da 1200px e 20px su Mobile.
- I titoli principali di Prossimi eventi, Chi siamo, Info utili e FAQ sono impostati a 50px.

## Footer

- Il footer segue la FAQ, usa sfondo nero, testi bianchi e font NewEdge 666 Rounded.
- Su Desktop sono presenti wordmark e slogan a sinistra, Contatti nella terza colonna e Seguici a destra, con spazio libero tra le aree. Il wordmark è 40.5px; slogan, contatti, social e copyright usano le misure Figma fornite.
- Su Mobile il contenuto è disposto in due colonne: wordmark e slogan a sinistra, Contatti e Seguici a destra. Wordmark 30px, slogan 11.23px e testi delle colonne 11px; copyright 8px.
- L'email apre `mailto:info@spaghettiunplugged.com`. Instagram e Facebook restano testo in attesa dei rispettivi URL. Non è presente la sezione Legal.
- Il footer usa un wordmark provvisorio perché il logo originale non è presente negli asset locali.

## Tecnologie

- HTML5
- CSS3
- Bootstrap 5.3.8 tramite CDN jsDelivr
- Bootstrap Icons tramite CDN jsDelivr
- JavaScript puro, senza librerie aggiuntive

## Layout responsive e overflow

- Nei breakpoint da 768px, i gutter orizzontali delle righe Bootstrap `.about-layout`, `.info-layout` e `.faq-layout` sono sincronizzati con il padding dei rispettivi container: il padding laterale equivale a metà del gutter.
- Il gutter Desktop è limitato a 2rem, mantenendo gli allineamenti e le colonne esistenti ed evitando che i margini negativi delle righe producano overflow orizzontale.
- La correzione usa il normale dimensionamento del layout, senza nascondere l'overflow su `html` o `body`. La verifica visiva ai breakpoint resta da fare manualmente.

## Anteprima locale

Dalla cartella del progetto apri la pagina nel browser predefinito:

```powershell
start index.html
```
