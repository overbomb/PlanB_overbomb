---
nome: Ashigaru
descrizione: Il fork di Samourai Wallet per proteggere, gestire e miscelare i bitcoin
---

![cover](assets/cover.webp)



Ashigaru è un'applicazione Bitcoin mobile wallet che segue il progetto Samourai Wallet, ma in una nuova forma. Questo software è nato in un contesto particolare: nell'aprile 2024, i fondatori di Samourai Wallet sono stati arrestati dalle autorità americane e i loro server sono stati sequestrati. Sebbene l'applicazione Samurai sia rimasta utilizzabile, attualmente non viene più mantenuta. Ashigaru è una versione gratuita fork di Samurai Wallet, mantenuta da un team anonimo per garantire la continuità delle funzionalità di Samurai e salvaguardare la sua filosofia originaria: difendere la privacy e la sovranità degli utenti di Bitcoin.



Ashigaru riprende molto del DNA di Samourai: un'interfaccia simile, self-custody, open source e con attenzione alla privacy. Il codice è distribuito sotto la licenza GNU GPLv3, che garantisce che chiunque possa controllare, modificare o ridistribuire il software.



L'applicazione Ashigaru integra una serie di strumenti avanzati per la riservatezza e la gestione dei tuoi UTXO:




- **Whirlpool**, è un protocollo di coinjoin basato su Zerolink, che consente di interrompere i legami deterministici tra le entrate e le uscite delle transazioni, senza perdere la sovranità sui propri fondi;
- **PayNym**, che implementa codici di pagamento riutilizzabili (BIP47), ora rappresentati tramite un sistema di avatar "*Pepehash*";
- **Ricochet**, una funzione che aggiunge salti intermedi alle transazioni per renderle più difficili da tracciare;
- **Coin Control** per selezionare, congelare ed etichettare con precisione gli UTXO;
- **Batch Spending**, per ridurre i costi raggruppando diversi pagamenti in un'unica transazione;
- **Stealth**, modalità che nasconde l'applicazione sul cellulare dietro un launcher fittizio per passare inosservata durante un'ispezione fisica del telefono;
- strumenti di spesa avanzati per ottimizzare la vostra riservatezza (payjoin, stonewall...);
- un sistema di recupero ottimizzato che utilizza la passphrase BIP39;
- un sistema per ottimizzare automaticamente la scelta delle commissioni di transazione.



![Image](assets/fr/01.webp)



Ashigaru si rivolge ad utenti consapevoli delle problematiche legate alla tracciabilità delle transazioni su Bitcoin. Che siate utenti attenti alla privacy, bitcoiner esperti impegnati nell'autocustodia o individui esposti ai rischi di una maggiore sorveglianza, questa applicazione per il wallet ti fornisce gli strumenti necessari per riprendere il controllo della vostra attività sul Bitcoin.



Ashigaru è disponibile in versione mobile tramite la sua applicazione, che esploreremo in questo tutorial. Ma può essere utilizzato anche sul PC con ***Ashigaru Terminal***, che presenteremo in un prossimo tutorial.



![Image](assets/fr/02.webp)



In questo tutorial, ti mostrerò le basi dell’utilizzo di Ashigaru. Ti guiderò attraverso l’installazione, la connessione al Dojo, il backup dei dati e le operazioni di ricezione e invio di bitcoin. Per gli strumenti avanzati, sarà disponibile una serie di tutorial specifici in seguito.



## 1. Prerequisiti per Ashigaru



L'applicazione richiede alcuni prerequisiti per funzionare correttamente. Innanzitutto, non è un'applicazione disponibile sui classici store come Google Play Store o App Store. Si installa manualmente sul telefono dal suo file `.apk`, scaricabile tramite la rete Tor. Pertanto, se si utilizza un iPhone, questo metodo non funziona: è necessario un dispositivo Android.



Per scaricare il file `.apk` tramite Tor, è necessario un browser in grado di accedere ai siti `.onion`. Il modo più semplice è installare l'applicazione Tor Browser sul proprio telefono, disponibile sul [Google Play Store](https://play.google.com/store/apps/details?id=org.torproject.torbrowser) o direttamente [tramite il suo `.apk`](https://www.torproject.org/download/#android).



![Image](assets/fr/03.webp)



La maggior parte degli smartphone recenti blocca per impostazione predefinita l'installazione di applicazioni provenienti da fonti sconosciute. È necessario attivare temporaneamente questa opzione nelle impostazioni del dispositivo per consentire l'installazione di Tor Browser. Una volta installata l'applicazione, ricordatevi di disattivare questa funzione per rafforzare la sicurezza del vostro telefono.



Un altro prerequisito essenziale per l'utilizzo di Ashigaru è avere un nodo Bitcoin Dojo. Per motivi di sicurezza, il team di Ashigaru non gestisce un server centralizzato a cui collegare la vostra applicazione. Dovrete quindi gestire la vostra istanza Dojo o collegarvi a una istanza fidata.



Il Dojo consente all'applicazione Ashigaru di consultare le informazioni della blockchain, visualizzare i tuoi UTXO e trasmettere le transazioni sulla rete Bitcoin.



Per saperne di più su Dojo e imparare a installarlo, vi invito a seguire questo tutorial dedicato:



https://planb.academy/tutorials/node/bitcoin/dojo-aa818a21-e701-48a2-8421-63c6186ed23f

Se proprio non potete permettervi di gestire un vostro Dojo, potete trovare persone disposte a condividere gratuitamente la loro istanza su [dojobay.pw](https://www.dojobay.pw/mainnet/). Questa può essere una soluzione temporanea, ma a lungo termine vi consiglio di usare il vostro Dojo per garantire la vostra sovranità e riservatezza.



## 2. Controllare e installare l'applicazione Ashigaru



### 2.1. Scaricare l'applicazione Ashigaru



Sul telefono, aprire Tor Browser e andare su [il sito ufficiale di Ashigaru] (https://ashigaru.rs/download/), nella sezione `Download`. Quindi fare clic sul pulsante `Download for Android` per scaricare il file di installazione.



![Image](assets/fr/04.webp)



Prima di installare l'applicazione sul dispositivo, ne verificheremo l'autenticità e l'integrità. Si tratta di un passaggio molto importante, soprattutto quando si installa un'applicazione direttamente da un file `.apk'.



### 2.2. Controllare l'applicazione Ashigaru



Tornare al [sito ufficiale di Ashigaru] (https://ashigaru.rs/download/) nella sezione `Download`, quindi copiare il messaggio visualizzato sotto il titolo `SHA-256 Hash del file APK`. Copiare l'intero blocco, da `BEGIN PGP SIGNED MESSAGE` a `END PGP SIGNATURE`.



![Image](assets/fr/05.webp)



Sempre dal telefono, aprite una nuova scheda in Tor Browser e andate a [lo strumento di verifica di Keybase](https://keybase.io/verify). Incollate il messaggio appena copiato nell'apposito campo, quindi fate clic sul pulsante "Verifica".



![Image](assets/fr/06.webp)



Se la firma è autentica, Keybase visualizzerà un messaggio che conferma che il file è stato firmato dagli sviluppatori di Ashigaru. È inoltre possibile fare clic sul profilo `ashigarudev` indicato da Keybase e verificare che l'impronta digitale della chiave corrisponda esattamente a : `A138 06B1 FA2A 676B`.



Tuttavia, se in questa fase compare un errore, significa che la firma non è valida. In questo caso, **non installare l'APK**. Ricominciare dall'inizio o chiedere aiuto alla comunità prima di continuare.



![Image](assets/fr/07.webp)



Keybase vi ha fornito l'hash dell'applicazione. Verifichiamo ora che l'hash del file `.apk' scaricato corrisponda a quello verificato su Keybase. Per farlo, andate su [HASH FILE ONLINE](https://hash-file.online/).



![Image](assets/fr/08.webp)



Fate clic sul pulsante `BROWSE...` e selezionate il file `.apk` scaricato al punto 2.1.


Scegliere quindi la funzione hash `SHA-256` e fare clic su `CALCULATE HASH` per calcolare l'hash del file.



![Image](assets/fr/09.webp)



Il sito visualizzerà l'hash del vostro file `.apk`. Confrontatelo con l'hash verificato su Keybase.io. Se i due hash sono identici, la verifica dell'autenticità e dell'integrità ha avuto successo. A questo punto è possibile procedere all'installazione dell'applicazione.



![Image](assets/fr/10.webp)



### 2.3. installare l'applicazione Ashigaru



Per installare l'applicazione, aprire il file manager del telefono e andare alla cartella dei download. Quindi fare clic sul file `.apk` appena controllato e confermare l'installazione quando richiesto.



![Image](assets/fr/11.webp)



Ashigaru è  installato sul vostro telefono.



## 3. Inizializzare l'applicazione e creare un wallet Bitcoin



Quando si avvia l'applicazione per la prima volta, selezionare `MAINNET`.



![Image](assets/fr/12.webp)



Quindi fare clic su "Get Started".



![Image](assets/fr/13.webp)



Ora creeremo un nuovo wallet Bitcoin. Premere il pulsante "Create a new wallet".



![Image](assets/fr/14.webp)



### 3.1. creare un wallet Bitcoin



Ashigaru richiede un passphrase BIP39. Scegliete la vostra passphrase e inseritela nei campi appropriati. Deve essere il più lungo e casuale possibile per resistere ad un brute-force attack.



Eseguire immediatamente un backup fisico di questo passphrase. Si tratta di un passo molto importante: in caso di smarrimento del telefono, **se non si dispone più di questa passphrase, non sarà più possibile accedere ai bitcoin** memorizzati con il wallet Ashigaru. Questa passphrase viene utilizzato anche per crittografare il file di recupero del wallet.



Se non sai cos'è una passphrase o non ne comprendi appieno il funzionamento, ti consiglio vivamente di leggere questo ulteriore tutorial. È importante, perché la passphrase è un elemento critico per la tua sicurezza: un'incomprensione del suo utilizzo potrebbe comportare la perdita permanente dei tuoi fondi.



https://planb.academy/tutorials/wallet/backup/passphrase-a26a0220-806c-44b4-af14-bafdeb1adce7

Una volta inserito la passphrase, fare clic su `NEXT`.



![Image](assets/fr/15.webp)



Scegli un codice PIN. Questo codice verrà utilizzato per sbloccare il wallet Ashigaru, proteggendolo dall'accesso fisico non autorizzato. Non partecipa alla derivazione crittografica delle chiavi del wallet. Ciò significa che, anche senza conoscere il codice PIN, chiunque abbia la tua frase mnemonica e la passphrase sarà in grado di riavere accesso ai tuoi bitcoin.



Opta per un codice PIN lungo e casuale. Ricordati di tenere una copia di backup in un luogo separato dal telefono, per evitare che vengano compromessi contemporaneamente.



![Image](assets/fr/16.webp)



Una volta creato il codice PIN, Ashigaru visualizza la frase mnemonica del wallet. Attenzione: questa frase, combinata con la passphrase, dà pieno accesso ai bitcoin. Chiunque ne sia in possesso può impossessarsi dei tuoi fondi, anche senza avere accesso al tuo telefono. Questa sequenza di 12 parole può essere utilizzata per ripristinare il wallet in caso di perdita, furto o rottura del telefono. È importante conservarla con la massima cura su un supporto fisico (carta o metallo).



Non salvare mai questa frase in formato digitale, poiché potresti esporre i tuoi fondi al rischio di furto. A seconda della tua strategia di sicurezza, puoi creare diverse copie fisiche, ma non dividetele mai. Mantenete le parole nell'ordine esatto e assicuratihe siano numerate.



Infine, non conservare mai il mnemonico e la passphrase nello stesso posto. Se entrambi venissero compromessi contemporaneamente, un malintenzionato potrebbe accedere al wallet.



![Image](assets/fr/17.webp)



Per saperne di più su come proteggere la tua frase mnemonica, consulta questo tutorial complementare:



https://planb.academy/tutorials/wallet/backup/backup-mnemonic-22c0ddfa-fb9f-4e3a-96f9-46e2a7954270

Ashigaru chiede di riconfermare la propria passphrase. Cogli l'occasione per verificare che il tuo backup fisico sia corretto.



![Image](assets/fr/18.webp)



### 3.2. collegare un dojo



Successivamente, si passa alla fase di connessione al Dojo. Come spiegato nell'introduzione, per interagire con la rete Bitcoin, l'Ashigaru deve essere collegato a un Dojo.



Accedere allo "Strumento di manutenzione" del proprio Dojo e aprire il menù "PAIRING".



![Image](assets/fr/19.webp)



Su Ashigaru, premere il pulsante "Scan QR", quindi scansionare il codice QR di connessione visualizzato dal DMT. Quindi fare clic su "Continue" per confermare.



![Image](assets/fr/20.webp)



Immettere il codice PIN per sbloccare il wallet. Si accede così alla pagina di sincronizzazione. È normale che in questa fase vengano visualizzati errori *PayNym*, poiché il wallet è nuovo. Fare semplicemente clic su "Continue".



![Image](assets/fr/21.webp)



Verrà visualizzata la pagina iniziale del wallet.



![Image](assets/fr/22.webp)



Prima di proseguire, ti consiglio di effettuare un ripristino di prova quando il wallet non contiene ancora bitcoin. In questo modo verificarai che i backup cartacei funzionino correttamente. Per sapere come fare, segui questo tutorial:



https://planb.academy/tutorials/wallet/backup/recovery-test-5a75db51-a6a1-4338-a02a-164a8d91b895

## 4. Impostazione dell'applicazione Ashigaru



Per accedere alle impostazioni dell'applicazione, clicca sull'immagine del tuo *PayNym* nell'angolo in alto a sinistra e selezionare "Settings".



![Image](assets/fr/23.webp)



Qui troverai diverse opzioni per adattare il funzionamento di Ashigaru alle tue esigenze. Tuttavia, ti consiglio vivamente di attivare fin dall'inizio due parametri importanti.



Apri il menù `Security > Stealth mode`, attiva questa funzione se ne hai bisogno. Questa funzione nasconde l'applicazione Ashigaru dietro il nome, il logo e l'interfaccia di una normale applicazione installata sul telefono. Lo scopo è quello di impedire a chiunque di identificare Ashigaru in caso di ispezione fisica del telefono.



![Image](assets/fr/24.webp)



Ogni applicazione falsa offerta ha un metodo specifico per sbloccare la vera interfaccia Ashigaru. Ad esempio, se si sceglie la calcolatrice, l'applicazione Ashigaru scompare dalla schermata iniziale e viene sostituita da una finta calcolatrice. Quando la si apre, si vede la classica interfaccia di una calcolatrice funzionante, ma per accedere ad Ashigaru è sufficiente toccare cinque volte velocemente il simbolo `=`.



Il secondo parametro importante da attivare è [**RBF** (*Replace-by-Fee*)](https://planb.academy/resources/glossary/rbf-replacebyfee). Questa opzione consente di aumentare il costo di una transazione se questa rimane bloccata nei mempool perché il costo è troppo basso. È possibile attivarla tramite il menù `Transactions > Spend using RBF`.



![Image](assets/fr/25.webp)



Suggerimento: è possibile cambiare l'unità di visualizzazione del wallet da `BTC` a `sat` semplicemente facendo clic sul saldo totale visualizzato nella pagina iniziale.



## 5. Ricevere bitcoin su Ashigaru



Ora che il wallet è operativo, è possibile ricevere i sats. Per farlo, premere il pulsante `+` in basso a destra dell'interfaccia, quindi il pulsante verde `Receive`.



![Image](assets/fr/26.webp)



Ashigaru ti mostra il primo indirizzo di ricezione inutilizzato nel tuo wallet, per evitare il riutilizzo dell'indirizzo (il riutilizzo dell'indirizzo è una pratica molto negativa per la privacy). È possibile inoltrare questo indirizzo alla persona o al servizio che deve inviare bitcoin.



![Image](assets/fr/27.webp)



Una volta trasmessa in rete, la transazione apparirà automaticamente sulla pagina iniziale dell'applicazione.



![Image](assets/fr/28.webp)



## 6. Inviare bitcoin con Ashigaru



Ora che hai dei bitcoin sul tuo Ashigaru wallet, puoi anche inviarli. Per farlo, premere il pulsante `+` in basso a destra, quindi selezionare il pulsante rosso `Send`.



![Image](assets/fr/29.webp)



Scegli il conto dal quale desideri effettuare la spesa. Per il momento non abbiamo ancora affrontato il conto `Postmix`, riservato alle coinjoin, di cui ci occuperemo in un prossimo tutorial. Invia i fondi dal conto di deposito principale.



![Image](assets/fr/30.webp)



Inserisci i dettagli della transazione: l'importo da inviare e l'indirizzo Bitcoin del destinatario.



![Image](assets/fr/31.webp)



Facendo clic sui tre puntini nell'angolo in alto a destra e poi su "Mostra uscite non spese", puoi scegliere con precisione quali UTXO desideri spendere, per migliorare la propria privacy.



![Image](assets/fr/32.webp)



Una volta compilati tutti i dettagli, fare clic sulla freccia bianca in fondo all'interfaccia per continuare.



Si ha accesso ad una pagina di riepilogo che mostra tutti i dettagli della transazione. Vengono visualizzati diversi elementi importanti:




- nel blocco `Destination`, verificare un'ultima volta che l'indirizzo del destinatario e l'importo inviato siano corretti;
- nel blocco `Fees`, è possibile visualizzare la tariffa selezionata automaticamente da Ashigaru e, se necessario, modificarla cliccando su `MANAGE`;
- Il blocco `Transaction` indica il tipo di transazione che si sta per eseguire. In questo caso, parliamo di una transazione semplice, ma Ashigaru supporta anche altri tipi di transazioni ottimizzate per la privacy, di cui parleremo in dettaglio in un prossimo tutorial;
- Il blocco rosso `Transaction Alert` avverte l'utente se la transazione mostra schemi che possono essere riconosciuti dagli strumenti di chain analysis che potrebbero compromettere la tua privacy. Facendo clic su Transaction Alert, è possibile visualizzare i dettagli. Ad esempio, nel mio caso, Ashigaru mi dice che l'importo inviato è rotondo (`3000 sats`), permettendomi di dedurre quale uscita corrisponde alla spesa e quale allo scambio. Per saperne di più su queste euristiche di chain analysis, ti invito a seguire la mia formazione su BTC 204 su Plan ₿ Academy;
- Infine, è possibile aggiungere un'etichetta alla transazione per tenere traccia del suo scopo.



https://planb.academy/courses/65c138b0-4161-4958-bbe3-c12916bc959c

Dopo aver controllato tutte le informazioni, utilizza la freccia verde per inviare i bitcoin. Tenere premuta la freccia e trascinarla verso destra per confermare il caricamento.



![Image](assets/fr/33.webp)



La tua transazione è stata trasmessa sulla rete Bitcoin.



![Image](assets/fr/34.webp)



## 7. Recupero dell'Ashigaru wallet



Il recupero di un Ashigaru wallet differisce leggermente da quello di un Bitcoin wallet classico, poiché l'applicazione utilizza gli stessi metodi del Samurai Wallet. Se si perde l'accesso al wallet (perché si è dimenticato il PIN, si è disinstallato o si è perso il telefono), ci sono diversi modi per recuperare i bitcoin.



Se avete ancora accesso al vostro telefono o se avete fatto una copia di backup di questo file, il metodo più semplice è usare il file di backup `ashigaru.txt`. Questo file contiene tutte le informazioni necessarie per ripristinare il wallet su una nuova istanza di Ashigaru (o su Sparrow Wallet), ma è criptato con la passphrase definita al punto 3.1 di questo tutorial. È quindi necessario disporre sia del file `ashigaru.txt` che della passphrase per utilizzare questo metodo.



Con questi due elementi è possibile, ad esempio, ripristinare il wallet su Sparrow Wallet.



![Image](assets/fr/35.webp)



Se non avete accesso al file `ashigaru.txt`, potete comunque recuperare l'accesso ai tuoi fondi usando la tua frase mnemonica e la passphrase, proprio come faresti per qualsiasi altro wallet Bitcoin. Ti consiglio di eseguire questo ripristino su una nuova istanza Ashigaru o su Sparrow Wallet, per recuperare facilmente i percorsi di bypass dal Whirlpool se lo stavate utilizzando. In alternativa, è possibile importare queste informazioni in qualsiasi altro software compatibile con BIP39 inserendo manualmente i percorsi di derivazione.



Per ulteriori informazioni su questa procedura, consultare il tutorial completo che ho scritto sul recupero di un Wallet Samurai wallet. Poiché l'Ashigaru è un fork e la procedura è identica:



https://planb.academy/tutorials/wallet/backup/samourai-recover-23bb6221-ea3e-42e6-a5b7-e6dbef5073c3

Come si può notare, qualunque sia il metodo di ripristino utilizzato, la passphrase è indispensabile. Assicurati di eseguire un backup accurato. È possibile creare diverse copie, a seconda della propria strategia di sicurezza.



## 8. Aggiornamento dell'applicazione



Per aggiornare l'app Ashigaru, dato che l'avete installata da un file `.apk` e non tramite il Play Store come una normale app, dovrete scaricare il nuovo file `.apk` corrispondente alla versione aggiornata ed installarlo manualmente.



Ripetete i passaggi descritti nella sezione 2 di questa guida, ma quando fate clic sul file `.apk` per avviare l'installazione, **il vostro telefono Android dovrebbe offrirvi l'opzione `Update` e non `Install`**.



![Image](assets/fr/41.webp)



Questo è un punto molto importante: se Android visualizza `Install` invece di `Update`, probabilmente si sta installando una versione fraudolenta. In questo caso, interrompete immediatamente la procedura di installazione.



Come per la prima installazione, verificare l'autenticità e l'integrità del file `.apk` prima di procedere con l'aggiornamento.



Per sapere quando è disponibile una nuova versione, controllate di tanto in tanto il sito ufficiale di Ashigaru. Siate certi che Ashigaru è un'applicazione stabile e matura, ereditata da Samourai Wallet, e gli aggiornamenti sono relativamente poco frequenti rispetto ai software più recenti.



## 9. Donazione al progetto Ashigaru



Ashigaru è un progetto open-source. Se vuoi sostenere il suo sviluppo, puoi fare una donazione direttamente dall'applicazione tramite PayNym.



Per farlo, clicca sul tuo PayNym in alto a destra dell'interfaccia e seleziona il codice di pagamento che inizia con `PM...`.



![Image](assets/fr/36.webp)



Premi il pulsante `+` in basso a destra dello schermo.



![Image](assets/fr/37.webp)



Seleziona `Ashigaru Open Source Project` come destinatario.



![Image](assets/fr/38.webp)



Fai clic sul pulsante `CONNECT` per stabilire il canale di comunicazione BIP47 (ulteriori informazioni su questo protocollo sono riportate nel tutorial sottostante).



https://planb.academy/tutorials/privacy/on-chain/paynym-bip47-a492a70b-50eb-4f95-a766-bae2c5535093

![Image](assets/fr/39.webp)



Una volta confermata la transazione di notifica, è possibile inviare le donazioni al progetto facendo clic sulla piccola freccia bianca nell'angolo in alto a destra dell'interfaccia.



![Image](assets/fr/40.webp)



Ora sai come utilizzare le funzioni di base dell'applicazione Ashigaru. Nelle prossime esercitazioni vedremo come sfruttare le transazioni di spesa avanzate, oltre a Whirlpool, l'implementazione del coinjoin ereditata da Samurai Wallet.
https://planb.academy/tutorials/privacy/on-chain/ashigaru-terminal-9a0d46d3-33b9-4c64-84c5-bfa25b3a0add
