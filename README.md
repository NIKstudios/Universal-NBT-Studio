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
- [Novità](#novità)
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

<!-- novita:inizio (scritto da make_changelog.py) -->
## Novità

Tutte le novità di ogni versione, come nella finestra **Novità** del programma. <img src="https://img.shields.io/badge/-Nuovo-4f7cff?style=flat-square" alt="Nuovo" height="18"> cose nuove, <img src="https://img.shields.io/badge/-Migliorato-d9831f?style=flat-square" alt="Migliorato" height="18"> cose migliorate, <img src="https://img.shields.io/badge/-Correzione-2e9e5b?style=flat-square" alt="Correzione" height="18"> problemi corretti.

<details open>
<summary><b>Versione 1.0.7</b></summary>


**Oggetti e inventario**

- <img src="https://img.shields.io/badge/-Nuovo-4f7cff?style=flat-square" alt="Nuovo" height="18"> Metti nell'inventario: pozioni, fuochi d'artificio, teste e gli altri oggetti dei generatori finiscono direttamente nell'inventario di un giocatore, senza /give. Nell'editor dell'inventario l'oggetto nuovo si illumina per un momento, con il colore del tema. Anche per le mappe.
- <img src="https://img.shields.io/badge/-Nuovo-4f7cff?style=flat-square" alt="Nuovo" height="18"> Editor oggetti: scheda Pozione (base, colore, effetti in più) e scheda Altro (rarità, quantità per slot, resistenza al fuoco, descrizione, custom model data).
- <img src="https://img.shields.io/badge/-Nuovo-4f7cff?style=flat-square" alt="Nuovo" height="18"> Supporti per armature, cornici e quadri come oggetti tengono i loro dati: posa, armatura, oggetto nella cornice... e quando li piazzi escono così.
- <img src="https://img.shields.io/badge/-Nuovo-4f7cff?style=flat-square" alt="Nuovo" height="18"> Poteri del giocatore rifatti: preset in schede con cosa fanno (anche Costruttore, Minatore, Sub, Ninja e Guerriero), i tuoi preset salvati con un nome, i poteri divisi in gruppi e quelli cambiati in evidenza.
- <img src="https://img.shields.io/badge/-Nuovo-4f7cff?style=flat-square" alt="Nuovo" height="18"> Conversione: arriva anche il tuo giocatore, con inventario, armatura, mano secondaria, cassa dell'End, livello, vita, fame e posizione. Verso Java va all'account Java di questo computer.
- <img src="https://img.shields.io/badge/-Nuovo-4f7cff?style=flat-square" alt="Nuovo" height="18"> Scelta dei blocchi: la lista ha una barra di ricerca e tutti i blocchi del gioco, che trovi per nome italiano o inglese, per id o con parole di tutti i giorni (cemento, legno, scale...).
- <img src="https://img.shields.io/badge/-Correzione-2e9e5b?style=flat-square" alt="Correzione" height="18"> Liste dei blocchi: l'icona segue il blocco scritto a mano e non cambia più colore sulla riga scelta.
- <img src="https://img.shields.io/badge/-Nuovo-4f7cff?style=flat-square" alt="Nuovo" height="18"> Alberi e foreste rifatti: 23 alberi (quercia grande, abete gigante, giungla con liane, mangrovia, salice, palma, albero millenario, funghi giganti, funghi del Nether, alberi luminosi e di cristallo...), 15 foreste come i biomi, erba, fiori, tronchi caduti e il terreno sotto gli alberi.
- <img src="https://img.shields.io/badge/-Correzione-2e9e5b?style=flat-square" alt="Correzione" height="18"> Villaggi: le strade non si spezzano più sopra il vuoto o sul terreno irregolare, e le case sopra il vuoto restano all'altezza del villaggio.
- <img src="https://img.shields.io/badge/-Migliorato-d9831f?style=flat-square" alt="Migliorato" height="18"> Il pulsante che riporta un numero al suo valore è ridisegnato: tondo, col colore del tema, un po' staccato dalle frecce.
- <img src="https://img.shields.io/badge/-Nuovo-4f7cff?style=flat-square" alt="Nuovo" height="18"> Attività di Discord: due pulsanti, per scaricare NBT Studio ed entrare nel server Discord, e la versione del programma.
- <img src="https://img.shields.io/badge/-Nuovo-4f7cff?style=flat-square" alt="Nuovo" height="18"> Mappe in gioco: col tasto destro elimini le mappe (anche più insieme). I file finiscono in una cartella del programma, così si possono rimettere.
- <img src="https://img.shields.io/badge/-Correzione-2e9e5b?style=flat-square" alt="Correzione" height="18"> Elimina tutte quelle mostrate: spiega perché alcune entità restano (con nome, addomesticate, villici dei villaggi...) e può eliminarle lo stesso.

</details>

<details>
<summary><b>Versione 1.0.6</b></summary>


**Conversione**

- <img src="https://img.shields.io/badge/-Nuovo-4f7cff?style=flat-square" alt="Nuovo" height="18"> Il programma trova da solo le cartelle di Java e Bedrock: ogni launcher e ogni account Bedrock, con la lista Salva in per scegliere dove va il nuovo mondo.
- <img src="https://img.shields.io/badge/-Migliorato-d9831f?style=flat-square" alt="Migliorato" height="18"> Un mondo Bedrock può finire direttamente tra i tuoi mondi, senza importarlo. Nell'elenco ci sono tutti i mondi Java, non solo quello aperto.
- <img src="https://img.shields.io/badge/-Migliorato-d9831f?style=flat-square" alt="Migliorato" height="18"> Un mondo convertito non sostituisce mai uno già esistente.
- <img src="https://img.shields.io/badge/-Migliorato-d9831f?style=flat-square" alt="Migliorato" height="18"> Nuova schermata per scegliere il mondo: immagini, dove si trova, modalità, ultima partita e ricerca.
- <img src="https://img.shields.io/badge/-Correzione-2e9e5b?style=flat-square" alt="Correzione" height="18"> Da Bedrock a Java: recinzioni, vetri, redstone, scale, porte e neve sull'erba escono come in Java, ricostruiti dai blocchi vicini.
- <img src="https://img.shields.io/badge/-Correzione-2e9e5b?style=flat-square" alt="Correzione" height="18"> Mondi 26.3: i blocchi con proprietà venivano letti come aria da conversione, mappa, vista 3D ed editor.
- <img src="https://img.shields.io/badge/-Correzione-2e9e5b?style=flat-square" alt="Correzione" height="18"> I mondi protetti del Marketplace vengono riconosciuti: non si possono convertire e non nasce un mondo rotto.

</details>

<details>
<summary><b>Versione 1.0.5 (Beta finale)</b></summary>


**Beta finale**

- <img src="https://img.shields.io/badge/-Nuovo-4f7cff?style=flat-square" alt="Nuovo" height="18"> Villaggi: tutte le case che vuoi, della grandezza che vuoi, in 10 stili, con strade, fattorie, chiesa e villici veri. E cose pazze: case volanti, sottosopra, fungo, arcobaleno e giganti.
- <img src="https://img.shields.io/badge/-Nuovo-4f7cff?style=flat-square" alt="Nuovo" height="18"> Castelli e torri: mura, mastio, fossato, ponte e bandiere in 8 stili, torri singole e del mago, anche in rovina, sospesi o sottosopra.
- <img src="https://img.shields.io/badge/-Nuovo-4f7cff?style=flat-square" alt="Nuovo" height="18"> Copia e incolla 3D: un'area girata, specchiata o sottosopra, con bauli e mob, dove vuoi, anche in un altro mondo.
- <img src="https://img.shields.io/badge/-Nuovo-4f7cff?style=flat-square" alt="Nuovo" height="18"> Trova e sostituisci con anteprima 3D, nei chunk selezionati o in un file schematica.
- <img src="https://img.shields.io/badge/-Correzione-2e9e5b?style=flat-square" alt="Correzione" height="18"> Villaggi: strade e lampioni non finiscono più dentro le case, anche con tante case o case molto grandi.
- <img src="https://img.shields.io/badge/-Correzione-2e9e5b?style=flat-square" alt="Correzione" height="18"> Villaggi: case e tetti rifatti, con le proporzioni giuste a ogni grandezza (le case alte sono anche larghe, quelle giganti sono davvero più grandi e non stirate) e strade ordinate in ogni disposizione.
- <img src="https://img.shields.io/badge/-Correzione-2e9e5b?style=flat-square" alt="Correzione" height="18"> Costruzioni: con Senza limiti spento i massimi sono più bassi e non si sfora più. Con Senza limiti acceso non c'è più un tetto fisso: il limite è la memoria del computer.
- <img src="https://img.shields.io/badge/-Correzione-2e9e5b?style=flat-square" alt="Correzione" height="18"> Villaggi e castelli poggiano sul terreno, non su quello che è già costruito lì: una nuova anteprima nello stesso posto non finisce più sopra i tetti vecchi.
- <img src="https://img.shields.io/badge/-Correzione-2e9e5b?style=flat-square" alt="Correzione" height="18"> Costruzioni: pannelli di vetro, sbarre, recinti e muretti sono collegati a quello che hanno accanto, non più paletti sottili.
- <img src="https://img.shields.io/badge/-Migliorato-d9831f?style=flat-square" alt="Migliorato" height="18"> In tutti i campi numerici, quando cambi un valore compare un piccolo tasto che lo riporta a quello di prima.
- <img src="https://img.shields.io/badge/-Nuovo-4f7cff?style=flat-square" alt="Nuovo" height="18"> Le costruzioni creano i chunk che servono: nei mondi void e piatti da sole, con il terreno giusto; nei mondi normali scegli tu, perché lì il gioco non può più creare il terreno. Annulla li toglie.
- <img src="https://img.shields.io/badge/-Nuovo-4f7cff?style=flat-square" alt="Nuovo" height="18"> Le case fungo sono case vere: gambo cavo con porta e finestre, e una stanza sotto il cappello.
- <img src="https://img.shields.io/badge/-Correzione-2e9e5b?style=flat-square" alt="Correzione" height="18"> L'anteprima delle costruzioni enormi mostra le case, non solo strade e lampioni.

**Aspetto**

- <img src="https://img.shields.io/badge/-Nuovo-4f7cff?style=flat-square" alt="Nuovo" height="18"> 12 temi che cambiano subito, senza riavviare, i tuoi colori e l'aspetto grigio di Windows.
- <img src="https://img.shields.io/badge/-Nuovo-4f7cff?style=flat-square" alt="Nuovo" height="18"> Nuovo ordine del menu laterale: prima la modifica, poi generatori e strumenti. L'ordine di prima è nelle impostazioni.
- <img src="https://img.shields.io/badge/-Nuovo-4f7cff?style=flat-square" alt="Nuovo" height="18"> Una nuova schermata di benvenuto con le novità.

**Conversione**

- <img src="https://img.shields.io/badge/-Nuovo-4f7cff?style=flat-square" alt="Nuovo" height="18"> Pagina Conversione: un mondo Java in Bedrock (.mcworld) e un mondo Bedrock in Java, con blocchi, biomi, contenitori con gli oggetti, mob, abitanti con i loro scambi, meccanismi redstone e tick in sospeso, e un report di cosa resta fuori. Arrivi dove stava il giocatore, e scegli modalità, trucchi e difficoltà.

**Mondi e server**

- <img src="https://img.shields.io/badge/-Nuovo-4f7cff?style=flat-square" alt="Nuovo" height="18"> Cronologia delle modifiche: una pagina con tutto quello che hai fatto a un mondo, anche dopo aver chiuso il programma, dove puoi annullare una costruzione o un incolla qualsiasi, non solo l'ultimo.
- <img src="https://img.shields.io/badge/-Nuovo-4f7cff?style=flat-square" alt="Nuovo" height="18"> Confronta due backup sulla mappa: i chunk nuovi, spariti e cambiati sono colorati e si possono selezionare.
- <img src="https://img.shields.io/badge/-Nuovo-4f7cff?style=flat-square" alt="Nuovo" height="18"> Pagina Server: impostazioni, whitelist, operatori e ban di un server, senza comandi.
- <img src="https://img.shields.io/badge/-Correzione-2e9e5b?style=flat-square" alt="Correzione" height="18"> Isole volanti: niente più erba, fiori e alberi sospesi nel vuoto. Le caverne potevano arrivare fino in superficie e togliere il terreno sotto di loro.

</details>

<details>
<summary><b>Versione 1.0.4</b></summary>


**Mappe in gioco**

- <img src="https://img.shields.io/badge/-Nuovo-4f7cff?style=flat-square" alt="Nuovo" height="18"> Metti le mappe nell'inventario di un giocatore: le selezioni e premi il pulsante, senza /give e senza trucchi. Vanno negli spazi liberi, poi nella cassa di Ender, e una mappa che il giocatore ha già non viene aggiunta due volte.
- <img src="https://img.shields.io/badge/-Nuovo-4f7cff?style=flat-square" alt="Nuovo" height="18"> Le nuove mappe da un'immagine vanno subito nell'inventario (si può togliere).
- <img src="https://img.shields.io/badge/-Nuovo-4f7cff?style=flat-square" alt="Nuovo" height="18"> Le mappe che un giocatore ha già sono segnate con una spunta e si possono vedere da sole, anche quelle dentro shulker e sacche: cambi l'immagine e il giocatore trova quella nuova.

**Link**

- <img src="https://img.shields.io/badge/-Migliorato-d9831f?style=flat-square" alt="Migliorato" height="18"> Sotto il menu laterale, tra i link di NIKstudios, ora c'è il pulsante del sito web.
- <img src="https://img.shields.io/badge/-Correzione-2e9e5b?style=flat-square" alt="Correzione" height="18"> Vedere le entità dei chunk selezionati sulla mappa non si ferma più con un errore, e "Teletrasportami qui" funziona in quella finestra.
- <img src="https://img.shields.io/badge/-Correzione-2e9e5b?style=flat-square" alt="Correzione" height="18"> Selezionando migliaia di chunk ora si trovano tutte le entità: prima venivano letti solo i primi 2048 chunk, spesso vuoti.
- <img src="https://img.shields.io/badge/-Correzione-2e9e5b?style=flat-square" alt="Correzione" height="18"> Il giocatore sulla mappa è nel blocco esatto e dove il gioco l'ha salvato per ultimo, anche se giochi con il programma aperto, e solo sulla mappa della dimensione in cui si trova (prima un giocatore nel Nether appariva nel posto sbagliato sulla mappa dell'Overworld).
- <img src="https://img.shields.io/badge/-Correzione-2e9e5b?style=flat-square" alt="Correzione" height="18"> Le entità eliminate dall'elenco spariscono subito dalla mappa, anche prima di salvare.
- <img src="https://img.shields.io/badge/-Correzione-2e9e5b?style=flat-square" alt="Correzione" height="18"> Viste 3D: le isole e le altre terre sospese si vedono intere. Il limite di profondità le tagliava e mostrava un pavimento piatto che nel gioco non c'è; ora vale solo per la roccia che arriva fino alla bedrock.
- <img src="https://img.shields.io/badge/-Correzione-2e9e5b?style=flat-square" alt="Correzione" height="18"> Viste 3D: i bauli sono disegnati come nel gioco, con coperchio, serratura sul lato giusto e le due metà dei bauli doppi unite.
- <img src="https://img.shields.io/badge/-Nuovo-4f7cff?style=flat-square" alt="Nuovo" height="18"> Le costruzioni trovano l'altezza da sole: se una uscirebbe sotto il fondo o sopra il limite del mondo viene spostata per farla stare tutta, anche nel vuoto. Se è più alta di tutto il mondo ti chiede prima.
- <img src="https://img.shields.io/badge/-Correzione-2e9e5b?style=flat-square" alt="Correzione" height="18"> Costruzioni: i pulsanti e il testo sotto l'anteprima non vengono più tagliati a destra.
- <img src="https://img.shields.io/badge/-Nuovo-4f7cff?style=flat-square" alt="Nuovo" height="18"> Elenco delle entità: la lista dei tipi trovati con quanti sono, ed Elimina tutte quelle mostrate per togliere in un colpo quelle in eccesso (quelle con un nome, addomesticate o al guinzaglio restano).

</details>

<details>
<summary><b>Versione 1.0.3</b></summary>


**Velocità**

- <img src="https://img.shields.io/badge/-Migliorato-d9831f?style=flat-square" alt="Migliorato" height="18"> NBT Studio parte molto più veloce (da circa 30 secondi a pochi secondi con tante versioni di Minecraft installate): le versioni del gioco vengono lette una volta sola e ricordate, e le pagine vengono create la prima volta che le apri.

**Giocatori**

- <img src="https://img.shields.io/badge/-Correzione-2e9e5b?style=flat-square" alt="Correzione" height="18"> La modalità di gioco scelta per un giocatore ora funziona quando entri nel gioco: volo, costruzione istantanea e invulnerabilità la seguono, viene tenuta la modalità precedente, e per il giocatore in singolo cambia anche la modalità del mondo.
- <img src="https://img.shields.io/badge/-Correzione-2e9e5b?style=flat-square" alt="Correzione" height="18"> Cambiare la modalità di gioco nelle Impostazioni del mondo la cambia anche per il giocatore in singolo (prima l'elenco dei mondi diceva Creativa ma il gioco partiva ancora in Sopravvivenza).
- <img src="https://img.shields.io/badge/-Correzione-2e9e5b?style=flat-square" alt="Correzione" height="18"> Viste 3D: l'acqua scende dalla sorgente come nel gioco (anche nella vista a immagini). 3D libero: le foglie mostrano le foglie dietro come nel gioco, le texture lontane non sfarfallano più e la vista è più veloce; i fotogrammi al secondo mostrati sono quelli veri.
- <img src="https://img.shields.io/badge/-Migliorato-d9831f?style=flat-square" alt="Migliorato" height="18"> I file dei giocatori che il gioco non usa (la vecchia playerdata di un mondo aggiornato alla 26.x, la copia del giocatore in singolo) sono segnati nell'elenco.

**Comandi**

- <img src="https://img.shields.io/badge/-Nuovo-4f7cff?style=flat-square" alt="Nuovo" height="18"> /give anche per mob ed entità: un uovo con tutti i loro dati (nome, vita, equipaggiamento, effetti...), oppure l'oggetto armor stand, cornice, carrello o barca.
- <img src="https://img.shields.io/badge/-Nuovo-4f7cff?style=flat-square" alt="Nuovo" height="18"> /give anche per bauli, spawner e gli altri blocchi con dati: il blocco tiene il suo contenuto quando lo piazzi.

**3D e texture**

- <img src="https://img.shields.io/badge/-Nuovo-4f7cff?style=flat-square" alt="Nuovo" height="18"> Vista 3D libera disegnata dalla scheda video: cammina e vola nell'area come in Minecraft (clic per guardarti intorno col mouse, Esc per il cursore, W A S D per muoverti), con le texture, i colori dei biomi e le ombre agli angoli, fluida anche con milioni di facce.
- <img src="https://img.shields.io/badge/-Correzione-2e9e5b?style=flat-square" alt="Correzione" height="18"> I tronchi di ciliegio e i blocchi di bambù della 26.x hanno di nuovo gli anelli sopra, non sui lati.
- <img src="https://img.shields.io/badge/-Correzione-2e9e5b?style=flat-square" alt="Correzione" height="18"> Tronchi, steli, pilastri e fieno messi in orizzontale mostrano gli anelli solo alle due estremità, e la corteccia sugli altri lati.
- <img src="https://img.shields.io/badge/-Correzione-2e9e5b?style=flat-square" alt="Correzione" height="18"> Il lato dei blocchi d'erba: solo la frangia d'erba prende il colore del bioma, la terra resta marrone.
- <img src="https://img.shields.io/badge/-Correzione-2e9e5b?style=flat-square" alt="Correzione" height="18"> Dispenser e dropper in 3D sono girati verso nord, come gli altri blocchi orientati.

</details>

<details>
<summary><b>Versione 1.0.2</b></summary>


**Creazione mappe (Beta)**

- <img src="https://img.shields.io/badge/-Nuovo-4f7cff?style=flat-square" alt="Nuovo" height="18"> Nuova pagina per le mappe fatte con i comandi, nei Generatori.
- <img src="https://img.shields.io/badge/-Nuovo-4f7cff?style=flat-square" alt="Nuovo" height="18"> Catene di blocchi comandi: un comando per riga (? per i condizionali), messe nel mondo con un pulsante per farle partire, o salvate come schematic.
- <img src="https://img.shields.io/badge/-Nuovo-4f7cff?style=flat-square" alt="Nuovo" height="18"> Checkpoint: una pedana d'oro che imposta il punto di respawn, con messaggio, suono e cura.
- <img src="https://img.shields.io/badge/-Nuovo-4f7cff?style=flat-square" alt="Nuovo" height="18"> Zone che attivano comandi: partono quando un giocatore entra in un'area (una volta, ogni volta, sempre o solo per il primo).
- <img src="https://img.shields.io/badge/-Nuovo-4f7cff?style=flat-square" alt="Nuovo" height="18"> Timer con conto alla rovescia: boss bar, secondi sopra la barra rapida e comandi all'inizio e alla fine.
- <img src="https://img.shields.io/badge/-Nuovo-4f7cff?style=flat-square" alt="Nuovo" height="18"> Dialoghi con gli NPC: un personaggio che parla quando ti avvicini, con risposte da cliccare in chat.
- <img src="https://img.shields.io/badge/-Nuovo-4f7cff?style=flat-square" alt="Nuovo" height="18"> Oggetti con poteri col tasto destro: scatto, salto, cura, velocità, fulmine, esplosione, teletrasporto o i tuoi comandi, con un'attesa tra un uso e l'altro.
- <img src="https://img.shields.io/badge/-Nuovo-4f7cff?style=flat-square" alt="Nuovo" height="18"> Datapack installati nel mondo aperto con un clic, nella sintassi di ogni versione.

**Strumenti del mondo**

- <img src="https://img.shields.io/badge/-Nuovo-4f7cff?style=flat-square" alt="Nuovo" height="18"> Ripristina da un backup solo i chunk che selezioni: la base fatta saltare da un creeper torna com'era, il resto del mondo resta com'è.
- <img src="https://img.shields.io/badge/-Nuovo-4f7cff?style=flat-square" alt="Nuovo" height="18"> Ripara i file regione: trova i chunk danneggiati (quelli che fanno crashare il gioco o spariscono) e li toglie, e rimette al loro posto i chunk salvati nella posizione sbagliata.
- <img src="https://img.shields.io/badge/-Nuovo-4f7cff?style=flat-square" alt="Nuovo" height="18"> Mappa dei minerali: i chunk colorati in base a quanti diamanti, detriti antichi, ferro, spawner... hanno tra due altezze.
- <img src="https://img.shields.io/badge/-Nuovo-4f7cff?style=flat-square" alt="Nuovo" height="18"> Strutture: ogni villaggio, roccaforte, città antica, camera della prova, monumento... davvero generato, con la posizione, prima i più vicini, e il teletrasporto.
- <img src="https://img.shields.io/badge/-Nuovo-4f7cff?style=flat-square" alt="Nuovo" height="18"> Modifica di gruppo: una modifica a ogni mob, baule, cartello, spawner o oggetto che corrisponde (il mob di tutti gli spawner, una parola su tutti i cartelli, un oggetto in ogni baule...), prima mostrata, poi applicata.
- <img src="https://img.shields.io/badge/-Nuovo-4f7cff?style=flat-square" alt="Nuovo" height="18"> Confronta due file NBT (o quello aperto con un backup): ogni valore aggiunto, tolto o cambiato.
- <img src="https://img.shields.io/badge/-Nuovo-4f7cff?style=flat-square" alt="Nuovo" height="18"> Oggetti convertiti tra versioni: kit e modelli di oggetti di un'altra versione vengono riscritti per il mondo, e il comando /give si può fare per un'altra versione.
- <img src="https://img.shields.io/badge/-Migliorato-d9831f?style=flat-square" alt="Migliorato" height="18"> Gli Strumenti costruzione mostrano in 3D quello che hai copiato o importato (.nbt, .schem, .litematic) prima di incollarlo.

**Spawner e mob**

- <img src="https://img.shields.io/badge/-Nuovo-4f7cff?style=flat-square" alt="Nuovo" height="18"> Spawner personalizzati: più mob nello stesso spawner, ognuno con la sua probabilità, anche con la luce.
- <img src="https://img.shields.io/badge/-Nuovo-4f7cff?style=flat-square" alt="Nuovo" height="18"> Ogni mob dello spawner con nome colorato, cucciolo, bagliore, fiamme, silenzioso, invulnerabile, senza IA, vita, dimensione, velocità, danno, equipaggiamento ed effetti.
- <img src="https://img.shields.io/badge/-Nuovo-4f7cff?style=flat-square" alt="Nuovo" height="18"> Torri di mob: mob uno sopra l'altro, con torri già pronte, da /summon o da un uovo.
- <img src="https://img.shields.io/badge/-Nuovo-4f7cff?style=flat-square" alt="Nuovo" height="18"> "I miei mob": salva un mob o una torre intera come modello e riusalo ovunque.

**Costruzioni**

- <img src="https://img.shields.io/badge/-Migliorato-d9831f?style=flat-square" alt="Migliorato" height="18"> La pagina Costruzioni ora è un elenco a sezioni invece delle schede.
- <img src="https://img.shields.io/badge/-Nuovo-4f7cff?style=flat-square" alt="Nuovo" height="18"> 10 nuovi generatori: parkour, dungeon, montagne russe, città, statue dalla skin, testo 3D, isole volanti, vulcani, arene per minigiochi e canzoni con i blocchi nota da file MIDI.
- <img src="https://img.shields.io/badge/-Nuovo-4f7cff?style=flat-square" alt="Nuovo" height="18"> Statue dalla skin che si girano o si sdraiano, riconoscono le braccia slim, hanno il secondo strato in rilievo e colori realistici, con vetro colorato per i pixel trasparenti.
- <img src="https://img.shields.io/badge/-Nuovo-4f7cff?style=flat-square" alt="Nuovo" height="18"> Città con stili, finestre, tetti, piazza con fontana, alberi, lampioni, luci accese e palazzi alti al centro.
- <img src="https://img.shields.io/badge/-Nuovo-4f7cff?style=flat-square" alt="Nuovo" height="18"> Isole volanti con 7 forme e 7 aspetti (erba, ciliegi, neve, deserto, funghi, Nether, End), i minerali che scegli in vene, caverne, stanze con spawner con i tuoi mob, bauli col bottino, piante e ponti.
- <img src="https://img.shields.io/badge/-Correzione-2e9e5b?style=flat-square" alt="Correzione" height="18"> Le isole volanti ricevono un bioma, così i mob ci appaiono (in un mondo vuoto il bioma "the void" non ne ha), e dopo averle messe NBT Studio ti dice se la difficoltà o una regola del gioco ferma i mob.
- <img src="https://img.shields.io/badge/-Nuovo-4f7cff?style=flat-square" alt="Nuovo" height="18"> Città con un aspetto diverso per ogni stile (moderna, centro storico, futuristica, nether, deserto e colorata): strade, strisce, lampioni, alberi, parchi, tetti, angoli e fasce cambiano con lo stile.
- <img src="https://img.shields.io/badge/-Nuovo-4f7cff?style=flat-square" alt="Nuovo" height="18"> Città con i colori che scegli: muri di un colore o a colori a caso, angoli e fasce, e il vetro.
- <img src="https://img.shields.io/badge/-Nuovo-4f7cff?style=flat-square" alt="Nuovo" height="18"> Dungeon con i mob che scegli (anche i tuoi modelli), un boss, il bottino che vuoi e stanze speciali: tesoro, biblioteca, prigione, lava, trappole e stanze invase dalla natura.
- <img src="https://img.shields.io/badge/-Nuovo-4f7cff?style=flat-square" alt="Nuovo" height="18"> "Senza limiti" in ogni generatore, per superare i massimi normali (con un avviso).
- <img src="https://img.shields.io/badge/-Nuovo-4f7cff?style=flat-square" alt="Nuovo" height="18"> "Senza limiti" toglie davvero i massimi: città e forme enormi vengono fatte e messe a pezzi (con il pulsante Interrompi e l'annullamento), l'anteprima mostra il centro o una copia più piccola.
- <img src="https://img.shields.io/badge/-Nuovo-4f7cff?style=flat-square" alt="Nuovo" height="18"> Annulla l'ultima costruzione, gira l'anteprima 3D e porta il giocatore alla costruzione.
- <img src="https://img.shields.io/badge/-Nuovo-4f7cff?style=flat-square" alt="Nuovo" height="18"> Annulla funziona anche con le costruzioni enormi, come le città intere: una copia dei file delle regioni resta fino alla costruzione dopo.
- <img src="https://img.shields.io/badge/-Migliorato-d9831f?style=flat-square" alt="Migliorato" height="18"> Spawner e bauli di una costruzione tengono i loro dati quando la salvi come schematic.

**Comandi**

- <img src="https://img.shields.io/badge/-Migliorato-d9831f?style=flat-square" alt="Migliorato" height="18"> Le pozioni sono come il tooltip del gioco: effetti dannosi in rosso, benefici in blu, durate giuste e "Effetto applicato".

**Interfaccia**

- <img src="https://img.shields.io/badge/-Migliorato-d9831f?style=flat-square" alt="Migliorato" height="18"> Grafica nuova: schede, caselle con la spunta, frecce, barre di scorrimento sottili, cursori e barre di avanzamento.
- <img src="https://img.shields.io/badge/-Nuovo-4f7cff?style=flat-square" alt="Nuovo" height="18"> Grandezza del testo con Ctrl + e Ctrl - (Ctrl 0: normale) subito, e lo zoom di tutta l'interfaccia nelle Impostazioni.
- <img src="https://img.shields.io/badge/-Nuovo-4f7cff?style=flat-square" alt="Nuovo" height="18"> Novità sopra le Impostazioni, e Segnala un problema nel menu Aiuto.
- <img src="https://img.shields.io/badge/-Migliorato-d9831f?style=flat-square" alt="Migliorato" height="18"> Le icone di GitHub si vedono nel tema chiaro; Creazione mappe è segnata (Beta).
- <img src="https://img.shields.io/badge/-Migliorato-d9831f?style=flat-square" alt="Migliorato" height="18"> Nomi delle torri di mob con il font del gioco, e un elenco dei colori con i nomi.
- <img src="https://img.shields.io/badge/-Migliorato-d9831f?style=flat-square" alt="Migliorato" height="18"> Le costruzioni piccole sono nitide nell'anteprima 3D invece che sfocate.
- <img src="https://img.shields.io/badge/-Migliorato-d9831f?style=flat-square" alt="Migliorato" height="18"> In 3D pulsanti, teste, letti, scale, porte, botole, cartelli, stendardi, bauli, torte, incudini, falò e altro hanno la loro forma.
- <img src="https://img.shields.io/badge/-Migliorato-d9831f?style=flat-square" alt="Migliorato" height="18"> I blocchi senza texture in 3D ora ce l'hanno: bauli di rame, teste, stendardi, vasi decorati, statue del golem di rame, sbarre di rame cerate, letti e cartelli appesi (26.x e più vecchie), e molti blocchi della 1.8.
- <img src="https://img.shields.io/badge/-Migliorato-d9831f?style=flat-square" alt="Migliorato" height="18"> Più mob mostrano la faccia invece dell'uovo (pipistrello, coniglio, capra, breeze, golem di rame, creaking, lama, hoglin, ravager, tartaruga, phantom, pesci, shulker, wither, pappagallo, giocatore...), anche nella 1.8.

**Correzioni**

- <img src="https://img.shields.io/badge/-Correzione-2e9e5b?style=flat-square" alt="Correzione" height="18"> I bauli prima della 1.15 (come nella 1.8) non sono più deformati nelle icone.
- <img src="https://img.shields.io/badge/-Correzione-2e9e5b?style=flat-square" alt="Correzione" height="18"> Fornaci, dispenser, osservatori e zucche intagliate mostrano in 3D i loro lati veri, non il davanti due volte.
- <img src="https://img.shields.io/badge/-Correzione-2e9e5b?style=flat-square" alt="Correzione" height="18"> Erba e foglie hanno il colore del gioco in ogni bioma (spiagge, caverne, End...), e i biomi delle mod sono come la pianura.
- <img src="https://img.shields.io/badge/-Correzione-2e9e5b?style=flat-square" alt="Correzione" height="18"> Le finestre più alte dello schermo (come quella degli oggetti con tanti incantesimi) stanno sopra la barra di Windows, e il contenuto scorre quando serve.
- <img src="https://img.shields.io/badge/-Nuovo-4f7cff?style=flat-square" alt="Nuovo" height="18"> Sotto il tooltip di oggetti e pozioni scegli se i tooltip lunghi si rimpiccioliscono o restano grandi e scorrono.
- <img src="https://img.shields.io/badge/-Correzione-2e9e5b?style=flat-square" alt="Correzione" height="18"> Il riavvio dalle Impostazioni non mostra più "No module named PySide6.QtSvg".
- <img src="https://img.shields.io/badge/-Correzione-2e9e5b?style=flat-square" alt="Correzione" height="18"> Il riavvio dopo un aggiornamento automatico funziona.
- <img src="https://img.shields.io/badge/-Correzione-2e9e5b?style=flat-square" alt="Correzione" height="18"> Chiudere Segnala un problema non riapre più le Novità di continuo fino al crash.
- <img src="https://img.shields.io/badge/-Correzione-2e9e5b?style=flat-square" alt="Correzione" height="18"> Le schede dei generatori non vengono più allungate con spazi vuoti.
- <img src="https://img.shields.io/badge/-Correzione-2e9e5b?style=flat-square" alt="Correzione" height="18"> L'anteprima 3D delle costruzioni molto grandi tiene muri, finestre e colori.
- <img src="https://img.shields.io/badge/-Correzione-2e9e5b?style=flat-square" alt="Correzione" height="18"> La finestra che compare mentre piazza i blocchi si chiama NBT Studio, non "python".

</details>

<details>
<summary><b>Versione 1.0.0</b></summary>

- <img src="https://img.shields.io/badge/-Nuovo-4f7cff?style=flat-square" alt="Nuovo" height="18"> Prima versione pubblica di NBT Studio.

</details>

---

<!-- novita:fine -->

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
