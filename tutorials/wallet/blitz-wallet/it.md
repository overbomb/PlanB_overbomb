---
nome: Blitz Wallet


description: Il wallet Bitcoin più semplice.
---
![cover](assets/cover.webp)



L'esperienza d'uso è uno dei fattori decisivi quando si tratta di iniziare ad usare con un Wallet. In questo tutorial vi presenteremo un Wallet che ha fatto della sua esperienza d'uso un fattore decisivo: Blitz Wallet offre il wallet Bitcoin più semplice e completo che si possa trovare.



## Che cos'è il Blitz Wallet?



Blitz Wallet è un wallet Bitcoin self-custody (detieni le chiavi private per l'accesso ai tuoi bitcoin) il cui codice sorgente è disponibile (Open Source), che si concentra sulla tua sovranità e su un'esperienza d'uso che lo rende semplice da usare.



[Blitz Wallet](https://blitz-Wallet.com/) è un Wallet mobile disponibile su Android (Play Store) e iOS (App Store).



⚠️**IMPORTANTE**: Scaricare un Bitcoin Wallet su una piattaforma ufficiale è importante per verificare l'autenticità dell'applicazione e, di conseguenza, per rafforzare la sicurezza dei tuoi fondi.



In questo tutorial ci baseremo sulla versione Android di Blitz Wallet, ma tutti i processi presentati di seguito sono ugualmente validi su iOS.



![installation](assets/fr/01.webp)



Poiché Blitz Wallet è un wallet self-custodial, puoi scegliere di creare un nuovo wallet o importare le parole di recupero 12/24 da un wallet già esistente.



In questo caso, iniziamo con la creazione di un nuovo wallet. Vedere di seguito le nostre raccomandazioni per il backup delle frasi di backup.



https://planb.academy/tutorials/wallet/backup/backup-mnemonic-22c0ddfa-fb9f-4e3a-96f9-46e2a7954270

iMPORTANTE: Queste 12 / 24 parole di recupero sono essenziali per accedere ai tuoi bitcoin. Se le perdi, non sarai più autorizzato a spendere i tuoi bitcoin.



"Not your keys, not your bitcoins".




Crea un codice PIN per autenticare l'accesso al proprio Wallet.



![setup-wallet](assets/fr/02.webp)



## Come iniziare con Blitz



Il trading con Blitz è più intuitivo rispetto a quello della maggior parte degli altri wallet Bitcoin.



Nel menù del Wallet, l'interfaccia è minimalista e si concentra esclusivamente sulle azioni principali:



### Ricevere bitcoin



Per ricevere bitcoin sul tuo Blitz Wallet, fai clic sull'icona "Freccia giù", inserisci l'importo in satoshi che desideri ricevere e il Wallet creerà un Invoice da condividere con il mittente.



⚠️ **NOTE**: Satoshi (o "sat") rappresenta l'unità più piccola di Bitcoin: 1 Bitcoin = 100.000.000 satoshi



Una delle caratteristiche speciali di Blitz Wallet è che supporta reti e canali diversi dell'ecosistema Bitcoin:





- **Lightning Network**: Un second layer di Bitcoin che consente di effettuare microtransazioni istantaneamente.





- **Bitcoin Mainnet**: La blockchain principale del protocollo Bitcoin, adatta a transazioni di grande valore.





- **Liquid Network**: Una chain parallela alla Bitcoin Mainnet sviluppata da BlockStream che utilizza Liquid Bitcoin (LBTC) per eseguire operazioni veloci.
  

https://planb.academy/tutorials/wallet/mobile/blockstream-app-liquid-b3e4fb82-902e-4782-ad2b-a61ab05a543a

Per impostazione predefinita, tutte le transazioni avverranno su Liquid Network, ma Blitz consente di definire la rete su cui si desidera ricevere i satoshi facendo clic sul pulsante **Choose format**.



![receive-sats](assets/fr/03.webp)



### Creare contatti con Blitz



Blitz Wallet consente di inviare facilmente bitcoin.



Nel menù **Contacts** è possibile registrare i nomi utente Blitz o gli URL Lightning con cui si interagisce maggiormente.



In questo modo è possibile inviare facilmente i satoshis a questi indirizzi, evitando la fase di scansione e di inserimento manuale del address.



![add-contacts](assets/fr/04.webp)



### Inviare bitcoin



Oltre ai metodi classici di invio di Bitcoin (codice QR, inserimento manuale), utilizzando i contatti pre-registrati nel tuo Wallet, puoi inviare Sats al tuo destinatario in soli tre clic.



Nel menù **Wallet**, clicca sul pulsante "Up Arrow", scegliere il metodo di invio dei bitcoin, inserire l'importo da inviare e procedere con la conferma.



L'importo minimo per inviare Bitcoin in Blitz Wallet è attualmente di 1.000 satoshi.



![send-bitcoin](assets/fr/05.webp)



## Il negozio Blitz



Oltre alle operazioni di trasferimento Bitcoin, Blitz Wallet offre un negozio dove è possibile utilizzare bitcoin per pagare i servizi digitali.





- **Accesso ai servizi di intelligenza artificiale**: Utilizzae modelli di intelligenza artificiale generativa come: Claude 3-5 sonnet, gpt-4o, gpt-4o-mini gemini-flash-1.5 e paga direttamente in bitcoin.



![ia-credits](assets/fr/06.webp)





- **Invia messaggi di testo in tutto il mondo**: Nel negozio Blitz, hai accesso ad un servizio GSM che ti permette di inviare messaggi di testo in forma anonima in tutto il mondo, con addebito diretto in Bitcoin.



![sms-credit](assets/fr/07.webp)





- **Naviga in totale riservatezza**: Paga un abbonamento WireGuard VPN (Virtual Private Network) nel negozio Wallet Blitz con bitcoin.



![wireguard](assets/fr/08.webp)



https://planb.academy/tutorials/exchange/centralized/bitrefill-8c588412-1bfc-465b-9bca-e647a647fbc1

https://planb.academy/tutorials/wallet/mobile/speed-wallet-8715e454-1720-4a7f-8c1d-3da02cf67312

## Blitz Wallet dietro le quinte: Andare oltre



Dietro la semplicità del funzionamento di Blitz Wallet si nasconde una grande quantità di potenza e personalizzazione.



Come abbiamo sottolineato in precedenza, tutti i bitcoin che si ricevono hanno come valore predefinito Liquid Network.



Blitz utilizza i microscambi Liquid Network per presentare il saldo in Satoshi quando il saldo è inferiore a 500.000 satoshi.



Questo approccio è giustificato dal desiderio di facilitare l'esperienza di avvio e di aiutare i nuovi utenti a effettuare transazioni su Lightning Network con piccoli importi nel modo più semplice possibile.



https://planb.academy/tutorials/wallet/mobile/aqua-8e6d7dd3-8c03-45cc-90dd-fe3899a7d125

È possibile visualizzare la ripartizione del saldo nel menù **Settings>Balance Info**.



![balance](assets/fr/09.webp)



Blitz Wallet offre tuttavia la possibilità di attivare la modalità Lightning, che apre automaticamente un canale di pagamento una volta raggiunto un saldo di 500.000 satoshi.



Per attivare la modalità Lightning, accedere a **Settings**, quindi nella sezione **Technical Settings** fare clic sull'opzione **Node Info**.



![enable-lightning](assets/fr/10.webp)



Attivando la modalità Lightning, una volta soddisfatta la condizione principale (saldo di 500.000 satoshi o 0,005 Bitcoin), si potranno effettuare transazioni su Lightning Network e non si dovrà più passare per Liquid Network di BlockStream.





- **Accettare Bitcoin nel proprio negozio**:



L'integrazione dei pagamenti Bitcoin nei negozi è ancora in fase di sperimentazione con Blitz Wallet. Si consiglia di utilizzarla con parsimonia.



Nel menù **Settings>Point-of-sale** è possibile impostare l'identificativo univoco associato al proprio negozio e la valuta fiat locale in cui si desidera ricevere i pagamenti.



![pos](assets/fr/11.webp)



Se questo tutorial ti ha aiutato a familiarizzare con Blitz, siamo sicuri che ti piacerà altrettanto il tutorial su Muun Wallet. Scopri Muun, un Wallet semplice e potente come  Bitcoin.



https://planb.academy/tutorials/wallet/mobile/muun-111b56b0-4872-4130-ad2e-e58f8363451d
