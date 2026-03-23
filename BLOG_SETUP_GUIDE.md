# 📝 Come Aggiungere Articoli al Blog — Guida Step-by-Step

**Questa guida è pensata per un principiante completo. Niente panico! È più facile di quanto sembri.** ✌️

---

## 📚 Scenario Ideale

Immagina di write un articolo su **Medium** o **Dev.to** e vuoi che appaia nel tuo portfolio. Non devi fare niente sul tuo sito se desideri semplicemente linkare l'articolo esterno — il blog si aggiorna in meno di 2 minuti.

---

## ✅ Prerequisiti

- ✓ Un account su Medium, Dev.to, o simile (dove pubblichi l'articolo)
  - **Oppure** — Scritti localmente come file HTML
- ✓ VS Code o un editor di testo (Notepad++, persino il Blocco Note funziona)
- ✓ Git installato (probabilmente già lo hai)

---

# 🚀 METODO FACILE: Aggiungere Articoli da Medium/Dev.to (5 Minuti)

## Passo 1: Scrivi e Pubblica L'Articolo

1. Vai su **Medium.com** o **Dev.to**
2. Scrivi il tuo bellissimo articolo tecnico
3. Pubblica (prendi il **link dell'articolo**, es: `https://medium.com/@tuonome/mio-articolo`)

Esempio:
```
https://medium.com/@mattia/ml-time-series-forecast
```

## Passo 2: Apri il File `blog/articles.json`

**Opzione A (Facile con VS Code):**
```
1. Apri VS Code
2. File → Open Folder → scegli "MattMattw.github.io"
3. Nel pannello sinistro: blog → articles.json (doppio click)
```

**Opzione B (Con Blocco Note):**
```
1. Apri Esplora File di Windows
2. Naviga a: C:\Projects\website\MattMattw.github.io\blog\
3. Tasto destro su articles.json → Apri con → Blocco Note
```

## Passo 3: Copia-Incolla un Template

Nel file `articles.json`, verso la **fine** (prima dell'ultimo `]`), aggiungi questo:

```json
,
{
  "id": "titolo-slug-senza-spazi",
  "title": "Il Titolo del Tuo Articolo",
  "date": "2024-03-23",
  "category": "Machine Learning",
  "tags": ["python", "ml", "tutorial"],
  "description": "Una frase breve che descrive l'articolo in 1-2 righe",
  "author": "Mattia Martinelli",
  "readTime": "10 min",
  "url": "https://medium.com/@tuonome/link-articolo",
  "externalLink": true
}
```

**Compila i campi così:**

| Campo | Cosa mettere | Esempio |
|-------|-------------|---------|
| `id` | Titolo ma in minuscolo senza spazi (usa `-`) | `"ml-forecasting-guide"` |
| `title` | Il vero titolo dell'articolo | `"Machine Learning per Previsioni"` |
| `date` | Data di oggi (YYYY-MM-DD) | `"2024-03-23"` |
| `category` | Una categoria a scelta | `"Machine Learning"` o `"Data Engineering"` |
| `tags` | Parole chiave, divise da virgola | `["python", "ml", "tutorial"]` |
| `description` | 1-2 frasi brevi | `"Come usare XGBoost per previsioni temporali"` |
| `author` | Il tuo nome | `"Mattia Martinelli"` |
| `readTime` | Stima tempo lettura | `"10 min"` o `"12 min"` |
| `url` | Link diretto all'articolo | `"https://medium.com/@mattia/..."` |
| `externalLink` | Sempre `true` per Medium/Dev.to | `true` |

## Passo 4: Salva il File

```
Ctrl + S  (su Windows/Linux)
oppure
Cmd + S   (su Mac)
```

## Passo 5: Pubblica su GitHub

Apri un Terminale/PowerShell nella cartella del progetto:

```bash
cd C:\Projects\website\MattMattw.github.io

git add blog/articles.json
git commit -m "Add blog post: Il Titolo del Tuo Articolo"
git push
```

## Passo 6: Verifica (30 secondi)

1. Attendi 30 secondi
2. Visita: `https://mattmattw.github.io`
3. Scorri fino alla sezione **Blog & Articoli**
4. Vedi il tuo articolo? 🎉 **Fatto!**

---

# 📝 METODO PRO: Articoli Locali nel Sito (15 Minuti)

Se vuoi mantenere gli articoli direttamente nel tuo sito (no Medium/Dev.to):

## Passo 1: Crea il File HTML dell'Articolo

1. Crea una cartella: `blog/articoli/`
2. Dentro crea un file: `blog/articoli/mio-articolo.html`

```html
<!DOCTYPE html>
<html lang="it">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Il Titolo del Mio Articolo</title>
  <style>
    body {
      font-family: 'Georgia', serif;
      line-height: 1.8;
      max-width: 800px;
      margin: 0 auto;
      padding: 40px 20px;
      color: #333;
      background: #f9f9f9;
    }
    article { background: white; padding: 40px; border-radius: 10px; }
    h1 { color: #222; font-size: 2.5em; margin-bottom: 10px; }
    .meta { color: #999; font-size: 0.9em; margin-bottom: 30px; }
    a { color: #0066cc; text-decoration: none; }
    code { 
      background: #f4f4f4;
      padding: 2px 6px;
      border-radius: 3px;
      font-family: 'Courier New', monospace;
    }
  </style>
</head>
<body>
  <article>
    <h1>Il Titolo del Mio Articolo</h1>
    <div class="meta">
      Scritto il 23 Marzo 2024 • 10 min di lettura
    </div>
    
    <h2>Introduzione</h2>
    <p>Scrivi qui il contenuto del tuo articolo...</p>

    <h2>Sezione 1</h2>
    <p>Più dettagli qui...</p>

    <h2>Conclusione</h2>
    <p>Considerazioni finali...</p>

    <hr>
    <p><a href="/index.html#blog">← Torna al Blog</a></p>
  </article>
</body>
</html>
```

## Passo 2: Aggiungi al `blog/articles.json`

```json
,
{
  "id": "mio-articolo-locale",
  "title": "Il Titolo del Mio Articolo",
  "date": "2024-03-23",
  "category": "Machine Learning",
  "tags": ["python", "ml"],
  "description": "Descrizione breve dell'articolo",
  "author": "Mattia Martinelli",
  "readTime": "10 min",
  "url": "blog/articoli/mio-articolo.html",
  "externalLink": false
}
```

**Nota:** `"externalLink": false` perché è ospitato nel tuo sito.

## Passo 3: Salva e Pubblica

```bash
git add blog/articoli/ blog/articles.json
git commit -m "Add blog article: Il Titolo del Mio Articolo"
git push
```

---

# 🎯 Workflow Veloce (La Versione Vera che Userai)

### Non leggere tutorial lunghi. Usa questo:

1. **Scrivi articolo** su Medium/Dev.to
2. **Copia il link** dell'articolo
3. **Apri** `blog/articles.json` in VS Code
4. **Aggiungi questa riga** prima dell'ultimo `]`:
   ```json
   ,{"id":"slug-titolo","title":"Titolo","date":"2024-03-23","category":"Categoria","tags":["tag1"],"description":"Descrizione","author":"Mattia Martinelli","readTime":"10 min","url":"https://medium.com/link","externalLink":true}
   ```
5. **Salva** (Ctrl+S)
6. **Pubblica:**
   ```bash
   git add . && git commit -m "Add article" && git push
   ```
7. **Attendi 30 secondi** → Visita il sito → Done! 🎉

---

# ⚠️ Errori Comuni

### ❌ "Il blog non carica / non vedo l'articolo"

**Causa più comune:** Errore nel JSON (virgola mancante, virgolette non chiuse)

**Soluzione:**
1. Apri **https://jsonlint.com** nel browser
2. **Copia-incolla** il contenuto di `articles.json`
3. Clicca "Validate"
4. Se c'è errore, ti dice la riga esatta
5. Correggi e risalva

**Esempio di errore comune:**
```json
❌ SBAGLIATO:
{
  "title": "Articolo "fantastico"
}
⬆️ Virgolette non chiuse

✅ CORRETTO:
{
  "title": "Articolo \"fantastico\""
}
⬆️ Metti \ prima delle virgolette interne
```

### ❌ "Ho aggiunto l'articolo ma non appare"

**Verifica:**
1. Hai salvato il file? (Ctrl+S)
2. Hai fatto push su GitHub? (`git push`)
3. Sono passati 30 secondi?
4. Hai ricaricato il browser? (Ctrl+F5 per clearare cache)

Se ancora non appare → Valida il JSON con jsonlint.com

---

# 🆘 Cheat Sheet per Copincollare

### Template Veloce — Copia e Modifica

```json
{
  "id": "SLUG-CON-TRATTINI",
  "title": "Il Titolo Dell'Articolo",
  "date": "YYYY-MM-DD",
  "category": "Machine Learning",
  "tags": ["tag1", "tag2", "tag3"],
  "description": "Descrizione breve (100-150 caratteri)",
  "author": "Mattia Martinelli",
  "readTime": "10 min",
  "url": "https://medium.com/@tuonome/articolo",
  "externalLink": true
}
```

### Categorie Suggerite

Scegli una di queste (o aggiungine altre):
```
- Machine Learning
- Data Engineering
- Backend
- Aerospace
- DevOps
- Tutorial
- Deep Dive
```

### Hosting Consigliati per Articoli

| Piattaforma | Pro | Contro |
|-------------|-----|--------|
| **Medium** | Grande community, SEO | Paywalls, meno controllo |
| **Dev.to** | Community dev, gratuito | Meno visibilità rispetto Medium |
| **Hashnode** | Gratuito, customizzabile | Community minore |
| **Substack** | Newsletter integrata | Meno traffico organico |
| **LinkedIn** | Professionale, networking | Breve shelf-life |
| **Blog Locale** | Pieno controllo | Devi mantenere content/hosting |

---

# 🎓 Se Vuoi Saperne Di Più

### Cosa Accade Dietro le Quinte?

1. Scrivi un articolo nel JSON
2. Il JavaScript nel sito legge il file JSON (`blog/articles.json`)
3. Crea automaticamente le "card" (rettangolini) per ogni articolo
4. Quando clicki su una card, ti porta al link dell'articolo
5. Filtra per categoria automaticamente

### Perché JSON?

- **Semplice**: Solo testo, niente database complicato
- **Veloce**: Si carica in millisecondi
- **Scalabile**: Puoi aggiungere 100+ articoli senza problemi
- **GitHub Pages Friendly**: Funziona perfettamente

---

# ✨ Pro Tips

1. **Scrivi titoli chiari** — Non: "Cose di ML" | Sì: "Feature Engineering per XGBoost"
2. **Usa descrizioni accattivanti** — Fai venire voglia di cliccare
3. **Scegli giuste categorie** — Migliora i filtri
4. **Ordina articoli per data** — I più recenti in alto
5. **Backup del JSON** — Fai backup di `articles.json` prima di modifiche importanti (`git` ti aiuta anche se sbagli)

---

# 🔗 Non Dimenticarti Di

- ✅ Aggiungi il link al tuo blog nei tuoi profili (LinkedIn, Twitter, ecc.)
- ✅ Share i tuoi articoli nei social media
- ✅ Rispondi ai commenti
- ✅ Prendi link dai tuoi articoli nei post LinkedIn

---

## 🎉 Hai Finito!

Complimenti! Adesso sai come gestire il tuo blog. Non è scienza missilistica, è letteralmente:

1. Scrivi articolo
2. Aggiungi riga JSON
3. Salva e pubblica
4. Done!

**Buona fortuna con il blog! 📝✨**

---

*Scritto per te da Copilot, Marzo 2024*
