# NBT Studio 1.0

World editor per Minecraft Java con interfaccia a pagine.

| Pagina | Cosa fa |
|---|---|
| **Home** | Mondi della cartella saves e aperti di recente, con icona, ricerca e doppio clic per aprirli |
| **World Settings** | Nome, modalita, difficolta, hardcore, cheat, ora, meteo, spawn, **world border**, game rules, info sul mondo |
| **Player** | Testa e nome, vita, fame, XP, posizione, **permessi (volo, invulnerabile...)**, inventario e **ender chest** con icone 3D come nel gioco; **trascina gli oggetti** tra gli slot o dalla palette di tutti gli oggetti; **editor oggetto** con nome e lore colorati (**gradienti**, grassetto, corsivo...), **incantesimi**, durabilita, indistruttibile, colore del cuoio, piu l'editor NBT completo |
| **Chunk Map** | **Viste Chunks / Terreno / Grotte**: il terreno vero visto dall'alto con texture, rilievo, ombre e profondita dell'acqua; zoomando si vedono le texture dei singoli blocchi; vista **Grotte** a un'altezza scelta; **vista 3D isometrica** della selezione; salvataggio immagine della mappa. Inoltre: | Mappa con zoom/pan e selezione; selezione per distanza, attivita o chunk non finiti; **mappa di calore**; **doppio clic su un chunk per modificarne l'NBT**; potatura; **compattazione**; **esporta la selezione come nuovo mondo** |
| **NBT Editor** | Albero NBT con filtro; **modifica come testo SNBT**; esporta in SNBT; **salva una copia in altro formato** (Java gzip/zlib/non compresso, Bedrock) |

In piu: **Annulla/Ripeti** (Ctrl+Z / Ctrl+Y) su tutte le modifiche, backup zip del mondo, backup automatico `.bak`.

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
  Q / E ruotano, rotella zoom (fino a 192 pixel per blocco, verso il punto sotto il mouse), trascina per spostare,
  F adatta alla finestra. Viene disegnata solo la parte visibile, quindi anche aree grandi restano fluide.
  Pannelli di vetro, sbarre, recinzioni, muretti e lastre hanno la loro forma, collegati ai blocchi vicini. "Cut at height" taglia tutto sopra un'altezza per vedere
  dentro grotte e edifici; "Depth below surface" regola quanta roccia mostrare sotto il terreno. "Save image" salva un PNG.
- Le tinte di erba, foglie e acqua seguono il bioma. Senza una versione di Minecraft selezionata si usano colori di riserva.

## Texture e teste dei giocatori
- **Texture**: nessuna texture di Mojang e inclusa. Vengono lette dai `.jar` gia installati in
  `.minecraft/versions/<versione>/` (1.8.9 ... 26.x, basta averle avviate una volta). Scegli la versione nella pagina Player.
- **Teste**: scaricate dal server pubblico di Mojang (serve internet) e salvate in `~/.nbt_studio/heads`.
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
