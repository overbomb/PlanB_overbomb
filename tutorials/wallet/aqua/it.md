---
nome: Aqua
descrizione: Bitcoin, Lightning e Liquid in un unico portafoglio
---
![cover](assets/cover.webp)

Aqua è un'applicazione mobile che semplifica la creazione di un hot wallet per Bitcoin e Liquid. Offre anche la possibilità di utilizzare Lightning senza la complessità di gestire un nodo, grazie agli swap integrati. Inoltre consente di gestire USDT su diverse reti.

L'applicazione è sviluppata dalla società JAN3 sotto la direzione di Samson Mow, Aqua è stata inizialmente progettata per le esigenze degli utenti dell'America Latina, anche se è adatta a qualsiasi utente in tutto il mondo. È particolarmente interessante per i principianti e per coloro che utilizzano quotidianamente Bitcoin per i loro pagamenti.

In questo tutorial scopriremo come utilizzare le numerose funzionalità di Aqua. Ma prima di farlo, cerchiamo di capire cos'è una sidechain su Bitcoin e come funziona Liquid, in modo da poter comprendere al meglio il valore di Aqua.

![AQUA](assets/fr/01.webp)

## Cos'è una sidechain?

Il protocollo Bitcoin ha limitazioni tecniche intenzionali che aiutano a mantenere la decentralizzazione della rete ed a garantire che la sicurezza sia distribuita tra tutti gli utenti. Tuttavia, queste limitazioni possono talvolta frustrare gli utenti, soprattutto in caso di congestione dovuta a un elevato volume di transazioni simultanee. Il dibattito sulla scalabilità di Bitcoin ha diviso la comunità per molto tempo, in particolare durante la Blocksize War. Dopo questo episodio, è stato riconosciuto dalla comunità Bitcoin che la scalabilità deve essere garantita da soluzioni off-chain, su sistemi second-layer. Queste soluzioni includono le sidechain, che sono ancora relativamente sconosciute e poco utilizzate rispetto ad altri sistemi come Lightning Network.

Una sidechain è una blockchain indipendente che opera in parallelo alla blockchain principale di Bitcoin. Utilizza bitcoin come unità di conto, grazie ad un meccanismo chiamato "*two-way peg*". Questo sistema permette di bloccare i bitcoin sulla blockchain principale per riprodurne il valore sulla sidechain, dove circolano sotto forma di token con sottostante bitcoin. Questi token mantengono normalmente la parità di valore con i bitcoin bloccati sulla blockchain principale ed il processo può essere invertito per recuperare i fondi su Bitcoin.

L'obiettivo delle sidechain è quello di offrire funzionalità aggiuntive o miglioramenti tecnici, come transazioni più veloci, commissioni più basse o supporto per gli smart contracts. Queste innovazioni non possono sempre essere implementate direttamente sulla blockchain di Bitcoin senza comprometterne la decentralizzazione o la sicurezza. Le sidechain permettono quindi di testare ed esplorare nuove soluzioni preservando l'integrità di Bitcoin. Tuttavia, questi protocolli richiedono spesso dei compromessi, soprattutto in termini di decentralizzazione e sicurezza, a seconda del modello di governance e del meccanismo di consenso scelto.

## Che cos'è liquid?

Liquid è una sidechain federata sovrapposta a Bitcoin, sviluppata da Blockstream per migliorare la velocità, la riservatezza e la funzionalità delle transazioni. Utilizza un meccanismo di ancoraggio bilaterale stabilito su una federazione per bloccare bitcoin sulla blockchain principale e creare Liquid-bitcoin (L-BTC).
![AQUA](assets/fr/02.webp)

La rete Liquid si basa su una federazione di partecipanti, composta da entità riconosciute dell'ecosistema Bitcoin, che convalidano i blocchi e gestiscono il peg bilaterale. Oltre a L-BTC, Liquid consente anche l'emissione di altri asset digitali, come le stablecoin USDT e altre criptovalute.

![AQUA](assets/fr/03.webp)

## Installare l'applicazione Aqua

Il primo passo è scaricare l'applicazione Aqua. Vai sul tuo store di applicazioni:

- [Per Android](https://play.google.com/store/apps/details?id=io.aquawallet.android);
- [Per Apple](https://apps.apple.com/us/app/aqua-wallet/id6468594241).
![AQUA](assets/fr/04.webp)

Per gli utenti Android, è  possibile installare l'applicazione tramite il file `.apk` [disponibile su GitHub] (https://github.com/AquaWallet/aqua-wallet/releases).

![AQUA](assets/fr/05.webp)

Avvia l'applicazione e spunta la casella "*I have read and agreed to the Terms of Service & Privacy Policy*".

![AQUA](assets/fr/06.webp)

## Crea il tuo portafoglio su Aqua

Clicca sul pulsante "*Create Wallet*".

![AQUA](assets/fr/07.webp)

E voilà, il tuo wallet è già stato creato!

![AQUA](assets/fr/08.webp)

Prima di tutto, dato che si tratta di un wallet self-custody, è indispensabile fare un backup fisico del tuo mnemonico. **Questo mnemonico ti dà accesso completo e illimitato a tutti i tuoi bitcoin**. Chiunque sia in possesso di questa mnemonica può rubare i tuoi fondi, anche senza accedere fisicamente al tuo telefono.

Il mnemonico permette di ripristinare l'accesso ai bitcoin in caso di smarrimento, furto o rottura del telefono. È  molto importante salvarlo con cura su un supporto fisico (non digitale) e conservarlo in un luogo sicuro. Puoi scriverlo su un pezzo di carta o, per maggiore sicurezza, se si tratta di un wallet di grandi dimensioni, ti consiglio di inciderlo su un supporto in acciaio inossidabile per proteggerlo dal rischio di incendi, inondazioni o crolli (per un hot wallet progettato per proteggere una piccola quantità di bitcoin, un semplice backup cartaceo probabilmente è sufficiente).

A tal fine, fare clic sul menù Impostazioni.

![AQUA](assets/fr/09.webp)

Quindi fare clic su "*View Seed Phrase*". Esegui un backup fisico di queste 12 parole.

![AQUA](assets/fr/10.webp)

Nel menù delle impostazioni è possibile modificare la lingua dell'applicazione e la valuta fiat utilizzata.

![AQUA](assets/fr/11.webp)

Prima di ricevere i primi bitcoin sul tuo portafoglio, **ti consiglio vivamente di eseguire un test di recupero a vuoto**. Prendi nota di alcune informazioni di riferimento, come il tuo indirizzo xpub o il primo indirizzo di ricezione, quindi cancella il tuo portafoglio dall'applicazione Aqua quando è ancora vuoto. Prova a ripristinare il wallet su Aqua utilizzando il backup cartaceo. Verifica che le informazioni cookie generate dopo il ripristino corrispondano a quelle annotate in origine. Se è così, puoi essere certo che il tuo backup cartaceo è affidabile. Per saperne di più su come effettuare un ripristino di prova, consultate quest'altro tutorial:

https://planb.academy/tutorials/wallet/backup/recovery-test-5a75db51-a6a1-4338-a02a-164a8d91b895

Non è visibile sul mio schermo perché utilizzo un emulatore, ma troverai anche un'opzione nelle impostazioni per bloccare l'applicazione con un sistema di autenticazione biometrica. Consiglio vivamente di attivare questa sicurezza, perché senza di essa chiunque abbia accesso al tuo telefono sbloccato potrebbe rubare i tuoi bitcoin. Puoi utilizzare Face ID su iOS o l'impronta digitale su Android. Se questi metodi fallissero durante l'autenticazione, potresti comunque accedere all'app tramite il codice PIN del tuo telefono.

## Ricevere bitcoin su Aqua

Ora che il tuo wallet è stato configurato, sei pronto a ricevere i tuoi primi Sats! Clicca sul pulsante "*Ricevi*" nel menù "*Wallet*".

![AQUA](assets/fr/12.webp)

Puoi scegliere di ricevere bitcoin onchain, su Liquid o tramite Lightning.

![AQUA](assets/fr/13.webp)

Per le transazioni onchain, Aqua genererà un indirizzo di ricezione specifico dove poter ricevere i Sats.

![AQUA](assets/fr/14.webp)

Allo stesso modo, scegliendo Liquid, Aqua ti fornirà un indirizzo Liquid.

![AQUA](assets/fr/15.webp)

Se preferisci ricevere i fondi tramite Lightning, dovrai prima specificare l'importo desiderato.

![AQUA](assets/fr/16.webp)

Clicca  su "*Generate Invoice*".

![AQUA](assets/fr/17.webp)

Aqua creerà un invoice per ricevere fondi da un wallet Lightning. Nota che, a differenza delle opzioni onchain e Liquid, i fondi ricevuti tramite Lightning saranno automaticamente convertiti in L-BTC su Liquid utilizzando lo strumento Boltz, poiché Aqua non è un nodo Lightning. Questo processo consente di ricevere e inviare fondi tramite Lightning, ma senza memorizzare i bitcoin su Lightning.

![AQUA](assets/fr/18.webp)

Personalmente, inizierò inviando bitcoin via Lightning ad Aqua. Una volta completata la transazione con l'invoice fornito, riceviamo una conferma.

![AQUA](assets/fr/19.webp)

Per seguire l'andamento dello scambio, torna alla pagina iniziale del tuo wallet e fai clic sul conto "*L2 Bitcoin*", che elenca le transazioni Lightning (tramite scambio) e Liquid.

![AQUA](assets/fr/20.webp)

Qui è possibile visualizzare la transazione e il saldo in L-BTC.

![AQUA](assets/fr/21.webp)

## Bitcoin swap con Aqua

Ora che hai delle attività sul tuo wallet Aqua, puoi scambiarle direttamente dall'applicazione, sia per trasferirle alla blockchain principale di Bitcoin, sia per trasferirle a Liquid. Puoi anche convertire i tuoi bitcoin in stablecoin USDT (o altri). Per farlo, vai nel menù "*Marketplace*".

![AQUA](assets/fr/22.webp)

Fare clic su "*Swaps*".

![AQUA](assets/fr/23.webp)

Nella casella "*Transfer from*", selezionare l'attività che desidera negoziare. Al momento possiedo solo L-BTC, quindi è quello che ho selezionato.

![AQUA](assets/fr/24.webp)

Nella casella "*Transfer to*", scegliere l'asset di destinazione per il tuo swap. Per quanto mi riguarda, ho optato per USDT sulla rete Liquid.

![AQUA](assets/fr/25.webp)

Inserire l'importo che si desidera convertire.

![AQUA](assets/fr/26.webp)

Confermare cliccando su "*Continue*".

![AQUA](assets/fr/27.webp)

Assicurati di essere soddisfatto delle impostazioni di swap, quindi conferma trascinando il pulsante "*Swap*" nella parte inferiore dello schermo.

![AQUA](assets/fr/28.webp)

Il tuo scambio è confermato.

![AQUA](assets/fr/29.webp)

Guardando al nostro wallet, possiamo notare che ora abbiamo USDT su Liquid.

![AQUA](assets/fr/30.webp)

## Inviare bitcoin con Aqua

Ora che hai dei bitcoin nel tuo wallet Aqua, puoi inviarli. Clicca sul pulsante "*Send*".

![AQUA](assets/fr/31.webp)

Scegli l'asset che desideri inviare o seleziona la rete per effettuare la transazione. Da parte mia, invierò bitcoin tramite Lightning.

![AQUA](assets/fr/32.webp)

Successivamente, inserisci le informazioni necessarie per inviare il pagamento: per i bitcoin on-chain o Liquid, dovrai inserire un indirizzo di ricezione; per Lightning, è necessaria un invoice. Puoi incollare queste informazioni direttamente nel campo fornito, oppure utilizzare l'icona del codice QR per aprire la fotocamera e scansionare l'indirizzo o l'invoice. Poi fai clic su "*Continue*".

![AQUA](assets/fr/33.webp)

Fare nuovamente clic su "*Continue*" se tutte le informazioni sono corrette.

![AQUA](assets/fr/34.webp)

Aqua presenta un riepilogo della transazione. Assicurati che tutte le informazioni siano corrette, compresi l'indirizzo di destinazione, le spese e l'importo. Per confermare la transazione, far scorrere il pulsante "*Scorri per inviare*" nella parte inferiore dello schermo.

![AQUA](assets/fr/35.webp)

Riceverai la conferma della spedizione.

![AQUA](assets/fr/36.webp)

Ora sai utilizzare l'app Aqua per ricevere e spendere fondi su Bitcoin, Lightning e Liquid, il tutto da un'unica interfaccia.

Se hai trovato utile questo tutorial, ti sarei grato se lasciassi un pollice verde qui sotto. Sentiti libero di condividere questo articolo sui tuoi social network. Ti ringrazio molto!

ti consiglio anche di dare un'occhiata a quest'altro tutorial completo sull'applicazione mobile Blockstream Green, che è un'altra soluzione interessante per impostare il vostro wallet Liquid:

https://planb.academy/tutorials/wallet/mobile/blockstream-app-liquid-b3e4fb82-902e-4782-ad2b-a61ab05a543a

