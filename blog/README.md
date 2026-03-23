# Blog di Mattia Martinelli

Questa cartella contiene i dati per la sezione blog del portfolio.

## Struttura

```
blog/
├── articles.json          # Lista di tutti gli articoli
└── README.md             # Questo file
```

## Come Aggiungere Articoli

### Step 1: Apri il file `articles.json`

Apri il file `blog/articles.json` con un editor di testo (Notepad++, VS Code, o anche il Blocco Note).

### Step 2: Aggiungi un Nuovo Articolo

Aggiungi un nuovo oggetto alla lista JSON. **Esempio:**

```json
{
  "id": "slug-articolo",
  "title": "Titolo del Tuo Articolo",
  "date": "2024-03-23",
  "category": "Machine Learning",
  "tags": ["python", "ml", "tutorial"],
  "description": "Una breve descrizione dell'articolo (100-150 caratteri)",
  "author": "Mattia Martinelli",
  "readTime": "10 min",
  "url": "https://medium.com/link-articolo",
  "externalLink": true
}
```

### Step 3: Salva il File

Salva il file. **Subito dopo**, il blog sul tuo portfolio si aggiornerà automaticamente.

---

## Guida Dettagliata per Principianti

### Cosa significa ogni campo?

| Campo | Spiegazione | Esempio |
|-------|-------------|---------|
| **id** | Identificatore unico (slugified) | `"ml-time-series-forecast"` |
| **title** | Titolo articolo | `"Machine Learning per Time Series"` |
| **date** | Data pubblicazione (YYYY-MM-DD) | `"2024-03-23"` |
| **category** | Categoria (per filtri) | `"Machine Learning"` |
| **tags** | Parole chiave (array) | `["python", "ml", "tutorial"]` |
| **description** | Breve descrizione (100-150 caratteri) | `"Come costruire modelli robusti..."` |
| **author** | Nome dell'autore | `"Mattia Martinelli"` |
| **readTime** | Tempo di lettura stimato | `"10 min"` |
| **url** | Link dell'articolo | `"https://medium.com/..."` |
| **externalLink** | (`true/false`) Se esterno = apre in tab nuova | `true` |

### Categorie Disponibili (Predefinite)

- Machine Learning
- Data Engineering
- Backend
- Aerospace
- DevOps (o aggiungi le tue)

### Esempi di URL per Articoli Hostati Esternamente

**Opzione 1: Medium**
```
"url": "https://medium.com/@tuonome/articolo",
"externalLink": true
```

**Opzione 2: Dev.to**
```
"url": "https://dev.to/tuonome/articolo",
"externalLink": true
```

**Opzione 3: Hashnode**
```
"url": "https://hashnode.com/@tuonome/articolo",
"externalLink": true
```

**Opzione 4: LinkedIn Article**
```
"url": "https://www.linkedin.com/pulse/mio-articolo",
"externalLink": true
```

**Opzione 5: Articolo nel tuo sito (locale)**
```
"url": "blog/articoli/mio-articolo.html",
"externalLink": false
```

---

## 🔄 Workflow Completo (Dall'Inizio alla Fine)

### Scenario: Vuoi Aggiungere un Articolo su Medium

```
1. ✍️  Scrivi l'articolo su Medium
   └─ Copia il link quando è pubblicato

2. 📝 Apri VS Code (o editor di testo)
   └─ File → Open Folder → scegli "MattMattw.github.io"

3. 📂 Naviga a: blog/articles.json
   └─ Vai alla fine dell'array JSON (prima dell'ultimo `]`)

4. ➕ Aggiungi una virgola dopo l'ultimo articolo:
   ```json
   },  ← AGGIUNGI QUESTA VIRGOLA se non c'è
   {
     "id": "nuovo-articolo",
     ...
   }
   ```

5. ✏️  Copia uno dei template di articolo
   └─ Modifica i campi con i tuoi dati

6. 💾 Salva il file (Ctrl+S)

7. 🚀 Push su GitHub:
   ```bash
   git add blog/articles.json
   git commit -m "Add new blog article: My New Article"
   git push
   ```

8. ✅ Fatto! Il blog si aggiorna automaticamente in ~30 secondi
```

---

## ⚠️ Errori Comuni e Come Risolverli

### Errore: "JSON Parsing Error" / Blog Non Carica

**Causa:** Errore di sintassi JSON (virgola mancante, virgolette non chiuse)

**Soluzione:**
1. Apri il file in VS Code
2. Guarda la riga rossa (errore evidenziato)
3. Verifica:
   - Virgole tra oggetti
   - Virgolette aperte/chiuse
   - Niente virgola prima dell'ultimo oggetto

**Validatore online:** https://jsonlint.com (incolla il contenuto, se c'è errore, ti dirà la riga)

### Errore: "Tutti gli articoli Scomparsi"

**Causa:** File `articles.json` è vuoto o corrotto

**Soluzione:**
1. Non panico! Il file è in Git, puoi recuperarlo
2. Terminal: `git checkout blog/articles.json`
3. Ricomincia dall'inizio

### Titolo/Descrizione Non Appare Bene

**Causa:** Caratteri speciali non escapati

**Soluzione:** Se usi `"`, usa l'escape: `\"`

```json
❌ SBAGLIATO: "title": "L'articolo "fantastico""
✅ CORRETTO: "title": "L'articolo \"fantastico\""
```

---

## 🎨 Come Personalizzare il Blog

### Aggregatori di Articoli Consigliati

Se non vuoi gestire articoli locali, usa questi servizi (gratuiti o freemium):

1. **Medium** — Grande community, monetizzazione possibile
2. **Dev.to** — Gratuito, community dev engineers
3. **Hashnode** — Gratuito, customizzabile, analytics
4. **LinkedIn Articles** — Professionale, networking
5. **Substack** — Se vuoi newsletter integrata

Il vantaggio: Scrivi una volta, condividi link nel portfolio. Non devi mantenere il blog nel sito.

---

## 📊 Performance & Best Practices

- ✅ `articles.json` è piccolo (<20KB) e veloce da caricareche
- ✅ Il JavaScript carica asyncronicamente (non blocca il sito)
- ✅ Se non c'è il file, il sito non si rompe (fallback message)
- ✅ Supporta filtri per categoria (automatici da JSON)

---

## 🆘 Hai Domande?

Se qualcosa non è chiaro:
1. Verifica il file `articles.json` con il validatore online
2. Controlla che il formato JSON sia corretto (es. virgolette, virgole)
3. Rileggi questa guida
4. Se continui ad avere problemi, contattami!

---

**Created:** March 2024  
**Last Updated:** March 2024  
**Maintained by:** Mattia Martinelli
