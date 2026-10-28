# Informativa sulla privacy — MotoLink

**Ultimo aggiornamento: 28 ottobre 2026.**

Questa informativa riguarda l'app Android **MotoLink**, per le funzionalità effettivamente presenti nella versione installata. MotoLink offre mirroring verso display moto compatibili, profili di collegamento e strumenti facoltativi di supporto. Il contatto ufficiale per privacy e assistenza è **[motolinkofficial.app@gmail.com](mailto:motolinkofficial.app@gmail.com)**.

## Dati e impostazioni conservati sul telefono

MotoLink conserva localmente profili moto, dati di collegamento configurati o acquisiti tramite QR, eventuali immagini dei profili scelte dall'utente, app preferite, impostazioni dell'interfaccia, adattamento del display, preferenze e Log tecnico.

Il Log può contenere dati tecnici relativi a dispositivo, moto, rete, connessione o errori. Resta sul telefono finché non viene eliminato tramite **Supporto → Log → Pulisci → Pulisci Log**, cancellazione dei dati dell'app o disinstallazione. Se si utilizza l'Assistente, i token della sessione anonima sono conservati nell'archivio privato dell'app. Salvare un profilo moto non comporta di per sé l'invio dei suoi dati al backend dell'Assistente.

## Log e diagnostica su richiesta

Una normale conversazione con l'Assistente **non invia automaticamente il Log**.

- **Condivisione esterna:** l'utente sceglie di aprire il pannello di condivisione Android e seleziona un destinatario.
- **Condivisione con l'Assistente:** soltanto scegliendo **Supporto → Log → Condividi → Assistente**, viene preparato e allegato un estratto filtrato del Log, limitato a 6.000 caratteri.

MotoLink applica un filtro locale e un secondo filtro lato server. Questi riducono la presenza di informazioni tecniche sensibili ma non garantiscono la rimozione di tutto ciò che l'utente abbia inserito volontariamente. **Non inviare password, token, codici completi o altri dati riservati.**

## Assistente MotoLink e sessioni anonime

L'Assistente è facoltativo e richiede una connessione Internet. Quando viene usato, MotoLink crea una **sessione tecnica anonima** tramite **Supabase Auth**, senza richiedere un profilo nominativo. Il sistema conserva le informazioni di autenticazione necessarie alla sessione.

- Alla pressione di **Invia**, la richiesta HTTPS può contenere testo della domanda (massimo 1.200 caratteri), versione dell'app e, solo su scelta dell'utente, diagnostica filtrata.
- Il backend può rispondere dalla knowledge base MotoLink oppure richiedere una risposta al provider IA **Groq**.
- Il database applicativo MotoLink non conserva cronologia chat, domande, risposte o contenuto dei Log inviati all'Assistente. Mantiene un contatore aggregato giornaliero delle chiamate al provider IA.

Questa precisazione **non** esclude i record di autenticazione gestiti da Supabase o eventuali metadati e log infrastrutturali conservati dai fornitori secondo le loro rispettive condizioni.

## Mirroring, connessione moto, QR e navigazione

- **Mirroring:** Android richiede il consenso **MediaProjection** prima di acquisire lo schermo. I contenuti visualizzati possono comprendere dati personali o notifiche; il flusso viene trasmesso al TFT compatibile tramite connessione locale e **non** viene inviato al backend dell'Assistente.
- **Connessione:** MotoLink usa Wi-Fi, Wi-Fi Direct/P2P e, dove previsto, Bluetooth/BLE per collegarsi al dispositivo moto; alcuni dettagli tecnici possono comparire nel Log locale.
- **QR e fotocamera:** l'associazione può utilizzare Google Code Scanner oppure, come alternativa, lo scanner interno con CameraX. I servizi Google possono trattare metadati tecnici secondo le proprie informative.
- **Google Maps:** solo dopo l'abilitazione dell'accesso alle notifiche, MotoLink interpreta le notifiche di navigazione compatibili di Google Maps per inviare indicazioni al TFT via BLE. L'autorizzazione può essere revocata in Android.

## Fornitori esterni, PayPal e adesivo SOSTENITORE

Per i servizi richiesti dall'utente possono intervenire **Supabase** (autenticazione/backend), **Groq** (IA quando necessaria), **Google/Android** (QR, sistema e navigazione), **PayPal** (pagina esterna per donazioni) e l'app email scelta dall'utente. Questi fornitori possono trattare indirizzi IP e altri metadati tecnici secondo le loro condizioni.

Le donazioni PayPal sono **libere, volontarie** e non sbloccano contenuti o funzionalità digitali. Il pagamento avviene **fuori da MotoLink** sul sito PayPal: l'app non raccoglie direttamente numeri di carta o credenziali di pagamento. Alcune versioni caricano nella pagina Crediti immagini o risorse web PayPal, generando richieste tecniche verso PayPal.

L'eventuale **adesivo fisico MotoLink SOSTENITORE da 6 cm** è un **omaggio facoltativo di ringraziamento, non un acquisto nell'app**. Non è necessario richiederlo per utilizzare MotoLink. Se l'utente sceglie di richiederlo, si apre la propria app email: l'utente decide se comunicare nome, cognome, indirizzo di spedizione e riferimento PayPal facoltativo. Queste informazioni, se inviate, servono per rispondere, verificare manualmente la donazione e, se applicabile, gestire la spedizione. MotoLink non le invia automaticamente attraverso l'app.

Informative dei fornitori: [Supabase](https://supabase.com/privacy), [Groq](https://groq.com/privacy-policy/), [Google](https://policies.google.com/privacy), [PayPal](https://www.paypal.com/it/legalhub/paypal/privacy-full).

## Permessi Android

Secondo le funzioni utilizzate, MotoLink può richiedere Internet/stato rete, Wi-Fi e dispositivi Wi-Fi vicini, Bluetooth/BLE, fotocamera per lo scanner QR di riserva, posizione legacy su Android meno recenti, **MediaProjection**, servizio in primo piano, visualizzazione sopra altre app e wake lock/prossimità. L'accesso alle notifiche per Google Maps richiede un'attivazione separata.

MotoLink non richiede `QUERY_ALL_PACKAGES`: per le app preferite visualizza soltanto applicazioni avviabili. Le autorizzazioni possono essere controllate o revocate dalle impostazioni Android, con possibile limitazione delle relative funzioni.

## Conservazione, cancellazione e contatti privacy

- **Dati locali:** per eliminare il Log usa **Supporto → Log → Pulisci → Pulisci Log**. Per rimuovere anche profili moto, foto, impostazioni e altri dati locali, usa **Impostazioni Android → App → MotoLink → Spazio di archiviazione → Cancella dati** oppure disinstalla l'app.
- **Sessione anonima dell'Assistente:** nelle versioni dotate del comando, vai in **Supporto → Log → Pulisci → Elimina sessione**, poi conferma. La funzione server **già collaudata** verifica l'identità anonima richiesta e ne elimina il record Supabase; dopo conferma il client cancella i token locali. Questa operazione **non** cancella profili moto, impostazioni o Log sul telefono. Un successivo utilizzo dell'Assistente può creare una nuova sessione anonima.
- **Richieste dall'esterno:** consulta la pagina pubblica **[Cancellazione dei dati MotoLink](https://mysterx92.github.io/motolink-privacy/delete-data.html)** o scrivi a **[motolinkofficial.app@gmail.com](mailto:motolinkofficial.app@gmail.com)**. Senza una sessione ancora identificabile, ad esempio dopo disinstallazione, potrebbe non essere tecnicamente possibile associare una richiesta email a un'identità anonima. Non inviare mai token o password per chiedere la cancellazione.

I dati locali restano fino alla pulizia o alla cancellazione dell'app; la sessione Supabase resta finché non viene eliminata. I tempi di conservazione dei log infrastrutturali dei fornitori e delle eventuali email di supporto o spedizione dipendono dai rispettivi sistemi e dalle esigenze di gestione delle richieste. Per informazioni, esercizio dei diritti sulla privacy o richieste di cancellazione contatta MotoLink all'indirizzo sopra indicato. La cancellazione dell'identità Supabase non elimina automaticamente email già inviate o dati presso servizi indipendenti.
