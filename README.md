# Spaghetti Unplugged 2027

Sito one-page in sviluppo, basato sul progetto Figma **SITO SPAGHETTi 2027**.

## Struttura del progetto

- `index.html` — documento HTML5 e punto d'ingresso; contiene Hero video, navigazione, Prossimi eventi, banner Open Mic, Chi siamo, Info utili, FAQ e footer.
- `style.css` — stili delle sezioni e dei menu responsive, font personalizzati e animazioni CSS.
- `font/` — file NewEdge 666 Rounded Regular e Light in formato OTF e TTF.
- `img/tappo generico.mp4` — video orizzontale utilizzato nella Hero.
- `img/eventi/`, `img/artisti/`, `img/partner/` — cartelle predisposte per le immagini del sito.

Il logo originale non è ancora presente negli asset: il footer usa un wordmark testuale provvisorio, sostituibile con il file definitivo. Le fasce animate dei partner e degli artisti restano da inserire.

## Hero e navigazione

- La Hero usa il video `img/tappo generico.mp4` in autoplay, muto e in loop. Su Mobile il video riempie la Hero con `object-fit: cover` e viene ritagliato ai lati.
- La navbar Desktop è sovrapposta al video e usa `mix-blend-mode: difference`.
- Su Mobile un unico pulsante apre e chiude il pannello bianco a schermo intero. Le due linee dell'icona si incrociano in una X mentre il pannello scorre da destra.
- Il menu supporta Escape, navigazione da tastiera, gestione del focus, chiusura alla selezione di un link, blocco dello scroll e `prefers-reduced-motion`.

## Fascia marquee

- Subito dopo la Hero compare la fascia verde con la frase “SCEGLI TU LA MUSICA DI DOMANI”, ripetuta per creare una sequenza continua.
- La fascia è alta 26px e usa il font NewEdge 666 Rounded, testo nero e animazione CSS orizzontale regolabile tramite `--music-marquee-duration` in `style.css`.
- La frase viene esposta una sola volta agli screen reader; con `prefers-reduced-motion` l'animazione viene disattivata e il contenuto resta visibile.

## Prossimi eventi

- La sezione `#eventi` contiene placeholder per Roma e Milano; le locandine originali potranno essere inserite in `img/eventi/`.
- Ogni locandina e fascia marquee formano un blocco quadrato responsive. Su Mobile le card scorrono orizzontalmente; da 1200px la griglia Desktop dispone le card su due colonne.
- Le barre “Acquista biglietto” sono predisposte visivamente; i collegamenti saranno aggiunti quando saranno disponibili gli URL.
- Le icone freccia usano Bootstrap Icons via CDN.

## Iscrizione Open Mic

- Dopo `#eventi` compare il banner blu “Iscriviti all'Open Mic”, con tipografia NewEdge 666 e icona Bootstrap Icons.
- Il banner è ancora senza URL: la destinazione verrà aggiunta quando sarà definita. Altezza Desktop attuale: 103px.

## Chi siamo

- La sezione `#chi-siamo` segue il banner Open Mic e contiene titolo e due paragrafi testuali.
- La galleria usa tre placeholder grigio chiaro quadrati. Su Desktop sono disposti in una griglia e possono raggiungere 513 × 513px ciascuno; su Mobile scorrono orizzontalmente e misurano 324 × 324px.
- Da 1200px in su la griglia mostra tre colonne che occupano la larghezza disponibile.
- Testi, proporzioni e spaziature della sezione sono ancora soggetti ad approvazione e verifica con Figma.

## Info utili

- La sezione `#info` segue «Chi siamo?» e presenta il titolo «Info utili» insieme al «Regolamento Open mic».
- Usa sfondo blu `#0b2cff`, testo bianco e font NewEdge 666 Rounded.
- Desktop: titolo 60px, intestazione 40px e paragrafo 30px. Mobile: titolo 50px, intestazione 30px e paragrafo 20px.
- Il paragrafo del regolamento è giustificato su Desktop e Mobile. Le spaziature sono provvisorie e ancora da confrontare con Figma.

## FAQ

- La sezione `#faq` segue «Info utili» e usa un accordion Bootstrap 5.3.8 accessibile e utilizzabile da tastiera.
- La prima domanda è aperta inizialmente; la seconda e la terza sono chiuse. Le risposte usano temporaneamente lo stesso testo Lorem ipsum e compaiono solo quando la relativa domanda viene aperta.
- I simboli `+` e `−` indicano lo stato delle domande. Il testo delle risposte è giustificato su Desktop e Mobile.
- Da 1200px: titolo 60px, domande 50.08px e risposte 30px. Mobile: titolo 50px, domande 40px e risposte 20px.

## Footer

- Il footer segue la FAQ, usa sfondo nero, testi bianchi e font NewEdge 666 Rounded.
- Su Desktop le quattro aree sono distribuite in orizzontale. Il wordmark testuale è impostato a 40.5px; slogan, contatti, voci Legal, social e copyright usano le misure Figma fornite.
- Su Mobile il contenuto è disposto in due colonne: wordmark e slogan a sinistra, Contatti, Legal e Seguici a destra. Wordmark 30px, slogan 11.23px e testi delle colonne 11px; copyright 8px.
- L'email apre `mailto:info@spaghettiunplugged.com`. Instagram, Facebook e le voci Legal restano testo in attesa dei rispettivi URL.
- Il footer usa un wordmark provvisorio perché il logo originale non è presente negli asset locali.

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
