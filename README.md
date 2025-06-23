# 🔋 KeepAwake – WakeLock App per Fire TV

**KeepAwake** è una semplice app Android progettata per **impedire che la Fire TV entri in standby o si spenga automaticamente**, mantenendo la CPU attiva grazie a un `WakeLock`.

> ✅ Nessuna interfaccia visibile  
> ✅ Funziona in background  
> ✅ Si avvia automaticamente all'accensione  
> ✅ Ideale per Fire TV Stick / Cube / Android TV  
> ✅ Completamente open source

---

## 📦 Caratteristiche

- Impedisce lo spegnimento o la sospensione automatica della Fire TV
- Nessuna UI, lavora in background in modo silenzioso
- Nessuna connessione a internet necessaria
- Si attiva da sola al riavvio del dispositivo
- Sorgente minimale e leggibile

---

## 📥 Come installare KeepAwake su Fire TV (Guida per tutti)

### ✅ Metodo 1 – Con PC (ADB)

#### Requisiti:
- Un PC con Windows, Linux o Mac
- Fire TV collegata alla **stessa rete Wi-Fi**
- Debug ADB attivo sulla Fire TV

#### Passaggi:

1. Vai su **Impostazioni > La mia Fire TV > Opzioni sviluppatore**  
   Attiva:
    - `Debug ADB`
    - `App da fonti sconosciute`

   > Se "Opzioni sviluppatore" non compare, vai su **Info > Fire TV Stick**, seleziona “Numero build” e premi **7 volte OK** sul telecomando.

2. Scopri l’IP della Fire TV da **Impostazioni > Rete**

3. [Scarica il file APK](https://github.com/lavitasecondopizzi/keepawake/releases/latest/download/KeepAwake.apk)

4. Installa ADB sul PC:
   https://developer.android.com/tools/releases/platform-tools

5. Esegui dal terminale (nella cartella `platform-tools`):
   ```bash
   adb connect IP_DELLA_FIRE_TV
   adb install KeepAwake.apk
   adb shell pm grant com.lavitasecondopizzi.keepawake android.permission.RECEIVE_BOOT_COMPLETED
   ```
    > IMPORTANTE: Sostituisci IP_DELLA_FIRE_TV con l'ip locale della tua fire tv.
---

### 🔶 Metodo 2 – Con l'app Downloader (senza PC)

1. Attiva: **Impostazioni > La mia Fire TV > Opzioni sviluppatore > App da fonti sconosciute > Downloader**

2. Installa l’app “Downloader” dallo store Amazon

3. Apri Downloader e inserisci:
   https://github.com/lavitasecondopizzi/keepawake/releases/latest/download/KeepAwake.apk

4. Scarica e seleziona **Installa**

> ℹ️ Alcune versioni di Fire OS potrebbero **non concedere** il permesso di avvio automatico al riavvio (funzione limitata se non usi ADB).

---

### 🔸 Metodo 3 – Chiavetta USB o cavo OTG

1. Copia `KeepAwake.apk` su una chiavetta USB
2. Inserisci la chiavetta sulla Fire TV (con adattatore OTG se necessario)
3. Apri un file manager (es. “X-plore”)
4. Seleziona e installa il file APK

---

## ✅ Dopo l’installazione

L’app è **completamente invisibile** e **non ha icone o interfaccia**.

Per verificare se è attiva:
- Accendi la Fire TV e lasciala inattiva
- Se **non si spegne più da sola**, l’app è in esecuzione correttamente

---

## 🗑️ Come disinstallarla

### Metodo 1 – da PC (ADB)
```bash
adb uninstall com.lavitasecondopizzi.keepawake
```

### Metodo 2 – dalla Fire TV
- Vai su **Impostazioni > Applicazioni > Gestisci applicazioni**
- Trova “KeepAwake” e premi **Disinstalla**

---

## 🏷️ Tag

```
fire-tv, android-tv, wakelock, standby, deep-sleep, adb, fireos, keep-awake, launcher, auto-start, background-service, power-management
```

---

## ⚠️ Avvertenze

- Questa app è pensata **per uso personale o tecnico**
- Non è pubblicata su Amazon Appstore
- Potrebbe non funzionare correttamente su versioni future di Fire OS con restrizioni aggiuntive

---

## 👤 Autore

Sviluppato da [@lavitasecondopizzi](https://github.com/lavitasecondopizzi)  
Licenza: MIT

---

## 💡 Contribuire

Pull request e suggerimenti sono benvenuti!