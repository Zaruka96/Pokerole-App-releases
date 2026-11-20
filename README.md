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
  <a href="#-docker">🐳 Docker / NAS</a>
</p>

---

## 📌 Cos'è

**Pokérole Companion** accompagna le sessioni di **Pokérole 2.0** (il gioco di ruolo, versione classica, non Mystery Dungeon). I dati vengono dal *Corebook 2.0*. Interfaccia e regole in italiano, nomi di Pokémon, mosse, abilità e oggetti in inglese come nel manuale.

> Questo repository contiene solo **installer** e **file di aggiornamento automatico**: il codice sorgente non è pubblico.

## ✨ Funzionalità

**Master**
- 📖 **Pokédex completo** (Kanto → Galar, forme e Mega): filtri per tipo, regione, rank, abilità e mosse; attributi a pallini come nella scheda, mosse per rank, linea evolutiva, debolezze
- ⚔️ **Mosse, abilità e oggetti** con ricerca e filtri
- 📚 **Regole** in 15 capitoli, spiegate in modo semplice
- 🎲 **Generatore di incontri** con Pokémon selvatici già pronti, **tracker di combattimento** (iniziativa, HP, dolore, stati, meteo)
- 👥 **Schede dei giocatori** importate da file o testo

**Player**
- 🪪 **Scheda allenatore** (Trainer Card) con punti per rank e achievement
- 🔴 **Squadra e box**, scheda di ogni Pokémon
- 🎯 **Dadi automatici sulle mosse**: accuratezza, danno, STAB, dolore, difesa, efficacia di tipo, critico e Chance Dice
- 🎒 **Inventario**, 🏋️ **training** verso il rank successivo, 🧬 vittorie per l'evoluzione, 🔥 **tabella dei tipi**

## 📦 Installazione

| Sistema | File | Note |
|---|---|---|
| **Windows** | `…_windows-x64-setup.exe` | Se SmartScreen avvisa: *Ulteriori informazioni → Esegui comunque* |
| **macOS** (Apple Silicon e Intel) | `…_macos-universal.dmg` | App non firmata: la prima volta clic destro sull'app → *Apri* |
| **Android** | `…_android.apk` | Consenti l'installazione da origini sconosciute |
| **iOS** | `…_ios-unsigned.ipa` | Con [SideStore](https://sidestore.io) o Sideloadly (vedi sotto) |
| **Server / NAS** | `ghcr.io/zaruka96/pokerole-app` | Vedi [Docker](#-docker) |

### iOS con SideStore
Aggiungi una volta questa fonte in SideStore (*Sources → +*):

```
https://github.com/Zaruka96/Pokerole-App-releases/releases/latest/download/source.json
```

## 🔄 Aggiornamenti

L'app controlla da sola le nuove versioni all'avvio e ogni 6 ore (anche dal pulsante *Controlla aggiornamenti* nella home):

- **Windows / macOS**: scarica, installa e si riavvia (pacchetti firmati, verificati prima dell'installazione)
- **Android**: scarica l'APK e lo installa, Android chiede solo la conferma
- **iOS**: apre SideStore sulla nuova versione
- **Docker**: mostra l'avviso con il comando per aggiornare il container

Schede, squadra e inventario restano sul dispositivo: esporta la scheda dall'app per fare un backup.

## 🐳 Docker

```yaml
services:
  pokerole:
    image: ghcr.io/zaruka96/pokerole-app:latest
    pull_policy: always
    ports:
      - "8080:80"
    restart: unless-stopped
```

Poi apri `http://<indirizzo-del-server>:8080`. Per aggiornare: `docker compose pull && docker compose up -d`. Immagine per `amd64` e `arm64`.

## ⚖️ Note

Progetto amatoriale per uso personale, senza scopo di lucro. Pokérole è un gioco fan-made; nomi, immagini e marchi Pokémon appartengono a Nintendo, Game Freak e The Pokémon Company.
