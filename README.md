**Comportamento:

All'avvio: carica prima i dati locali (IndexedDB), poi se connesso a Drive li sovrascrive con quelli cloud
Al salvataggio: salva sia in locale che su Drive automaticamente
Sincronizzazione: ogni modifica viene salvata su Drive in tempo reale
Offline: funziona sempre grazie alla cache locale


⚙️ Come configurare Google Drive
Devi creare un progetto Google Cloud (gratuito):

Vai su https://console.cloud.google.com/
Crea un nuovo progetto (es. "Bank Analyzer")
Nel menu laterale vai su "API e servizi" → "Libreria"
Cerca "Google Drive API" e abilitala
Vai su "Credenziali" → "Crea credenziali" → "ID client OAuth"
Se richiesto, configura la schermata di consenso (tipo "Esterno", inserisci solo i campi obbligatori)
Tipo applicazione: "Applicazione web"
Aggiungi nelle Origini JavaScript autorizzate:

http://localhost (se usi un server locale)
http://127.0.0.1
O il dominio dove ospiti il file


Crea e copia il Client ID
Incolla il Client ID nel codice alla riga:

javascriptconst GOOGLE_CLIENT_ID = 'IL_TUO_CLIENT_ID.apps.googleusercontent.com';
**
