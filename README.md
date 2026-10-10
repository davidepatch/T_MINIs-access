# T_MINIs Beta

**Rilevamento e analisi automatizzati delle correnti postsinaptiche in miniatura**<br>
*Automated detection and analysis of miniature postsynaptic currents*

**Italiano** · [English](#english)

T_MINIs è un programma in Python, con interfaccia grafica, per il rilevamento e l'analisi delle correnti postsinaptiche
in miniatura (mEPSC e mIPSC) in registrazioni whole-cell voltage-clamp continue (file ABF).

T_MINIs impara il criterio con cui un operatore seleziona gli eventi, a partire dalle annotazioni esportate da Clampfit,
e lo applica in modo riproducibile a nuove registrazioni. Per ogni operatore usa tre modelli Random Forest, che
riconoscono l'inizio, la fine e la forma degli eventi; più modelli, addestrati da operatori diversi, possono essere usati
insieme.

L'analisi è organizzata per esperimenti: si definiscono le fasi sperimentali (per esempio controllo, farmaco e lavaggio)
e l'intervallo di ogni fase in ogni registrazione. Per ogni cellula e fase il programma misura ampiezza, cinetica e
frequenza degli eventi e può eseguire l'analisi delle fluttuazioni non stazionarie scalata al picco (ps-NSFA), che stima
la corrente unitaria e il numero di canali aperti al picco, con intervalli di confidenza bootstrap e controlli di
qualità, senza mai riunire gli eventi di cellule diverse. Il report principale raccoglie i risultati di tutte le
cellule, e i report di ogni cellula e fase registrano anche i modelli, i parametri e le soglie usati.

Una documentazione tecnico-scientifica dettagliata, in italiano, giustifica con la letteratura ogni scelta metodologica e
descrive la validazione del programma.

### Stato del progetto

T_MINIs è in versione Beta. È stato validato su registrazioni sintetiche con verità nota; la validazione su
registrazioni reali, con annotazioni indipendenti evento per evento e il confronto con altri programmi, non è ancora
stata fatta. Sono benvenute le collaborazioni con laboratori che registrano mEPSC o mIPSC e con chi si occupa di analisi
dei segnali e di neuroscienze computazionali.

### Licenza

T_MINIs è distribuito con la licenza [PolyForm Strict 1.0.0](https://polyformproject.org/licenses/strict/1.0.0): è
consentito usarlo solo per scopi non commerciali, per esempio da parte di università ed enti di ricerca pubblici, e non
è consentito ridistribuirlo, nemmeno in parte, né modificarlo senza il permesso dell'autore. Il programma è fornito
senza garanzie.

### Come chiedere l'accesso

Il codice e la documentazione sono in un repository privato: l'accesso, anche solo per leggere il codice, viene
concesso dall'autore caso per caso.

1. Accedi a GitHub con l'account che userai per scaricare il codice: serve un account GitHub.
2. Apri una [nuova richiesta di accesso](https://github.com/davidepatch/T_MINIs-access/issues/new?template=richiesta-accesso.yml)
   e compila il modulo.
3. Se la richiesta viene approvata, GitHub ti invia un invito via email e tra le notifiche. Accettalo entro sette
   giorni, poi scade.

Le richieste sono pubbliche, come tutto il contenuto di questa pagina: non scrivere indirizzi email, numeri di telefono
o altri dati personali oltre a quelli chiesti dal modulo.

### Autore

Davide Di Stasio · © 2026

---

## English

T_MINIs is a Python program with a graphical interface for the detection and analysis of miniature postsynaptic
currents (mEPSCs and mIPSCs) in continuous whole-cell voltage-clamp recordings (ABF files).

T_MINIs learns the criterion an operator uses to select events, from annotations exported from Clampfit, and applies
it reproducibly to new recordings. Each operator has three Random Forest models, which recognise the onset, the end and
the shape of events; models trained by different operators can be used together.

Analyses are organised by experiment: the user defines the experimental phases (for example control, drug and washout)
and the interval of each phase in each recording. For each cell and phase the program measures event amplitude,
kinetics and frequency, and can run peak-scaled non-stationary fluctuation analysis (ps-NSFA), which estimates the
unitary current and the number of channels open at the peak, with bootstrap confidence intervals and quality controls,
never pooling events from different cells. The main report collects the results of all cells, and each cell-and-phase
report also records the models, parameters and thresholds used.

Detailed technical and scientific documentation, in Italian, justifies every methodological choice with the literature
and describes how the program was validated.

### Project status

T_MINIs is in Beta. It has been validated on synthetic recordings with known ground truth; validation on real
recordings, against independent event-by-event annotations and other programs, has not been done yet. Collaborations
with laboratories recording mEPSCs or mIPSCs, and with researchers in signal analysis and computational neuroscience,
are welcome.

### License

T_MINIs is distributed under the [PolyForm Strict License 1.0.0](https://polyformproject.org/licenses/strict/1.0.0):
it may be used for noncommercial purposes only, for example by universities and public research institutions, and it
may not be redistributed, in whole or in part, or modified without the author's permission. The software is provided
without warranty.

### How to request access

The code and documentation are kept in a private repository: access, even just to read the code, is granted by the
author on a case-by-case basis.

1. Sign in to GitHub with the account you will use to download the code: a GitHub account is required.
2. Open a [new access request](https://github.com/davidepatch/T_MINIs-access/issues/new?template=richiesta-accesso.yml)
   and fill in the form.
3. If the request is approved, GitHub sends you an invitation by email and in your notifications. Accept it within
   seven days, after which it expires.

Requests are public, like everything on this page: do not include email addresses, phone numbers or any personal data
beyond what the form asks for.

### Author

Davide Di Stasio · © 2026
