---
nome: BIP-85
descrizione: Come posso utilizzare il BIP-85 per generate più seed da un seed principale?
---
![cover](assets/cover.webp)



## 1. Comprendere il BIP-85



### 1.1 Che cos'è il BIP-85?



BIP-85 è una funzione avanzata che consente di creare diversi **seedphrase secondari** da un **seedphrase principale**.



Ogni seedphrase secondario  può essere utilizzato per creare un wallet Bitcoin completamente indipendente. Questi wallet possono essere utilizzati per diversi scopi: un Hot Wallet sul cellulare, un wallet per un parente, un wallet di risparmio separato, ecc.



Tutti i sub seedphrase sono **derivati matematicamente**, ma è **impossibile risalire al seedphrase principale** da un seedphrase secondario. Questo garantisce la completa separazione tra ogni wallet.



Finché si ha accesso al seed principale (ed alla passphrase associata, se se ne usa una), è possibile rigenerare qualsiasi seed secondario in modo **identico**, senza doverla salvare separatamente.



### 1.2 Perché utilizzare il BIP-85?



Il BIP-85 è utile se si desidera :





- creare più wallet Bitcoin indipendenti senza backup multipli;
- gestire i fondi in base ai diversi usi (risparmi, spese, famiglia, progetti);
- garantire le tutele per i parenti (funzione "Uncle Jim");
- cancellare un portafoglio senza perdere l'accesso ai fondi;
- semplificare la sicurezza: solo una seedphrase da proteggere.



### 1.3 Vantaggi rispetto al BIP-32



Con BIP-32, una singola frase seed può essere utilizzata per generate una gerarchia completa di conti e indirizzi Bitcoin, utilizzando percorsi di derivazione (ad esempio: `m/44'/0'/0'/0/0`). Ogni percorso può rappresentare un account separato, ma **tutti rimangono collegati alla stessa frase seed**. Quindi, se questa frase seed viene compromessa, **tutti gli account derivati diventano accessibili**.



Con BIP-85, una frase principale seed può essere utilizzata per generate diverse frasi secondarie seed totalmente indipendenti: **Se uno di questi semi secondari viene compromesso, l'attaccante non sarà mai in grado di tornare al seed principale o di accedere agli altri wallet**.


In questo modo è possibile compartimentare i rischi:





- è possibile utilizzare un seed secondario per un Hot Wallet o per un uso temporaneo, accettando un'esposizione maggiore;
- anche se questo Hot Wallet viene compromesso, gli altri fondi, protetti da altri semi secondari o tenuti offline, **rimangono al sicuro**.



D'altra parte, sia per il BIP-32 che per il BIP-85, se il seed principale viene compromesso, **tutti i fondi sono vulnerabili**. È quindi fondamentale proteggerlo con il massimo livello di sicurezza.



![image](assets/fr/02.webp)


## 2. Casi d'uso pratici per il BIP-85



Il BIP-85 consente di creare più wallet Bitcoin a partire da un'unica seedphrase, ciascuna con la propria seedphrase  secondaria. Ecco cinque casi d'uso pratici per organizzare e proteggere i fondi Bitcoin. Ogni caso spiega perché l'uso di BIP-85 è più pratico della gestione di più seed. 



### 2.1 Limitare il rischio di un wallet meno sicuro





- **Scenario**: Si utilizza un "Hot Wallet" Wallet (installato su un dispositivo connesso a Internet), per le transazioni quotidiane.
- **Soluzione BIP-85**: Si crea una seedphrase secondaria dedicata a questo portafoglio.
- **Vantaggio rispetto al BIP-32**: Non è necessario importare la  seedphrase primaria  sul telefono, riducendo il rischio di hacking. Solo la seedphrase secondaria viene compromessa, proteggendo gli altri wallet. Con BIP-32, è necessario utilizzare la seedphrase principale ed un percorso di bypass, esponendo tutti i fondi.



### 2.2 Creare un wallet per un familiare


- **Scenario**: Si imposta un Bitcoin Wallet per una persona cara (ad esempio, la propria madre), con la possibilità di recuperarlo in caso di smarrimento.
- **Soluzione BIP-85**: Si crea una seedphrase secondaria dedicata e si condivide solo questa.
- **Vantaggio rispetto a BIP-32**: Con BIP-32, la creazione di un conto per una persona cara richiede la condivisione della seedphrase principale, mettendo a rischio tutti i fondi e complicando la gestione per la persona amata (gestione dei percorsi di ramificazione), oppure la creazione di una nuova seedphrase da salvare in aggiunta alla seedphrase principale.



### 2.3 Facilitare la gestione di portafogli separati


- **Scenario**: Separa i tuoi bitcoin per scopi diversi (ad esempio, risparmi a lungo termine, fondi non KYC).
- **Soluzione BIP-85**: Si creano seedphrase secondarie dedicate a ciascun obiettivo.
- **Vantaggio rispetto a BIP-32**: Con BIP-32, tutti i conti condividono la stessa seedphrase, il che complica la gestione nei wallet di terze parti richiedendo la gestione di derivation path come `m/44'/0'/0'`. Inoltre, non è possibile assegnare un conto separato per dispositivo (ad esempio, "risparmi su Coldcard", "giornaliero su cellulare", "vacanze su Trezor"). BIP-85 assegna una seedphrase secondaria unica per obiettivo, che è facile da identificare e importare separatamente su ogni dispositivo.



### 2.4 Utilizzo di un Wallet temporaneo per le transazioni


- **Scenario**: hai bisogno di un wallet temporaneo per una transazione unica o per preservare la riservatezza (ad esempio: mix di UTXO, interazione con un KYC Exchange, ecc.)
- **Soluzione BIP-85**: Si crea una seedphrase secondaria, la si utilizza per la transazione, quindi la si distrugge se necessario, sapendo che può essere rigenerata.
- **Vantaggio rispetto a BIP-32**: Con BIP-32, un conto temporaneo dipende dalla seedphrase principale, esponendo tutti i tuoi fondi se compromessi.





## 3. Prima di iniziare



- **Hardware** (opzionale)
 - Coldcard Mk4 o Q1;
 - scheda MicroSD;
 - conoscenze di base;
 - comprendere le frasi Mnemoniche (BIP-39): un elenco di 12-24 parole per salvare un portfolio;
 - sapere cos'è un Bitcoin Wallet: un software o un dispositivo per la gestione dei bitcoin e come ripristinarlo con una frase Mnemonica;
 - altre risorse negli allegati,
 - software compatibile;
 - Sparrow wallet (computer, per watch-only o la gestione avanzata);
 - Nunchuck (mobile, per le firme multiple);
 - BlueWallet (mobile)
 - ...



**3.4 Configurazione Coldcard**
 - inizializzare una seedphrase di 24 parole sul Coldcard;
 - opzionale: aggiungere una passphrase per proteggere l'accesso ai rami BIP-85;
 - attivare le opzioni utili: NFC (per l'esportazione), disabilitazione dell'USB a batteria (sicurezza).




## 4. Tutorial passo dopo passo



Segui questi passaggi per creare, utilizzare e recuperare un Mnemonico secondario con BIP-85 sul tuo Coldcard.



### 4.1 genera ana seedphrase secondaria



Si creerà una seedphrase secondaria a partire dalla seedphrase principale.


Accendere il Coldcard ed inserire il codice PIN.





- 1. Se si è applicato un passphrase al proprio seed principale:
 - dalla schermata principale, andare su `passphrase`;
    - scegliere `Add Word` e inserire la password;
    - premere `Apply`;
    - controllare l'identità del Wallet: Andare su `Advanced > View Identity` per notare l'impronta digitale del Wallet.





- 2. Andare al menu **BIP-85**
 - nella schermata principale, andare su `Advanced > Derive seed B85`;
 - leggere l'avviso e confermare.



ColdCard informa che i seed generati sono matematicamente derivati dal tuo seed principale, ma crittograficamente totalmente indipendenti.


![image](assets/fr/03.webp)





- 3. Scegliere un formato


Selezionare il formato della frase seed: 12, 18 o 24 parole. Controllare il numero di parole accettate dal Wallet in cui si desidera importare la seedphrase.


![image](assets/fr/04.webp)





- 4. Selezionare l'indice
 - inserire un indice compreso tra 0 e 9999;
 - questo indice è fondamentale per rigenerare il seed secondario in un secondo momento. Conservalo con cura con un'etichetta come: "Indice 1 = Wallet mobile", "Indice 2 = progetto famiglia", "Indice 4 = mixing di prova", ...
 - se lo perdi, non perderai l'accesso ai tuoi fondi, ma dovrai testare le combinazioni da 0 a 9999 per trovarli.


![image](assets/fr/05.webp)





- 5. Nota o esportazione della **seedphrase** secondaria


ColdCard visualizza ora una nuova seedphrase secondaria. È possibile :




 - Scrivi la **nota manualmente**.
 - premi:
     - `1` per salvarlo sulla scheda SD
     - `2` per **inserire la modalità "usa questo seed"** sul ColdCard (utile per esportare o firmare una transazione)
     - `3` per visualizzare un **codice QR** (da scansionare con un'applicazione mobile come BlueWallet o Nunchuck)
     - `4` per inviarlo tramite **NFC**



💡 A questo punto, avete una frase seed indipendente, utilizzabile in qualsiasi Wallet BIP39 (Trezor, Ledger, BlueWallet, Nunchuck...).


![image](assets/fr/06.webp)


![image](assets/fr/07.webp)


### 4.2 Utilizzo del seed secondario



Ora è possibile utilizzare questo seed derivato per creare un nuovo wallet in :




- un'applicazione mobile;
- un altro Hardware Wallet;
- un portafoglio Multisig.



### 4.3 Recupero di una seedphrase secondaria perduta



Per recuperare una seedphrase secondaria in qualsiasi momento, ripetere la procedura:


1. riavviare ColdCard;


2. inserire il PIN;


3. inserire la propria passphrase, se impostata;


4. andare su `Avanzate > Deriva seed B85;


5. scegliere il formato (12/18/24 parole)


6. inserire lo stesso indice (ad es. `1`)


7. Otterrete esattamente lo stesso seed secondario.




## 5. Limiti, rischi e buone pratiche



### 5.1 Dipendenza dalla seedphrase principale + passphrase



L'uso di BIP85 si basa interamente sul seed principale di 24 parole, oltre che su passphrase se ne hai applicata una.




- da questi due Elements si possono rigenerare tutte le seedphrase secodnarie;
- senza uno di questi 2 Elements, si perde l'accesso a tutti i wallet derivati.



### 5.2 Rischi della configurazione multi-firma



Si sconsiglia vivamente di utilizzare seedphrase secodnarie generate dalla seedphrase primaria in una configurazione multi-sig: se il dispositivo o la seedphrase primaria vengono compromessi, tutte le chiavi multi-sig potrebbero essere rigenerate da un utente malintenzionato.



### 5.3 Compatibilità del software



Non tutte le applicazioni supportano direttamente la derivazione BIP85. Tuttavia, i semi generati tramite BIP85 sono semi BIP39 standard (12, 18 o 24 parole) e possono quindi essere utilizzati in qualsiasi portafoglio compatibile con BIP39.



### 5.4 Registro dei conti BIP85



Si raccomanda di tenere un registro personale aggiornato delle seedphrase secondarie,




- consente di scoprire rapidamente quale indice BIP85 corrisponde a quale wallet, senza dover tenere le seedphrase secondarie;
- questo registro deve rimanere minimalista, senza alcuna menzione esplicita a Bitcoin, e deve essere conservato separatamente dal seed principale. Ricordatevi di menzionarlo nel vostro piano di eredità.



Il registro può contenere:


- BIP85 index  (numero da 0 a 9999)
- un nome d'uso o di riferimento (ad esempio Hot Wallet, risparmio personale, wallet della mamma);
- se necessario, l'impronta digitale Wallet per la verifica su ColdCard.



### 5.5 Backup



I backup devono includere :




- il seed principale
- gW-76 (se utilizzato)



Non conservare mai insieme:




- il seed principale e la passphrase
- il seed principale ed il registro dei conti BIP85



Altre risorse negli allegati.




## APPENDICI



## A.1 Glossario





- [BEEP](https://planb.academy/resources/glossary/bip)
- [BIP-32](https://planb.academy/resources/glossary/bip0032)
- [BIP-39](https://planb.academy/resources/glossary/bip0039)
- [BIP-85](https://planb.academy/resources/glossary/bip0085)
- [frase seed](https://planb.academy/resources/glossary/recovery-phrase)
- [passphrase](https://planb.academy/resources/glossary/passphrase-bip39)
- [Multisig](https://planb.academy/resources/glossary/multisig)




### A.2 Salvare la frase di recupero



https://planb.academy/tutorials/wallet/backup/backup-mnemonic-22c0ddfa-fb9f-4e3a-96f9-46e2a7954270


### A.3 Comprensione della passphrase BIP39



https://planb.academy/tutorials/wallet/backup/passphrase-a26a0220-806c-44b4-af14-bafdeb1adce7


### A.4 Come funzionano i wallet Bitcoin



https://planb.academy/courses/46b0ced2-9028-4a61-8fbc-3b005ee8d70f
