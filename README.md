# NBT Studio 1.2

World editor per Minecraft Java con interfaccia a pagine.

| Pagina | Cosa fa |
|---|---|
| **Home** | Mondi della cartella saves e aperti di recente, con icona, ricerca e doppio clic per aprirli |
| **World Settings** | Nome, modalita, difficolta, hardcore, cheat, ora, meteo, spawn, **world border**, game rules, info sul mondo |
| **Player** | Testa e nome, vita, fame, XP, posizione, **permessi (volo, invulnerabile...)**, inventario e **ender chest** con icone 3D come nel gioco; **trascina gli oggetti** tra gli slot o dalla palette di tutti gli oggetti; **editor oggetto** con nome e lore colorati (**gradienti**, grassetto, corsivo...), **incantesimi**, durabilita, indistruttibile, colore del cuoio, piu l'editor NBT completo |
| **Chunk Map** | **Viste Chunks / Terreno / Grotte**: il terreno vero visto dall'alto con texture, rilievo, ombre e profondita dell'acqua; zoomando si vedono le texture dei singoli blocchi; vista **Grotte** a un'altezza scelta; **vista 3D isometrica** della selezione; salvataggio immagine della mappa. Inoltre: | Mappa con zoom/pan e selezione; selezione per distanza, attivita o chunk non finiti; **mappa di calore**; **doppio clic su un chunk per modificarne l'NBT**; potatura; **compattazione**; **esporta la selezione come nuovo mondo** |
| **NBT Editor** | Albero NBT con filtro; **modifica come testo SNBT**; esporta in SNBT; **salva una copia in altro formato** (Java gzip/zlib/non compresso, Bedrock) |

In piu: **Annulla/Ripeti** (Ctrl+Z / Ctrl+Y) su tutte le modifiche, backup zip del mondo, backup automatico `.bak`.

## Menu
Il menu a sinistra è diviso in sezioni: **Mondo** (Home, Impostazioni mondo, Mappa chunk, Editor NBT, Datapack),
**Giocatori** (Giocatore, Trasferisci oggetti), **Editor** (Scoreboard e team, Villaggi, Mappe in gioco), **Generatori** (Comandi; Fuochi, pozioni,
testi; Costruzioni; Datapack e preset), **Resource pack** (Pack Studio) e **Analisi** (Statistiche mondo). Le **Impostazioni** sono sempre in fondo
al menu e anche nell'ingranaggio ⚙ in alto a destra.

## Novità: più semplice da usare
- **Cerca una funzione**: la casella sopra il menu trova dove si fa una cosa (es. "cucciolo", "labirinto", "kit").
- **Tour di benvenuto** al primo avvio (si rivede dalle Impostazioni).
- **Tema chiaro o scuro** e **modalità semplice** (nasconde le pagine per esperti) nelle Impostazioni.

## Pack Studio (menu Resource pack)
Strumenti per i resource pack nello stile dell'app MCTools: tema viola, titoli con il font di Minecraft, schede.
Crei, clicchi **Importa nel gioco** e giochi: il pack va nella cartella `resourcepacks` e viene attivato in
`options.txt` (con Minecraft chiuso; si tiene una copia `options.txt.nbtstudio.bak`). Formato giusto per ogni
versione (letto dai jar installati, fino alla 26.x).
- **Crea totem**: totem dell'immortalità con la skin di un giocatore (nome Java o file), 3 stili.
- **Crea dischi musicali**: sostituisci un disco con la tua musica (.ogg; MP3/WAV/FLAC con ffmpeg), nome nel
  gioco, colore o immagine dell'etichetta, e per la 1.21+ un datapack con la nuova durata nel giradischi.
- **Quadri personalizzati**: le tue immagini sui quadri, con le misure in blocchi di ogni quadro.
- **Emoji personalizzate**: immagini che diventano caratteri da incollare in chat.
- **Crea avatar**: immagine profilo da una skin (faccia, busto, corpo), fino a 2048 px.
- **Unisci pack**, **Pack installati** (attiva, disattiva, togli), **Codici colore** e **Coordinate**
  Overworld ↔ Nether.

## Trasferisci oggetti (menu Giocatori)
Due inventari disegnati come nel gioco: scegli chi dà e chi riceve, clicca gli oggetti (o spunta barra rapida,
inventario, armatura, mano secondaria, ender chest) e **copia**, **sposta** o **scambia**. Gli oggetti vanno negli
stessi slot se liberi, altrimenti nel primo libero (e nella ender chest se serve); quello che non ci sta resta al
primo giocatore. I **kit** salvano gli oggetti scelti per ridarli a chiunque, anche in altri mondi.
Il pulsante **Poteri del giocatore** (pagina Giocatore) cambia vita massima, velocità, dimensione, salto, portata
e altri attributi con i cursori, con preset (Gigante, Minuscolo, Super velocità, Corazzato, Salto lunare).

## Editor del mondo
- **Pennello blocchi e pennello biomi** (Mappa chunk, riga "Strumento"): trascina sulla mappa per mettere blocchi
  sopra, sostituire o togliere la superficie, fare colonne, oppure dipingere un bioma; dimensione del pennello a
  scelta. Ogni tratto viene scritto subito (conferma e backup chiesti una volta sola).
- **Chunk degli slime** (calcolati dal seme, come nel gioco) e **Strutture** (villaggi, templi, fortezze... lette
  dai chunk, cioè quelle davvero generate) sovrapposti alla mappa.
- **Tasto destro sulla mappa**: sposta un giocatore in quel punto (sul terreno), imposta lì il suo punto di respawn
  o lo spawn del mondo (formati 26.x e precedenti).
- **Vista 3D**: "Modifica i blocchi con un clic" mette un blocco accanto alla faccia cliccata, lo sostituisce o lo
  toglie; la vista si aggiorna da sola. **Video (GIF)**: una giornata col sole che gira fino alla notte, oppure i
  quattro lati.
- **Strumenti di costruzione**: oltre alle strutture .nbt esportano e importano **.schem** (WorldEdit / FAWE,
  versioni 2 e 3) e **.litematic** (Litematica).
- **Scoreboard e team**: obiettivi, punteggi, team (colore, prefisso, suffisso, fuoco amico, nomi, spinte, membri),
  cosa mostrano barra laterale / lista / sotto il nome, e boss bar.
- **Villaggi**: trova i villici di una dimensione e li divide per villaggio (campana); lavoro, livello, letto,
  blocco di lavoro e opinione dei giocatori. Pulsanti: ama un giocatore (prezzi migliori), dimentica, rinnova gli
  scambi, livello esperto, dimentica letto e lavoro, ferma i raid.
- **Mappe in gioco**: tutte le mappe di carta con l'immagine, salvataggio in PNG, blocco, un'immagine dentro una
  mappa o **nuove mappe da un'immagine** (anche più mappe per un muro di cornici) con i comandi /give
  (data/map_N.dat fino alla 1.21, data/minecraft/maps nei 26.x).
- **Datapack**: attiva o disattiva i datapack del mondo e gli esperimenti, aggiungi zip o cartelle, togli.

## Generatori
- **Fuochi, pozioni, testi**: fuochi d'artificio con **anteprima animata in 3D** (la forma vera: sfera, grande, stella, creeper, esplosione; bagliore, sfumature,
  scia, scintillio; /give o /summon), pozioni e frecce intinte con la **boccetta del colore del gioco** (si mescola
  con gli effetti scelti), messaggi
  **/tellraw** e **/title** con colori, gradienti, clic e hover, **/execute** passo per passo con aiuto per i
  selettori, e **teste personalizzate** da nome, URL o valore texture (con la faccia in anteprima). Tutto nella
  sintassi della versione scelta (1.8 ... 26.x).
- **Costruzioni** (nel mondo aperto, con anteprima 3D prima di piazzare): **pixel art** da un'immagine (lana,
  cemento, terracotta, legni, pietre, metalli; stesa a terra o in piedi; dithering), **forme** (sfera, cupola,
  cilindro, cono, piramide, scatola, anello, arco, piene o vuote), **strade** tra due punti che seguono il
  terreno (alberi tagliati, ponti sull'acqua, bordi, lampioni) e **alberi o foreste** (quercia, betulla, abete,
  quercia scura, giungla, ciliegio, acacia, quercia pallida) solo su terreno adatto.
- **Datapack e preset**: crea un datapack con ricette (crafting con griglia 3x3 o senza forma, fornace, altoforno,
  affumicatore, falò), drop di mob e blocchi, progressi (ottenere un oggetto, uccidere un mob, cambiare dimensione)
  e funzioni (al caricamento o a ogni tick), nel formato giusto per la versione (letto dai jar installati); salva
  lo zip o mettilo direttamente nel mondo. **Preset superpiatti** con anteprima degli strati, e
  **Crea un mondo superpiatto**: nuovo mondo pronto nella cartella saves (1.8 ... 26.x: nome, seme, modalità,
  trucchi, villaggi, fortezze).
- **Spawner** (Generatori › Fuochi e pozioni): qualsiasi mob, velocità, quanti per volta, raggio; /give o
  /setblock nella sintassi della versione, con preset (farm veloce, stanza del boss, sempre attivo).
- **Labirinti e arene** (Costruzioni): labirinto perfetto con entrata e uscita, corridoi larghi a scelta, tetto di
  vetro e luci; arena rotonda con gradinate.
- **Bauli con bottino casuale** (Datapack › Drop): più oggetti con probabilità, e il comando /setblock pronto.
- **Mappa come pagina web**: Salva immagine mappa › "Pagina web da esplorare (*.html)": si apre nel browser, si
  sposta e si zooma e mostra le coordinate sotto il mouse.
- **📍 Scegli sulla mappa**: nelle costruzioni non serve scrivere coordinate, clicchi sulla mappa del mondo e
  vedi dove finisce l'ingombro; l'altezza la trova da solo (o usa la posizione del giocatore o dello spawn).
- Ogni pagina ha una **guida a passi** in alto e il menu ha le **icone di Minecraft**.

## Statistiche mondo
Legge un'intera dimensione in sottofondo: i blocchi più comuni, quanti **minerali** e a che **altezze** (grafico),
una **mappa** di dove si trova ogni minerale (un pixel per chunk) e le entità per tipo. Non cambia niente.

## Avvio
    pip install PySide6 numpy
    python app.py                    # oppure: python app.py "C:\percorso\del\mondo"


## Versione .exe (senza installare Python)
- Doppio clic su **build_exe.bat**: installa PyInstaller, PySide6 e numpy e crea l'eseguibile.
  - scelta **1**: un solo file `dist\NBTStudio.exe` (comodo da spostare, si apre in qualche secondo)
  - scelta **2**: cartella `dist\NBTStudio\` (si apre subito; va copiata tutta la cartella)
- L'exe funziona su altri PC Windows senza Python. Impostazioni, cache e modelli restano in `%USERPROFILE%\.nbt_studio`.
- L'icona e in `app.ico` (si rigenera con `python make_icon.py`); la ricetta di PyInstaller e `nbt_studio.spec`.
- Windows SmartScreen puo avvisare al primo avvio perche l'exe non e firmato: "Ulteriori informazioni" > "Esegui comunque".
## Chunk Map - comandi
- Trascina: seleziona. **Ctrl**+trascina aggiunge, **Shift**+trascina toglie
- Tasto destro/centrale (o "Hand tool"): sposta la vista. Rotella: zoom. "Go" salta a coordinate
- Pallino verde = spawn, giallo = giocatore
- "Scan chunks" legge tempo di permanenza dei giocatori e stato di generazione di ogni chunk; poi puoi colorare la mappa,
  selezionare i chunk poco usati o quelli lasciati a meta
- La potatura elimina i chunk da `region`, `entities` e `poi` insieme e ricompatta i file; prima propone un backup

## Lingua e impostazioni
- L'interfaccia e in **italiano** (predefinito) o **inglese**: pagina **Impostazioni** > Lingua, poi "Riavvia ora".
  Nomi di oggetti, incantesimi, attributi e biomi sono quelli ufficiali del gioco, letti dai file lingua di
  Minecraft gia presenti sul PC (`.minecraft/assets`). Anche i pulsanti standard (OK, Annulla...) sono tradotti.
- **Memoria e prestazioni**: profilo Basso / Bilanciato / Alto oppure valori personalizzati (region e texture
  tenute in memoria, processi per leggere la mappa, zona 3D massima, profondita e qualita del 3D),
  **limite RAM** (Windows, minimo 1024 MB), RAM in uso e "Libera memoria ora".
- **Cache su disco**: dimensione massima (i dati piu vecchi vengono tolti all'avvio), riduci o svuota.
- **Backup e privacy**: proposta di backup prima delle modifiche ai chunk, cartella dei backup, download delle
  teste dei giocatori.
- Le impostazioni sono in `~/.nbt_studio/config.json`.

## Player - inventario
- **Clic** su uno slot: apre l'editor dell'oggetto. **Trascina** uno slot su un altro per spostarlo (scambia se occupato),
  con **Ctrl** lo copia. Trascina sul riquadro rosso per eliminarlo. **Tasto destro**: copia, incolla, duplica, quantita.
- **Palette**: tutti gli oggetti della versione scelta, con ricerca; trascinali negli slot o fai doppio clic.
- **Nome e lore**: colore singolo o **gradiente** (fino a 8 colori, con preset come Rainbow, Fire, Ocean...),
  grassetto, corsivo, sottolineato, barrato, offuscato. Nel testo puoi usare i codici `&c`, `&l`, `&#FF8800`, `&r`.
  Anteprima del tooltip come nel gioco.
- **Barra del gradiente** (come il generatore RGB di birdflop.com): i colori sono maniglie sotto la barra;
  **trascinali** per spostarli lungo il testo (anche uno oltre l'altro per cambiare l'ordine), clic sulla barra
  per aggiungere un colore in quel punto, doppio clic per cambiarlo, tasto destro o trascinalo in basso per
  toglierlo. Pulsanti: aggiungi, togli il selezionato, inverti, distribuisci in modo uniforme. Riaprendo un nome
  salvato, i colori e le loro posizioni vengono ricostruiti dalle lettere.
- **Incantesimi**: lista con quelli adatti all'oggetto, livelli fino a 255, "Max all", libri incantati.
- **Attributi**: danno, velocita d'attacco, armatura, vita massima, velocita, scala, gravita, portata... con
  operazione (somma, % della base, moltiplica) e slot (mano, testa, ovunque...). Attenzione: un oggetto con
  attributi propri perde quelli normali; "Add item defaults" li aggiunge per poterli aumentare.
- I dati vengono scritti nel formato giusto per la versione del mondo: 1.8-1.12 (codici §), 1.13-1.20.4 (JSON),
  1.20.5-1.21.4 (components) e 1.21.5+ (components NBT, armatura in `equipment`). Prima della 1.16 i gradienti
  usano i 16 colori classici.
- **Contenitori come oggetti**: casse, barili, scatole shulker, tramogge, distributori, fornaci, alambicchi,
  sacchetti (bundle)... aprono l'editor oggetti direttamente sulla scheda **"Contenuto"** (o tasto destro sullo
  slot > "Contenuto…"); le icone di casse, shulker, teste, scudi sono i loro modelli 3D. Si riempiono direttamente
  nell'inventario, anche uno dentro l'altro (una shulker piena dentro una cassa), con trascinamento tra gli slot,
  "Riempi gli slot vuoti" e la tabella del bottino. Il tooltip dello slot dice quanti oggetti contiene.
- **"Dati del blocco…"** per gli altri blocchi con dati (spawner, alveari, blocchi comandi, beacon, cartelli...).
- **Trim delle armature** (1.20+): pulsante **"Trim armatura…"** con anteprima 3D sullo stand (anche il set
  completo), tutti i motivi e materiali della versione con le loro icone, cambio del tipo di armatura e "Casuale".
  Il trim si vede anche sull'icona dell'oggetto e nell'anteprima degli armor stand, come nel gioco (con le
  varianti scure, es. trim d'oro su armatura d'oro).
- **File del giocatore senza mondo**: "Apri file del giocatore…" (pagina Giocatore o menu File), oppure
  trascina un file `.dat` sulla finestra: si modifica come gli altri giocatori e si salva con Ctrl+S. Si
  possono trascinare anche cartelle dei mondi, `level.dat` e altri file NBT.
- **Cartelle dei server**: "Apri cartella…" (o trascina la cartella `players`, `players/data` o `playerdata`)
  apre tutti i giocatori in un attimo (i file si leggono quando li selezioni). Sui server Paper / Spigot si
  vede il **nome** salvato dal server, l'elenco è in ordine alfabetico e le copie vecchie sono indicate.
  Teste: account Java da Mojang; giocatori **Bedrock** (Geyser / Floodgate) dal servizio pubblico di skin di
  GeyserMC; giocatori di server **offline / craccati** con la skin dell'account Java con lo stesso nome, se
  esiste; altrimenti una skin predefinita del gioco (Steve, Alex...). Il download si può spegnere nelle
  Impostazioni (teste dei giocatori).

## Testo con il font di Minecraft
- Il **tooltip** nell'editor oggetti, il **nome sopra la testa** dei mob (scheda Generale) e la **pagina del
  libro** (scheda Libro, a capo come nel gioco, 14 righe) sono disegnati con il **font del gioco** preso dalla
  versione scelta: larghezza di ogni lettera, ombra, accenti, grassetto, corsivo, sottolineato, barrato e
  testo offuscato animato. Senza texture si usa il testo normale.
- L'elenco degli id nell'editor oggetti mostra l'**icona** di ogni oggetto; la scheda Equipaggiamento mostra
  nome e incantesimi accanto a ogni slot.

## Link e aggiornamenti
- In basso a sinistra, sotto il menu: **Crediti codici sorgenti** (GitHub di
  [Minecraft-ArmorStand](https://github.com/haselkern/Minecraft-ArmorStand) di haselkern, base dell'editor armor
  stand) e **NIKstudios Links**: il **server Discord** di NBT Studio e il **GitHub** di NIKstudios.
- **Aggiornamenti automatici**: all'avvio (si può spegnere in Impostazioni > Aggiornamenti, dove c'è anche
  "Controlla ora") NBT Studio legge `version.txt` dal repository GitHub (`REPO` in `updater.py`). Se il numero
  è più alto della sua versione chiede se aggiornare: scarica `NBTStudio.exe` dall'ultima release, controlla che
  sia integro, si chiude, sostituisce l'exe (tenendo il vecchio finché il nuovo è al suo posto) e si riavvia.
  Si può anche "Saltare questa versione". Funziona con l'exe in un solo file; la versione a cartella e quella
  avviata da Python aprono invece la pagina di download.

### Come pubblicare un aggiornamento
1. Alza il numero in `version.py` (es. `VERSION = "1.3"`).
2. Crea l'exe con `build_exe.bat` (scelta 1, un solo file).
3. Su GitHub crea una **Release** (es. tag `v1.3`) e allega `dist\NBTStudio.exe` con questo nome esatto.
4. Nel repository, nel ramo `main`, aggiorna `version.txt`: la prima riga è il numero (`1.3`). Righe
   facoltative: `notes=testo mostrato all'utente`, `sha256=...` (controllo di integrità, si ottiene con
   `certutil -hashfile dist\NBTStudio.exe SHA256`), `url=...` (se l'exe non è nell'ultima release).
5. Da quel momento chi apre NBT Studio riceve l'aggiornamento.

## Discord (Rich Presence)
- Nelle Impostazioni, sezione **Discord**: "Mostra su Discord che sto usando NBT Studio". Il profilo mostra
  NBT Studio, la pagina in cui sei, da quanto tempo e (se vuoi) il nome del mondo. È spento di default.
- Usa l'applicazione Discord ufficiale di NBT Studio (l'ID è già nel programma, non va inserito). L'immagine
  grande dell'attività è l'asset chiamato `logo` dell'applicazione. Funziona con l'app di Discord aperta sul PC;
  disattivandolo o chiudendo NBT Studio l'attività sparisce.

## Texture dei blocchi
- Mappa 2D e vista 3D prendono la texture di ogni blocco dal **suo modello del gioco** (blockstate → modello →
  faccia superiore / laterale), quindi anche blocchi come i command block hanno la loro texture vera.
- **Barriere, blocchi luce e structure void** (invisibili nel gioco) si vedono semitrasparenti con la loro icona.

## Contenitori come nel gioco
- Fornaci (anche altoforno e affumicatore), alambicco, distributore, espulsore, tramoggia, fabbricatore, bauli,
  barili e scatole shulker mostrano la **loro schermata del gioco** (presa dalla versione scelta) con gli slot
  al posto giusto: ingrediente, combustibile e risultato della fornace, ampolle e polvere di blaze
  dell'alambicco... Vale per i blocchi piazzati e per gli oggetti nell'inventario.

## Mappa 2D: facce dei mob, letti, foglie, rilievo
- I mob sulla mappa (e nell'elenco Entità) sono la **faccia** del mob presa dalla sua texture, con gli strati
  esterni (cappelli, cappucci, vestiti del villager e il cappello della sua professione): zombi, scheletri,
  creeper, villager, illager, streghe, mucche, maiali, pecore, golem, cavalli (di profilo), gatti, api,
  axolotl, panda e altri; quelli che mancano restano uova.
- Il **letto** è un unico letto, come nel gioco: una sola icona, un solo elemento nell'elenco (modifica ed
  eliminazione valgono per le due metà) e, ingrandendo, la sua texture vista dall'alto con il cuscino dalla
  parte giusta.
- Le **foglie** lasciano vedere il terreno nei buchi, in ombra; il **rilievo** ingrandito ha una sfumatura ai
  bordi dei blocchi (ombra dove il vicino è più alto, bordo chiaro verso il sole) regolata dal cursore
  "Rilievo". La prima apertura dopo l'aggiornamento ricalcola la cache della mappa.

## Chunk Map - strumenti sui chunk
- **Tasto destro** su un chunk (senza trascinare): modifica NBT, 3D del chunk, copia, incolla qui, sposta qui,
  elimina. Gli stessi comandi sono nel riquadro "Chunk tools".
- **Copia / Incolla**: copia blocchi, entita e punti di interesse; si puo incollare in un altro punto, in
  un'altra dimensione o in **un altro mondo** (gli appunti restano aprendo un altro mondo). Le coordinate interne
  (casse, cartelli, mob, letti dei villager...) vengono spostate e le entita copiate ricevono nuovi UUID.
- **Sposta**: come copia + incolla, poi la posizione vecchia viene svuotata (si rigenera).
- **Replace blocks**: sostituisce un blocco con un altro nella selezione (anche solo tra due altezze).
- **Set biome**: imposta un bioma su tutti i chunk selezionati (mondi 1.18+).
- Prima di ogni modifica viene chiesta conferma e proposto il backup.

## Entità e block entity
- Seleziona dei chunk e premi **"Entità e block entity..."** (oppure tasto destro sulla selezione / su un chunk):
  elenco di mob, animali, villager, oggetti a terra, nuvole di pozione, spawner, casse e altri blocchi, con icone,
  nomi ufficiali, filtri e ricerca. Doppio clic per modificare; anche Duplica ed Elimina.
- **Editor completo** (le schede compaiono in base al tipo):
  - *Generale*: posizione, rotazione, nome con colori e gradienti, nome sempre visibile, senza IA, invulnerabile,
    silenzioso, senza gravità, contorno luminoso, non scompare, vita, cucciolo, fiamme, loot table delle casse
  - *Colore bagliore*: il colore del contorno luminoso (16 colori). Nel gioco il contorno prende il colore del
    **team dello scoreboard**: NBT Studio mette l'entità nel team `nbts_glow_<colore>` dello scoreboard del mondo
    (`data/scoreboard.dat`, `data/minecraft/scoreboard.dat` nei 26.x), che colora anche il nome. "Bianco (nessun
    team)" la toglie dai team (quelli di NBT Studio rimasti vuoti si cancellano). Scegliere un colore attiva il
    contorno. Per uova spawn, spawner e comandi il mob riceve il tag `Team` ed entra nel team quando appare: il
    team viene creato nel mondo aperto; per altri mondi la pagina Comandi mostra i due comandi `/team` da eseguire
    prima. I team `nbts_glow_...` restano anche vuoti (servono alle uova). Nota: in Creativa i giocatori possono
    comunque uccidere i mob invulnerabili (è così nel gioco).
  - *Equipaggiamento*: mani, armatura, corpo, con probabilità di drop (editor oggetti completo per ogni slot)
  - *Effetti* (anche infiniti), *Attributi* (vita massima, velocità, danno, scala, salto...)
  - *Scambi* dei villager e dei mercanti: professione, livello, tipo, esperienza, e ogni scambio con oggetti
    da comprare / vendere, usi, XP, prezzo; usi illimitati, duplica, riordina
  - *Spawner*: mob generato (anche personalizzato: nome, armi, effetti...), tempi, quantità, distanze
  - *Nuvola di pozione*: pozione, colore, particelle, raggio, durata (anche per sempre) ed effetti extra
  - *Contenuto* di casse, barili, tramogge, fornaci... con la scelta della **tabella del bottino** (casse dei
    dungeon, templi, trial chambers...) e il seme
  - *Drop* dei mob: normali, niente, quelli di un altro mob (es. zombi con i drop dello scheletro wither) o una
    tabella personalizzata; pulsanti rapidi "Cade sempre / Non cade mai / Normale" per l'equipaggiamento
  - *Oggetto* per gli oggetti a terra: non sparisce mai, nessuno può raccoglierlo, indistruttibile (per esposizioni)
- Nell'editor oggetti, per **spawner** e **uova spawn** c'è il pulsante "Spawner / mob…": spawner personalizzati
  nell'inventario e uova con mob su misura.
- **Dati del blocco negli oggetti** (es. un blocco copiato con Ctrl + clic centrale): il pulsante "Dati del
  blocco…" compare per ogni oggetto che li contiene. Schede dedicate:
  - *Blocco comandi*: comando, sempre attivo, conserva l'ultimo output, una volta per tick, esecuzioni riuscite
  - *Cartello* (anche sospeso): fronte e retro con 4 righe ciascuno (codici `&`), tintura, testo luminoso,
    cerato, con l'anteprima come la schermata di modifica del gioco (legno giusto, font di Minecraft). Formati
    1.8-1.19 (`Text1`...), 1.20+ (`front_text`/`back_text`) e 1.21.5+ (testo NBT)
  - casse, fornaci e altri contenitori hanno già la scheda *Contenuto* con l'interfaccia come nel gioco
- Per i mob non ancora nel mondo (uova, spawner, comandi) l'editor non mostra posizione e rotazione e salva solo
  quello che hai cambiato (una posizione 0,0,0 sposterebbe il mob all'origine del mondo). "Cucciolo" c'è per tutti
  i mob che possono esserlo (`Age` per animali e villager, `IsBaby` per zombi, piglin e simili). Sui supporti per
  armature non compaiono le opzioni che valgono solo per i mob (senza IA, mancino...).
- Le modifiche si salvano con "Salva modifiche" o Ctrl+S, con Annulla / Ripeti. Chiudi Minecraft prima.
- **Icone sulla mappa**: nella barra della Mappa chunk attiva **"Entità"**; con **"Quali…"** scegli le categorie
  (villager, spawner, contenitori, mob, oggetti a terra, altro) oppure "Solo villager" / "Solo spawner" /
  "Solo contenitori". Le icone compaiono avvicinandosi; passandoci sopra si vedono nome e posizione, con un
  clic si apre l'editor. Dopo il salvataggio (o se il gioco cambia il mondo) si aggiornano da sole.

## Supporti per armature (armor stand)
- Trovali sulla mappa (icone viola, categoria "Supporti per armature" in "Quali…"), nell'elenco Entità o con la
  ricerca; clic per aprire l'editor. Tasto destro sulla mappa > "Piazza qui un supporto per armature" per crearne uno.
- **Anteprima 3D** con le misure e le rotazioni del modello del gioco: trascina per girare, rotella per lo zoom,
  clic su una parte per selezionarla. Disegnata con buffer di profondità (nessuna parte sparisce più girando la
  camera) e con le texture della versione scelta: legno dello stand, **armature indossate in 3D** (elmo, corazza,
  gambali, stivali; cuoio tinto), **oggetti in mano in 3D** come nel gioco (oggetti piatti estrusi, blocchi,
  scudo, tridente), blocchi e teste dei mob sulla testa, e **effetto incantesimo animato** su oggetti e armature
  incantati (o con il bagliore forzato).
- Tutte le finestre degli editor si possono **ingrandire** (pulsante massimizza) e ridimensionare.
- **Posa**: testa, busto, braccia e gambe con cursori X / Y / Z, pose pronte (saluta, cammina, corre, seduto,
  zombi, spada alzata, balla...), Specchia, Azzera.
- **Opzioni**: braccia, piccolo, senza base, invisibile, marker; **slot bloccati** per ogni pezzo
  (i giocatori non possono prendere o cambiare gli oggetti). Equipaggiamento nella scheda accanto.

## Strumenti del mondo (pagina Mappa chunk)
- **Cerca nel mondo** (Ctrl+F): oggetti ovunque (casse, inventari e mani dei mob, cornici, oggetti a terra,
  giocatori; anche per nome o incantesimo), mob ed entità, spawner e casse, **scambi dei villager**, **blocchi**
  (es. ancient_debris, contati per chunk). Dai risultati: mostra sulla mappa, modifica, seleziona i chunk.
- **Pulizia lag**: quante entità per tipo e i chunk più pesanti; rimuove oggetti a terra, sfere di esperienza,
  frecce e mob oltre un numero per chunk (mai quelli con nome, addomesticati, villager, golem...).
- **Strumenti di costruzione**: riempi o sostituisci blocchi in un'area precisa (anche con stati, es.
  `minecraft:oak_stairs[facing=east]`), copia / incolla aree, esporta e importa **file structure .nbt**.
- **Waypoint**: tasto destro sulla mappa > "Aggiungi un waypoint qui"; elenco nel riquadro per tornarci.
- **Teletrasporto**: tasto destro > "Teletrasporta qui il giocatore", oppure "Teletrasportami qui" dall'elenco entità.
- **Vista 3D**: icone delle entità anche in 3D; clic su un'icona o su un blocco (cassa, spawner...) per modificarlo.

## Oggetti e mob: comandi, modelli, libri, stendardi, negozi
- **Comando…** nell'editor oggetti (/give) e nell'editor entità (/summon, /setblock): pronto da copiare, con
  l'avviso se è troppo lungo per la chat. Nei modelli c'è anche "Incolla un comando /give".
- **Modelli…**: salva un oggetto, un mob, un villager con i suoi scambi o uno spawner e riusalo in qualsiasi mondo
  (`~/.nbt_studio/templates`). Ogni modello ha **nome, categoria e nota**, data e versione di Minecraft; nel menu
  sono raggruppati per categoria con le icone. **"Gestisci modelli…"** apre l'elenco completo: ricerca, filtro per
  categoria, anteprima dei dati, carica, rinomina / sposta, duplica, elimina, **importa / esporta** (file .snbt o
  uno .zip da condividere). Avvisa prima di sovrascrivere e quando un modello è di un'altra versione.

## Generatore di comandi (pagina "Comandi")
- Funziona **senza aprire un mondo**. Scegli la versione di Minecraft (1.8-1.12, 1.13-1.20.4, 1.20.5-1.21.4,
  1.21.5+ / 26.x): la sintassi cambia da sola. Con un mondo aperto prende la sua versione.
- **Oggetto (/give)**: parti da un oggetto e modificalo con l'editor completo (nomi con sfumature, incantesimi,
  attributi, contenuto, trim...), destinatario e quantità.
- **Mob (/summon)**: editor completo del mob (equipaggiamento, drop, effetti, attributi, scambi...), posizione,
  oppure **come uovo generatore** con il mob dentro.
- **Blocco (/setblock)**: casse con contenuto e bottino, spawner, blocchi comandi...; modo sostituisci / solo se
  vuoto / rompi, oppure **come oggetto** da piazzare che tiene il contenuto.
- **Altri comandi**: effetti (anche infiniti), teletrasporto, modalità di gioco, ora, meteo, esperienza, regole di
  gioco, rimuovi oggetti a terra, svuota inventario.
- **Copia** e **Copia come blocco comandi** (per i comandi troppo lunghi per la chat); elenco dei comandi copiati.
  Ogni sezione ha i suoi **Modelli…**.
- **Libri scritti / da scrivere**: titolo, autore, generazione e pagine con colori (codici &).
- **Stendardi e scudi**: motivi e colori con anteprima disegnata con le texture del gioco.
- **Negozi pronti** per i villager: armi, armature, cibo, blocchi, libri incantati, oggetti rari, attrezzi
  (sostituisci o aggiungi; professione, livello 5 e usi illimitati).

## Giocatore: respawn, progressi, statistiche
- Punto di **respawn** (letto) modificabile o rimovibile.
- **Progressi e statistiche**: tutti i progressi del gioco con nomi italiani, sblocca / blocca singoli o tutti;
  statistiche modificabili (tempo di gioco in ore, blocchi scavati, mob uccisi...).

## Sicurezza e backup
- Avviso se **Minecraft (o un server) sta usando il mondo** prima di salvare o modificare chunk.
- **Backup automatico** prima del primo salvataggio di ogni sessione, tenendo gli ultimi N (Impostazioni).
- **Backup e ripristino** (Home > Backup... o menu File): ripristina un backup come nuovo mondo (non sovrascrive
  nulla) e **confronta** due backup, o un backup con il mondo attuale: impostazioni, inventari, chunk cambiati.

## Terreno e 3D
- **Terreno**: legge i blocchi veri dai chunk (formati 1.8-1.12, 1.13-1.17 e 1.18 fino alla 26.x). La prima volta
  ogni region viene decodificata in background (in parallelo su piu processi); poi resta in cache in
  `~/.nbt_studio/tiles`, quindi la seconda apertura e immediata.
- **Rilievo e ombre**: luce da nord-ovest, ombre proiettate da montagne, alberi e costruzioni. Slider "Relief"
  e caselle "Shadows", "Height shading", "Block textures".
- **Grotte**: taglio orizzontale all'altezza scelta; la roccia e scura, i vuoti mostrano il pavimento della grotta.
- Vetro e pannelli sono trasparenti sulla mappa e da vicino pannelli, recinzioni e muretti sono disegnati come linee collegate.
- **3D**: seleziona dei chunk e premi "3D view"; senza selezione mostra **esattamente la zona inquadrata nella
  mappa** (fino a 768x768 blocchi: se inquadri di piu usa il centro, avvicinati per vederla tutta).
  Q / E ruotano, rotella zoom (fino a 512 pixel per blocco, verso il punto sotto il mouse), trascina per spostare,
  F adatta alla finestra. Viene disegnata solo la parte visibile, quindi anche aree grandi restano fluide.
  Pannelli di vetro, sbarre, recinzioni, muretti e lastre hanno la loro forma, collegati ai blocchi vicini. "Cut at height" taglia tutto sopra un'altezza per vedere
  dentro grotte e edifici; "Depth below surface" regola quanta roccia mostrare sotto il terreno.
- **Sole, notte e caverne (3D)**: cursori della **direzione** e dell'**altezza del sole** (ombre lunghe col sole
  basso; "Sole predefinito" torna all'aspetto classico). **Notte**: luce lunare azzurra, illuminano solo torce,
  lanterne, lava, pietra luminosa, lampade e candele accese, fornaci attive, froglight, lanterne marine...
  **Caverne buie**: anche di giorno grotte e stanze chiuse ricevono solo la luce che ci arriva. La luce si propaga
  blocco per blocco come nel gioco (livelli 0-15, cielo e blocchi luminosi, le foglie la lasciano passare) e
  viene calcolata sull'area intera, quindi con "Taglia all'altezza" le stanze aperte dal taglio restano col
  loro buio e le loro torce.
- **Immagini in alta definizione (2D e 3D)**: "Salva immagine" chiede la risoluzione (dimensione della finestra,
  Full HD, 2K, 4K, **8K** o personalizzata fino a 7680 px) e salva in PNG o JPG. Nel 3D puoi salvare quello che
  vedi o tutta l'area, anche con sfondo trasparente; l'immagine viene disegnata a pezzi direttamente alla
  risoluzione scelta (poca memoria). Nella mappa 2D il terreno viene ridisegnato al dettaglio dell'immagine
  (con le texture dei blocchi), con a scelta icone delle entità e waypoint, griglia e chunk selezionati.
- **Memoria**: aree 3D grandi leggono solo la roccia che serve sotto il terreno (anche sotto le scogliere, senza
  buchi) e preparano le facce a strisce; se la memoria non basta compare un messaggio invece di un crash.
  Anche il disegno del 3D procede a riquadri, quindi lo zoom (fino a 512 pixel per blocco) resta nei limiti di RAM.
- **Impostazioni senza tetti**: in "Memoria e prestazioni" i valori (region e chunk in memoria, processi della
  mappa, zona 3D, roccia sotto il terreno, limite RAM) non hanno più massimi bassi: per valori molto grandi
  compare solo un avviso arancione con la memoria stimata. Con il profilo "Personalizzato" vengono usati tanti
  processi quanti ne scegli; con un limite RAM le cache della mappa si riducono comunque per non esaurirlo
  (l'avviso dice quante ne vengono tenute). Anche le foto vanno oltre 8K (16K o qualsiasi misura) con un avviso.
- **Foto enormi**: in PNG l'immagine viene disegnata e scritta nel file a strisce, quindi anche 16K e oltre
  funzionano con poca memoria (16K della mappa in circa 20 s restando sotto 1 GB). Il JPG invece deve stare
  intero in memoria: per immagini molto grandi conviene il PNG.
- Le tinte di erba, foglie e acqua seguono il bioma. Senza una versione di Minecraft selezionata si usano colori di riserva.

## Texture e teste dei giocatori
- **Texture**: nessuna texture di Mojang e inclusa. Vengono lette dai `.jar` gia installati in
  `.minecraft/versions/<versione>/` (1.8.9 ... 26.x, basta averle avviate una volta). Scegli la versione nella pagina Player.
- **Teste**: scaricate dal server pubblico di Mojang (serve internet) e salvate in `~/.nbt_studio/heads`.
- **Teste di giocatore (oggetti)**: NBT Studio riconosce di chi e la testa (`minecraft:profile` o il vecchio
  `SkullOwner`: nome, UUID o skin in base64 dei siti di teste) e la mostra con la **sua faccia** nelle icone,
  nell'editor oggetti e sul supporto per armature in 3D; il nome diventa "Testa di <giocatore>" come nel gioco e
  il tooltip dice di chi e la skin. Le skin si scaricano in sottofondo (solo da `textures.minecraft.net` /
  Mojang / GeyserMC) e restano in `~/.nbt_studio/heads/textures`.
- **Backup**: File > Backup world crea uno zip in `~/NBT Studio backups`.

## Sicurezza
- **Chiudi Minecraft** prima di salvare, potare o modificare chunk, e fai un backup del mondo.
- Al primo salvataggio di un file viene creata una copia `.bak`. Le modifiche ai singoli chunk riscrivono il file region: usa il backup.
- La potatura e definitiva.

## Mondi 26.x
Dalla 26.x Minecraft ha spostato molti dati fuori da `level.dat`; NBT Studio li legge e li modifica dove si trovano:
- giocatore in `players/data/<uuid>.dat` (riconosciuto come "Singleplayer player" grazie a `singleplayer_uuid`)
- difficolta e hardcore in `difficulty_settings`, ora del giorno in `data/minecraft/world_clocks.dat`,
  meteo in `weather.dat`, game rules in `game_rules.dat`, seed in `world_gen_settings.dat`
- world border in `dimensions/minecraft/overworld/data/minecraft/world_border.dat`
- l'export della selezione come nuovo mondo copia anche le cartelle `data` (seed, tipo di mondo, game rules)

## Limiti attuali
- Solo mondi Java (formato Anvil). Bedrock: apri `level.dat` nell'NBT Editor; mappa e pruner non funzionano.
- Chunk con compressione LZ4 (mondi piu recenti) non sono leggibili dalla scansione e dall'editor di chunk.
- Nessun convertitore di mondi tra edizioni.
- Nella vista 3D scale, porte e cancelli sono disegnati come cubi interi e le lastre sempre nella meta bassa
  (lo stato dei blocchi non viene letto); i liquidi hanno sempre altezza piena.
- Le tessere in cache non si cancellano da sole: se occupano troppo spazio svuota `~/.nbt_studio/tiles`.

## Test
    python test_nbtcore.py
    python test_anvil.py
    python test_extras.py
    python test_more.py
    python test_terrain.py
