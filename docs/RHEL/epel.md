# Cos'è EPEL e come si usa?

E' risaputo che Fedora è l'upstream per le principali versioni di Red Hat Enterprise Linux (RHEL). Si può anche notare che Red Hat distribuisce un set di pacchetti più piccolo per RHEL rispetto a quello che potete con Fedora, questo per una serie di ragioni.

Cosa succede se sei un utente Fedora che vuole anche ImageMagick o Chromium sulla tua workstation RHEL? Potresti voler dare un'occhiata a EPEL.

## Cos'è EPEL e come si usa con le derivate di RHEL?

RHEL viene rilasciata con solo un sottoinsieme di pacchetti che si può trovare in Fedora Linux. Questo ha senso, perché c'è un sacco di software in Fedora che non è necessario in un ambiente aziendale o non rientra nello scopo di RHEL.

Red Hat mantiene e supporta i pacchetti in RHEL molto più a lungo della durata di una release di Fedora, e il software è selezionato per avere successo nell'implementazione e nell'utilizzo di RHEL e derivate e per eseguire i loro carichi di lavoro.

Ma a volte è necessaria qualche applicazione che è disponibile in Fedora ma non in RHEL. Così è stato formato EPEL.

Extra Packages for Enterprise Linux (EPEL) è un gruppo di interesse speciale (SIG) del Fedora Project che fornisce un insieme di pacchetti aggiuntivi per RHEL (e CentOS, Rocky Linux, e altri) dai sorgenti Fedora.

Per portare un pacchetto in EPEL, deve prima esserelo in Fedora.

EPEL segue le Fedora Packaging Guidelines per assicurare un'integrazione corretta, e include solo software libero e open source che non è gravato da brevetti. Quindi non troverete alcun software proprietario in EPEL o cose come i codec multimediali che sono limitati da brevetti, anche se il software che li abilita è sotto una licenza open source.

## EPEL è supportato?

Prima di entrare nel "come" dovremmo probabilmente affrontare la questione del supporto.

EPEL è supportato nella migliore tradizione della comunità open source. ("Se si rompe, puoi tenere entrambi i pezzi")

Vale a dire che EPEL non è supportato nel senso in cui lo è RHEL. Come la maggior parte dei progetti open source (al contrario dell'open source aziendale), è un accordo del tipo "facciamo quello che possiamo" che fornisce un sacco di vantaggi per gli utenti, ma senza la garanzia della rapidità nella produzione di aggiornamenti o del supporto.

Red Hat non supporta i pacchetti in EPEL o non offre nessun SLA intorno ai bugfix o alle patch per i CVE. È anche possibile che i pacchetti in EPEL "vadano e vengano" (per usare il linguaggio del progetto) nel corso di una singola release di RHEL. È possibile che gli aggiornamenti richiedano l'intervento dell'amministratore.

Il progetto EPEL raccomanda agli utenti di EPEL di iscriversi alla mailing list epel-announce per essere al corrente dei prossimi problemi e per avere il tempo di testare prima che l'aggiornamento abbia un impatto.

Questo non significa che EPEL non abbia un posto nel vostro ambiente, solo che dovreste considerare dove e come distribuite i pacchetti da EPEL.

## Cosa è incluso in EPEL?

EPEL è una selezione di pacchetti da Fedora, ma solo pacchetti che non sono in RHEL o nei loro prodotti derivati per evitare conflitti. (Così, per esempio, non troverete in EPEL una versione più recente di qualcosa che è già presente in RHEL)

L'elenco dei pacchetti per EPEL varia a seconda della release e dell'architettura. I pacchetti che sono disponibili per, diciamo, EPEL 7 su x86_64 potrebbero non essere disponibili per EPEL 8 su Power o ARM.

Puoi trovare i link ai set di pacchetti sul Fedora Wiki. I pacchetti non sono automaticamente aggiornati da un rilascio all'altro perché i vari manutentori vogliono aggiungere i loro pacchetti solo quando sono pronti a farlo.

Questo significa che i pacchetti possono richiedere tempo per entrare in una nuova release come EPEL 8.

Attualmente EPEL ha pacchetti per RHEL 6, RHEL 7 e RHEL 8. I pacchetti in EPEL includono cose come i moduli per Python, Perl e altri extra per altri linguaggi di programmazione. Troverete anche utility come etckeeper, ImageMagick e GraphicsMagick, e le build del browser Chromium. (Non è una lista completa, ovviamente)

Per provare EPEL, ecco da dove si può iniziare, le istruzioni sono sul [Fedora Wiki](https://docs.fedoraproject.org/en-US/epel/) per ogni release.

EPEL non è una parte ufficiale dell'universo RHEL o un'offerta ufficiale di Red Hat. Ma può essere utile per gli amministratori e gli sviluppatori che lavorano con RHEL e hanno bisogno di alcune utility preparate per RHEL da una fonte di cui possono sentirsi sicuri.
