<p align="center"><img src="icon.png" alt="Pokérole Companion" width="120"></p>

<h1 align="center">Pokérole Companion</h1>

<p align="center"><b>Il compagno di gioco per Pokérole 2.0: tutto il manuale per il Master, schede e dadi automatici per i giocatori.</b></p>

<p align="center">
  <a href="https://github.com/Zaruka96/Pokerole-App-releases/releases/latest"><img alt="Ultima release" src="https://img.shields.io/github/v/release/Zaruka96/Pokerole-App-releases?label=release&color=E5503A"></a>
  <a href="https://github.com/Zaruka96/Pokerole-App-releases/releases"><img alt="Download" src="https://img.shields.io/github/downloads/Zaruka96/Pokerole-App-releases/total?label=download"></a>
  <a href="https://github.com/users/Zaruka96/packages/container/package/pokerole-app"><img alt="Docker" src="https://img.shields.io/badge/docker-ghcr.io%2Fzaruka96%2Fpokerole--app-2496ED?logo=docker&logoColor=white"></a>
  <br>
  <img alt="Piattaforme" src="https://img.shields.io/badge/piattaforme-Windows%20%7C%20macOS%20%7C%20Android%20%7C%20iOS%20%7C%20Docker-555">
</p>

<p align="center">
  <a href="https://github.com/Zaruka96/Pokerole-App-releases/releases/latest"><b>⬇️ Scarica l'ultima versione</b></a> ·
  <a href="#-installazione">📦 Installazione</a> ·
  <a href="#-aggiornamenti">🔄 Aggiornamenti</a> ·
  <a href="#-docker--nas">🐳 Docker / NAS</a>
</p>

---

## 📌 Cos'è

**Pokérole Companion** accompagna le sessioni di **Pokérole 2.0** (il gioco di ruolo, versione classica, non Mystery Dungeon). I dati vengono dal *Corebook 2.0*. Interfaccia e regole in italiano, nomi di Pokémon, mosse, abilità e oggetti in inglese come nel manuale.

> Questo repository contiene solo **installer** e **file di aggiornamento automatico**: il codice sorgente non è pubblico.

## ✨ Funzionalità

**Accesso**
- 🔐 All'apertura scegli l'**host**: *Locale* (lobby sulla stessa Wi-Fi, basta il nome) o un **server** (nome utente e password; i server usati restano in elenco). Oppure usa l'app **offline** come companion
- 🛡️ Tab **Admin server** per aprire il pannello di amministrazione di un server (o crearne il primo amministratore)

**Guida** (per tutti)
- 📖 **Pokédex completo** (Kanto → Galar, forme e Mega): filtri per tipo, regione, rank, abilità e mosse; attributi a pallini come nella scheda, mosse per rank, linea evolutiva, debolezze
- ⚔️ **Mosse, abilità e oggetti** con ricerca e filtri, 📚 **regole** in 15 capitoli spiegate in modo semplice, 🔥 **tabella dei tipi**

**Lobby** (si gioca insieme)
- 🏠 **Le mie lobby** con codice e ruolo; ospiti una lobby o entri con il codice, con un **link o un QR d'invito**
- 🎭 Entrando scegli **Master o Player**; il player crea un personaggio per la campagna o collega uno già fatto. In lobby il player non vede gli strumenti del Master e viceversa
- 💬 **Chat** con whisper, immagini, video, ritratti e messaggi non letti; richieste di tiro e ricompense del Master; scena a schermo intero
- 🧑‍🤝‍🧑 Tab **Giocatori** per il Master: HP di tutti a colpo d'occhio, modifica di statistiche, squadra e inventario dei player, con **annulla**
- 🗺️ **NPC** secondari (nome, immagine, squadra) e principali (scheda completa, solo per il Master), nascosti finché il Master non li rivela
- ⚔️ **Combattimento** secondo le regole con dadi veri o simulati e avviso quando **tocca a te**; scambi tra player; diario di sessione

**Player**
- 👤 **I miei personaggi**: più schede, con un account server le ritrovi da ogni dispositivo
- 🪪 **Scheda allenatore** (Trainer Card) con punti per rank e achievement; 🔴 **squadra e box**, scheda di ogni Pokémon
- 🎯 **Dadi automatici sulle mosse**: accuratezza, danno, STAB, dolore, difesa, efficacia di tipo, critico e Chance Dice
- 🎒 **Inventario**, 🏋️ **training** verso il rank successivo, 🧬 vittorie per l'evoluzione

**Master** (anche senza lobby)
- 🎲 **Generatore di incontri** con Pokémon selvatici già pronti, **tracker di combattimento** (iniziativa, HP, dolore, stati, meteo)

Su smartphone le sezioni stanno in una barra in basso; tema **chiaro, scuro o automatico** dal menu del profilo.

## 📦 Installazione

| Sistema | File | Note |
|---|---|---|
| **Windows** | `…_windows-x64-setup.exe` | Se SmartScreen avvisa: *Ulteriori informazioni → Esegui comunque* |
| **macOS** (Apple Silicon e Intel) | `…_macos-universal.dmg` | App non firmata: la prima volta clic destro sull'app → *Apri* |
| **Android** | `…_android.apk` | Consenti l'installazione da origini sconosciute |
| **iOS** | `…_ios-unsigned.ipa` | Con [SideStore](https://sidestore.io) o Sideloadly (vedi sotto) |
| **Server / NAS** | `ghcr.io/zaruka96/pokerole-app` | Vedi [Docker](#-docker--nas) |

### iOS con SideStore
Aggiungi una volta questa fonte in SideStore (*Sources → +*):

```
https://github.com/Zaruka96/Pokerole-App-releases/releases/latest/download/source.json
```

## 🔄 Aggiornamenti

L'app controlla da sola le nuove versioni all'avvio e ogni 6 ore (anche dal pulsante *Controlla aggiornamenti* in *Le mie lobby* o *I miei personaggi*):

- **Windows / macOS**: scarica, installa e si riavvia (pacchetti firmati, verificati prima dell'installazione)
- **Android**: scarica l'APK e lo installa, Android chiede solo la conferma
- **iOS**: apre SideStore sulla nuova versione
- **Docker**: mostra l'avviso con il comando per aggiornare il container

Senza account le schede restano sul dispositivo (esportale dall'app per un backup); con un account su un server i tuoi personaggi sono salvati anche lì.

## 🐳 Docker / NAS

Il container serve l'app web **e il server delle lobby** per giocare via internet. Campagne, chat e immagini/video caricati restano nel volume `/data`, quindi sopravvivono agli aggiornamenti.

```yaml
services:
  pokerole:
    image: ghcr.io/zaruka96/pokerole-app:latest
    pull_policy: always
    ports:
      - "8080:80"
    volumes:
      - pokerole-data:/data # campagne e media delle lobby
    restart: unless-stopped
volumes:
  pokerole-data:
```

**Primo avvio:** apri `http://<indirizzo-del-server>:8080/admin` (oppure, dall'app, *Admin server* nella schermata di accesso) e crea l'account amministratore. In alternativa imposta `ADMIN_USERNAME` e `ADMIN_PASSWORD` nel compose.

**Account e ruoli:** chiunque può iscriversi dalla schermata di accesso dell'app (*Non hai un account? Iscriviti*), ma entra solo dopo l'approvazione dell'admin. Dal pannello `/admin` l'admin approva le iscrizioni, assegna i ruoli (**Admin**, **Master** che può creare campagne, **Player**), gestisce campagne, connessioni, impostazioni, registro degli accessi e backup.

**Per giocare insieme:** nell'app scegli il server come host e accedi, poi *Ospita una lobby*; gli altri entrano con il codice di 6 caratteri o con il link/QR d'invito (*Lobby → Invita*) e ritrovano le loro lobby in *Le mie lobby*, da qualsiasi dispositivo.

Per aggiornare: `docker compose pull && docker compose up -d` (i dati in `/data` restano). Immagine per `amd64` e `arm64`. Su un NAS con cartelle condivise imposta `PUID`/`PGID` dell'utente che deve possedere i dati (predefinito 1000).

### TrueNAS SCALE

*Apps → Discover Apps → ⋮ → Install via YAML*. Crea prima un dataset (es. `tank/apps/pokerole`): i permessi li sistema il container, che dà la cartella all'utente `apps` (568) e poi gira come quell'utente. Non aggiungere `user:` al file, altrimenti non può farlo.

```yaml
services:
  pokerole:
    image: ghcr.io/zaruka96/pokerole-app:latest
    pull_policy: always
    restart: unless-stopped
    environment:
      PUID: "568" # utente "apps" di TrueNAS
      PGID: "568"
      PORT: "8080" # porta interna non privilegiata
    ports:
      - "8080:8080" # porta del NAS : porta interna
    volumes:
      - /mnt/tank/apps/pokerole:/data
    healthcheck:
      test: ["CMD", "wget", "-qO-", "http://127.0.0.1:8080/health"]
      interval: 30s
      timeout: 3s
      retries: 3
```

Per aggiornare: *Update* dall'elenco delle app.

### Dietro un reverse proxy (dominio HTTPS)

- **WebSocket attivi** sul percorso `/ws` (in Nginx Proxy Manager: *Websockets Support*), altrimenti le lobby non si collegano.
- **Upload fino a 25 MB** per immagini e video in chat (nginx: `client_max_body_size 25m;`).
- Nell'app usa l'indirizzo `https://tuo-dominio` come server Docker.
- Il server è pensato per stare su internet (account, password cifrate, limite ai tentativi, media visibili solo ai partecipanti), ma usalo sempre **dietro HTTPS**: in chiaro le password viaggerebbero leggibili.

## ⚖️ Note

Progetto amatoriale per uso personale, senza scopo di lucro. Pokérole è un gioco fan-made; nomi, immagini e marchi Pokémon appartengono a Nintendo, Game Freak e The Pokémon Company.
