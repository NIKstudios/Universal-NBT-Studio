# Universal NBT Studio

**Il modo più semplice per modificare i tuoi mondi di Minecraft Java.**
Giocatori, oggetti, mob, mappe, costruzioni, comandi e resource pack: tutto con i pulsanti, senza scrivere comandi
e senza conoscere i file del gioco.

## Perché è nato Universal NBT Studio

**Universal NBT Studio** non è nato per essere l'ennesimo e classico NBT editor, ma a differenza di classici NBT
editor questo vuole **semplificare il lavoro**: mettere in un solo programma tutto quello che di solito è sparso
tra decine di siti e generatori online (come mc-tools e simili), e farlo funzionare **sul tuo PC**.

Niente siti da aprire, niente file da caricare su server di altri, niente attese: i tuoi mondi, le tue skin, la
tua musica e le tue immagini restano tuoi, sul tuo computer. Internet serve solo per le cose che non si possono
fare altrimenti, come scaricare le skin dei giocatori e controllare se c'è un aggiornamento.

Per ora il codice non è open source, ma lo diventerà quando il progetto avrà raggiunto una buona fase di sviluppo.

> Funziona su **Windows**, con i mondi di **Minecraft Java Edition** dalla 1.8 alla 26.x.
> Non serve installare nulla: scarichi `NBTStudio.exe` e lo apri.

---

## Indice
- [Novità della versione 1.0.3](#novità-della-versione-103)
- [Novità della versione 1.0.2](#novità-della-versione-102)
- [Scaricare e aprire](#scaricare-e-aprire)
- [Il primo avvio](#il-primo-avvio)
- [Come è fatto il programma](#come-è-fatto-il-programma)
- [Cosa puoi fare](#cosa-puoi-fare)
- [Pack Studio: resource pack in un clic](#pack-studio-resource-pack-in-un-clic)
- [Sicurezza dei tuoi mondi](#sicurezza-dei-tuoi-mondi)
- [Aggiornamenti](#aggiornamenti)
- [Domande frequenti](#domande-frequenti)
- [Contatti e crediti](#contatti-e-crediti)

---

## Novità della versione 1.0.3
- **3D libero con la scheda video**: cammini e ti giri liberamente nell'area, fluido anche con milioni di blocchi.
- **Avvio molto più veloce**: da circa 30 secondi a pochi secondi anche con tante versioni di Minecraft installate.
- **/give anche per mob, entità e blocchi**: nella finestra "Comando…" un mob diventa un uovo con tutti i suoi
  dati, un armor stand o una cornice diventano il loro oggetto, e bauli e spawner tengono il contenuto.
- **Modalità di gioco sistemata**: quella scelta per un giocatore ora funziona davvero quando entri nel mondo
  (volo e costruzione istantanea compresi).
- **3D**: tronchi di ciliegio e bambù della 26.x con le facce giuste, tronchi orizzontali con gli anelli solo
  alle estremità, e sul lato dell'erba si colora solo la frangia, non la terra.

## Novità della versione 1.0.2
Le cose principali (l'elenco completo è nel programma, in **✨ Novità**):

**Strumenti del mondo** (nella Mappa chunk)
- **Ripristino da backup per zona**: rimetti solo i chunk che selezioni come erano in un backup (la base fatta
  saltare da un creeper torna com'era), il resto del mondo resta com'è.
- **Riparazione dei file regione**: trova i chunk danneggiati, quelli che fanno crashare il gioco o spariscono, e
  li sistema.
- **Mappa dei minerali**: i chunk colorati in base a quanti diamanti, detriti antichi, ferro o spawner hanno.
- **Strutture**: villaggi, roccaforti, città antiche, camere della prova, monumenti... con la posizione e il
  teletrasporto.
- **Modifica di gruppo**: una modifica a tutti i mob, bauli, cartelli, spawner o oggetti che corrispondono (il mob
  di tutti gli spawner, una parola su tutti i cartelli, un oggetto in ogni baule...).
- **Confronto tra file NBT** e **oggetti convertiti tra versioni** (kit, modelli e /give per un'altra versione).

**Creazione mappe (Beta)**: catene di blocchi comandi, checkpoint, zone che attivano comandi, timer, dialoghi con
gli NPC e oggetti con poteri, con i datapack installati in un clic.

**Costruzioni**
- 10 nuovi generatori: parkour, dungeon, montagne russe, città, statue dalla skin, testo 3D, isole volanti,
  vulcani, arene per minigiochi e canzoni con i blocchi nota da file MIDI.
- Città con 6 stili diversi e colori a scelta; dungeon con i mob che vuoi, boss e stanze speciali.
- Isole volanti con 7 forme e 7 aspetti, minerali, caverne, spawner, bauli e ponti; ricevono un bioma così i
  mob ci appaiono anche in un mondo vuoto.
- **Senza limiti** in ogni generatore: città e forme enormi fatte e messe a pezzi, con Interrompi e Annulla.
- Annulla l'ultima costruzione (anche enorme), gira l'anteprima 3D, porta il giocatore alla costruzione.

**Spawner e mob**: spawner con più mob e qualsiasi luce, mob personalizzati, **torri di mob** e "I miei mob" come
modelli.

**Grafica e interfaccia**
- 3D più fedele al gioco: pulsanti, teste, letti, scale, porte, cartelli, stendardi, bauli e altro hanno la loro
  forma; tutti i blocchi della 26.x hanno la texture; più mob mostrano la faccia.
- Testo più grande o più piccolo con Ctrl + e Ctrl -, zoom di tutta l'interfaccia, grafica rinnovata.
- Le finestre stanno sempre nello schermo, sopra la barra di Windows.

---

## Scaricare e aprire
1. Scarica **`NBTStudio.exe`** dalla pagina **Releases** (l'ultima versione è sempre in cima).
2. Mettilo dove vuoi (Desktop, Documenti...) e fai **doppio clic**.
3. La prima volta Windows potrebbe mostrare un avviso blu ("Windows ha protetto il PC"): è normale per i programmi
   nuovi. Clicca **Ulteriori informazioni** e poi **Esegui comunque**.

L'avvio può richiedere qualche secondo: il programma è tutto in un unico file.

## Il primo avvio
Alla prima apertura una breve configurazione ti chiede:
- **la lingua**: viene già scelta quella di Windows (italiano o inglese), puoi cambiarla;
- **l'aspetto**: tema scuro o chiaro, grandezza del testo e la **modalità semplice**, che nasconde le pagine per
  esperti;
- **i tuoi giochi**: il programma mostra da solo i Minecraft che trova sul PC (launcher ufficiale, CurseForge,
  Prism, Modrinth, TLauncher, Lunar, Feather e altri);
- **la sicurezza**: se fare un backup automatico dei mondi (consigliato).

Poi un piccolo **tour** ti mostra dove sono le cose. Puoi rivederlo quando vuoi dalle Impostazioni.

## Come è fatto il programma
- A sinistra c'è il **menu**, diviso in sezioni: **Mondo**, **Giocatori**, **Editor**, **Generatori**,
  **Resource pack** e **Analisi**.
- Sopra il menu c'è la **ricerca**: scrivi cosa vuoi fare (per esempio *cucciolo*, *diamanti*, *totem*,
  *labirinto*) e ti porta nel posto giusto.
- In ogni pagina una **guida a passi** in alto spiega cosa fare, in ordine.
- Le **Impostazioni** sono in fondo al menu e nell'ingranaggio ⚙ in alto a destra.
- **Ctrl+S** salva, **Ctrl+Z** annulla, **Ctrl+Y** ripete.
- **Ctrl +** e **Ctrl -** ingrandiscono o rimpiccioliscono il testo, **Ctrl 0** lo riporta normale. Nelle
  Impostazioni c'è anche lo **zoom di tutta l'interfaccia** (icone e pulsanti compresi).
- **✨ Novità**, sopra le Impostazioni, mostra cosa è cambiato in ogni versione (si apre da sola dopo un
  aggiornamento). **Aiuto › Segnala un problema** prepara il testo da incollare sul Discord.

## Cosa puoi fare

### Il mondo
- **Aprire un mondo**: dalla Home vedi i mondi del gioco con la loro icona, oppure trascini la cartella sulla
  finestra.
- **Impostazioni del mondo**: nome, modalità, difficoltà, hardcore, trucchi, ora, meteo, spawn, confine del mondo
  e tutte le regole di gioco.
- **Mappa del mondo**: il terreno vero visto dall'alto, con texture, rilievo, ombre, acqua e una vista delle
  **grotte**. Mostra villaggi, strutture, chunk degli slime, villici, spawner e bauli.
- **Vista 3D**: qualsiasi zona in 3D, con il sole che puoi spostare, la **notte** con le luci accese e foto in
  altissima risoluzione (fino a 16K) o piccoli video.
- **3D libero (scheda video)**: dalla vista 3D apri la stessa zona in una vista dove cammini e ti giri
  liberamente come in Minecraft (clic per guardarti intorno col mouse, Esc per il cursore, W A S D per
  muoverti), fluida anche con aree enormi.
- **Strumenti sulla mappa**: pennello per dipingere blocchi e **biomi**, copia, incolla e sposta pezzi di mondo
  (anche tra mondi diversi), sostituisci blocchi, cancella i chunk da rigenerare, **pulizia del lag**, **cerca**
  oggetti, mob e blocchi in tutto il mondo, segnaposti.
- **Ripristino da backup per zona**: selezioni i chunk sulla mappa e li rimetti come sono in un backup, senza
  toccare il resto del mondo.
- **Ripara i file regione**: trova e sistema i chunk danneggiati o salvati nel posto sbagliato.
- **Mappa dei minerali**: i chunk colorati in base a quanti diamanti, detriti antichi, ferro, spawner... hanno tra
  due altezze.
- **Strutture**: l'elenco di quelle davvero generate, le più vicine per prime, con "Mostra sulla mappa" e
  "Porta il giocatore lì".
- **Modifica di gruppo**: una modifica a tutto quello che corrisponde (mob, bauli, cartelli, spawner, oggetti),
  prima mostrata e poi applicata.
- **Confronta due file NBT**: ogni valore aggiunto, tolto o cambiato (anche tra il file aperto e un backup).
- **Datapack**: attivali, disattivali, aggiungili o toglili.
- **Statistiche**: quanti minerali, blocchi e mob ci sono, con la mappa dei diamanti.

### Giocatori e oggetti
- **Giocatore**: vita, fame, esperienza, posizione, volo e permessi, inventario ed **ender chest** con le icone
  del gioco. Trascini gli oggetti tra gli slot come in Minecraft.
- **Editor degli oggetti**: nome e descrizione colorati (anche con sfumature), incantesimi, durabilità, colori,
  finiture delle armature, teste dei giocatori con la loro faccia, libri, stendardi, contenuto di bauli e shulker,
  blocchi comandi e cartelli.
- **Poteri del giocatore**: con dei cursori cambi vita massima, velocità, **dimensione**, salto, portata e altro.
  Ci sono preset pronti: *Gigante*, *Minuscolo*, *Super velocità*, *Corazzato*, *Salto lunare*.
- **Trasferisci oggetti**: dai oggetti da un giocatore a un altro (copia, sposta o scambia), con i due inventari
  disegnati come nel gioco. I **kit** salvano un gruppo di oggetti da ridare a chiunque, anche in altri mondi:
  se il mondo è di un'altra versione, gli oggetti vengono convertiti da soli.
- **Progressi e statistiche** del giocatore.

### Mob ed entità
- Modifica qualsiasi mob: nome, vita, **cucciolo**, **immortale**, bagliore colorato, equipaggiamento, effetti,
  attributi, scambi dei villici.
- **Supporti per armature** messi in posa con un manichino.
- **Villaggi**: villici, scambi, ripristino delle offerte e incursioni.

### Generatori
- **Costruzioni**, con anteprima 3D prima di metterle nel mondo:
  - **pixel art** da un'immagine;
  - **forme**: sfera, cupola, cilindro, cono, piramide, anello, arco;
  - **strade** che seguono il terreno, con ponti e lampioni;
  - **alberi e foreste**;
  - **labirinti** e **arene** con gradinate;
  - **parkour** con salti sempre possibili, checkpoint e arrivo, in 4 difficoltà;
  - **dungeon** con stanze, corridoi, spawner e bauli con il bottino del gioco;
  - **montagne russe** con salite e binari elettrificati, pronte per il carrello;
  - **città** con strade, marciapiedi, palazzi, parchi e lampioni;
  - **statue** gigantesche dalla skin di un giocatore (braccia slim riconosciute, secondo strato in rilievo,
    colori realistici, ruotabili o sdraiate) e **testo 3D** con il font di Minecraft;
  - **isole volanti** con alberi e cascate, e **vulcani** con cratere e colate di lava;
  - **arene per minigiochi**: spleef, bow spleef, sumo e survival games;
  - **canzoni con i blocchi nota** da un file MIDI, che suonano premendo un pulsante.

  Il posto lo scegli **cliccando sulla mappa** (📍 *Scegli sulla mappa*): niente coordinate da scrivere.
  Dopo averla piazzata puoi **annullare l'ultima costruzione** e **portare il giocatore lì**; l'anteprima 3D si
  gira con il pulsante ⟳. Ogni costruzione si può anche **salvare come schematic** (.schem per WorldEdit, .litematic per Litematica,
  .nbt per i blocchi struttura).
- **Comandi pronti** per la versione che usi: fuochi d'artificio con anteprima animata, pozioni con il loro
  colore e il tooltip come nel gioco, messaggi colorati in chat e titoli, teste personalizzate, `/execute` passo
  per passo, `/give` e `/summon` di qualsiasi oggetto o mob.
- **Spawner personalizzati**: più mob nello stesso spawner, ognuno con la sua probabilità, che possono comparire
  anche con la luce. Ogni mob ha nome colorato, cucciolo, bagliore, vita, dimensione, velocità, equipaggiamento
  ed effetti.
- **Torri di mob**: mob uno sopra l'altro (fantini, totem di animali, boss con le guardie), ognuno
  personalizzato, da evocare con `/summon` o con un uovo che fa nascere tutta la torre.
- **I miei mob**: salvi un mob o una torre come modello e lo riusi quando vuoi, nello spawner o nelle torri.
- **Datapack**: ricette, drop dei mob e dei blocchi, **bauli con bottino casuale**, progressi e funzioni,
  messi direttamente nel mondo.
- **Mondi superpiatti**: scegli gli strati e il bioma, e il nuovo mondo compare nella lista del gioco.
- **Mappe del gioco**: trasforma un'immagine in mappe da appendere nelle cornici.
- **Scoreboard e squadre**: obiettivi, punteggi, squadre e barre dei boss.

## Creazione mappe (strumenti per chi fa mappe con i comandi)
Nel menu **Generatori › Creazione mappe**, con i comandi scritti nella sintassi della tua versione:
- **Catene di blocchi comandi**: scrivi i comandi uno per riga (con `?` per quelli condizionali) e la catena
  viene piazzata nel mondo dove scegli sulla mappa, con un pulsante per farla partire, o salvata come .schem.
- **Checkpoint**: una pedana d'oro che imposta il punto di respawn, con messaggio, suono e cura.
- **Zone che attivano comandi**: quando un giocatore entra in un'area (una volta, ogni volta, sempre o solo il
  primo) partono i tuoi comandi.
- **Timer con conto alla rovescia**: boss bar, secondi sopra la barra rapida, comandi all'inizio e alla fine.
- **Dialoghi con gli NPC**: un personaggio che parla quando ti avvicini, con risposte da cliccare in chat che
  fanno partire comandi (non serve essere operatore).
- **Oggetti con poteri**: un oggetto che col tasto destro fa uno scatto, un salto, un fulmine, un'esplosione, un
  teletrasporto o i tuoi comandi, con l'attesa tra un uso e l'altro.

Le ultime quattro diventano un **datapack** che si installa nel mondo aperto con un clic (poi `/reload`).

## Pack Studio: resource pack in un clic
Nella sezione **Resource pack**: lo crei, clicchi **🎮 Importa nel gioco** e giochi. Niente file zip da
spostare e niente cartelle da cercare.

- **Crea totem**: il totem dell'immortalità con la tua skin (basta il nome del giocatore).
- **Crea dischi musicali**: metti la tua musica su un disco (MP3, WAV, FLAC o OGG), con il nome della canzone e
  il colore dell'etichetta.
- **Quadri personalizzati**: le tue immagini sui quadri del gioco.
- **Emoji personalizzate**: immagini da usare in chat.
- **Crea avatar**: immagine profilo dalla tua skin per Discord o YouTube.
- **Unisci pack**: più resource pack in uno.
- **Pack installati**: vedi, attiva, disattiva o togli i pack.
- **Codici colore** e **Coordinate** tra Overworld e Nether.

Il programma **riconosce i launcher** che hai (ufficiale, CurseForge, Prism, Modrinth, TLauncher, Lunar, Feather
e altri), con le loro icone, e ti propone per primo quello in cui hai giocato per ultimo. Il pack viene fatto
nel formato giusto per la versione di quell'istanza.

## Sicurezza dei tuoi mondi
- **Chiudi Minecraft** prima di salvare le modifiche a un mondo.
- Prima del primo salvataggio NBT Studio fa da solo una **copia di sicurezza** del mondo. Le copie le trovi
  nella Home (pulsante *Backup*) e puoi ripristinarle o confrontarle quando vuoi.
- **Ctrl+Z** annulla qualsiasi modifica prima di salvare.
- Alcune operazioni, come cancellare dei chunk, non si possono annullare dopo il salvataggio: il programma lo
  chiede sempre prima.

## Aggiornamenti
All'avvio NBT Studio controlla se c'è una nuova versione. Se c'è, ti chiede se vuoi aggiornare: si scarica,
si sostituisce e si riapre da solo. Puoi spegnere il controllo, o farlo quando vuoi, in **Impostazioni >
Aggiornamenti**.

## Domande frequenti
**Le texture e i nomi degli oggetti non si vedono.**
NBT Studio prende texture e nomi dal Minecraft installato sul tuo PC (non contiene file di Mojang). Apri almeno
una volta nel launcher la versione a cui giochi; in Impostazioni puoi scegliere quale versione usare.

**Funziona con i mondi dei server?**
Sì, se hai la cartella del mondo (per esempio scaricata dal pannello del server). Fermala o chiudi il server
prima di salvare.

**Funziona con Bedrock (telefono, console, Windows Edition)?**
No, solo con Minecraft Java Edition.

**Dove vengono salvate le impostazioni?**
Nella cartella `.nbt_studio` del tuo utente di Windows. Cancellandola il programma riparte come la prima volta.

**Qualcosa non va.**
Se compare un errore, il programma salva i dettagli in un file e te lo mostra: mandalo sul server Discord e lo
sistemiamo.

## Contatti e crediti
- **Discord** di NBT Studio e **GitHub** di NIKstudios: i pulsanti sono in basso a sinistra nel programma.
- L'editor dei supporti per armature si ispira a
  [Minecraft-ArmorStand](https://github.com/haselkern/Minecraft-ArmorStand) di haselkern.
- Gli strumenti di Pack Studio si ispirano a [mc-tools.net](https://mc-tools.net/).
- Le statue dalla skin si ispirano a [PlayerStatueBuilder](https://github.com/SkyTechBytes/PlayerStatueBuilder) di
  SkyTechBytes (colori in LAB, vetro colorato per i pixel trasparenti). Il suo codice è sotto licenza GPL-3.0 e
  non è incluso: in NBT Studio le idee sono state scritte da zero.

---

© NIKstudios. Tutti i diritti riservati. NBT Studio è distribuito gratuitamente solo come programma (`.exe`);
il codice sorgente non è pubblico.

NBT Studio non è un prodotto ufficiale di Minecraft e non è approvato né collegato a Mojang o Microsoft.
Minecraft è un marchio di Mojang AB.
