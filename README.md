# La rete delle ontologie ISPRA

Questo repository include la cosiddetta **rete delle ontologie ISPRA** ([*Istituto Superiore per la Protezione e la Ricerca Ambientale*](https://www.isprambiente.gov.it/it)). La rete delle ontologie è organizzato in moduli ontologici che permettono di rappresentare i diversi concetti contenuti nei dati ambientali: stazioni di monitoraggio, osservazioni, indicatori, nonché features geografiche e amministrative associate all'informazione ambientale.

## Moduli costituenti la rete delle ontologie ISPRA
Al momento fanno parte della rete i seguenti moduli ontologici. Li presentiamo brevemente di seguito.

### [Ontologia Top](https://w3id.org/italia/env/onto/top)

Il modulo TOP definisce i concetti e le proprietà di più alto livello che vengono poi specializzati nei moduli sottostanti. Ad esempio, l’ontologia definisce classi come Concept, Collection, e Location che sono molto generiche, ma allo stesso tempo forniscono dei concetti di supporto per la definizione di classi più di dettaglio negli altri moduli. Il namespace del modulo TOP è https://w3id.org/italia/env/onto/top/

### [Ontologia Place](https://w3id.org/italia/env/onto/place)

Il modulo PLACE estende il modulo TOP aggiungendo classi e proprietà che descrivono in maniera più dettagliata i luoghi sia dal punto di vista fisico che nella loro accezione amministrativa. 
Di conseguenza tali classi sono modellate come sottoclassi di ispra-top:Location tramite l’utilizzo dell’assioma rdfs:subClassOf. In maniera analoga il modulo TOP è esteso modellando tutta una serie di proprietà (ex. :hasAdministrativeUnit, :hasCountry, ecc…) come sottoproprietà della object property ispra-top:hasLocation tramite l’utlizzo dell’assioma rdfs:subPropertyOf. Il namespace del modulo TOP è https://w3id.org/italia/env/onto/place/.

### [Ontologia Inspire-mf](https://w3id.org/italia/env/onto/inspire-mf)

Il modulo INSPIRE-MF modella le classi e le proprietà che rappresentano il modello dati INSPIRE rilevante per il dominio dei dati ISPRA rappresentati attualmente secondo il paradigma dei Linked Data. In particolare il modulo ontologico rappresenta oggetti istanze della classe MonitoringObject nelle diverse possibili alternative, come MonitoringFacility e MonitoringNetwork. Il modulo presenta inoltre classi e proprietà che descrivono osservazioni, collezioni di osservazioni, sensori, piattaforme, reti, parametri di osservazione, procedure, valori, etc. Il modulo è ispirato alle ontologie SSN e SOSA (estendendole in taluni casi, ad es. se si desidera utilizzare serie di osservazioni - Classe ObservationSeries) ed all’ontologia sull’Internet of Things (IoT) di OntoPiA. 
Sono anche  modellate le classi e le proprietà per rappresentare indicatori e collezioni di indicatori. La caratterizzazione temporale e geografica dell’indicatore è demandata alla collezione di indicatori. Questa soluzione è stata adottata per contenere nel dataset finale il numero di triple RDF che riguardano appunto la caratterizzazione temporale e geografica degli indicatori utilizzando la collezione come raggruppamento per indicatori che sono stati ottenuti nello stesso luogo e allo stesso tempo. Il modulo INSPIRE-MF importa direttamente il modulo TOP. Il namespace del modulo INSPIRE-MF è https://w3id.org/italia/env/onto/inspire-mf/.


### [Ontologia Rendis](https://w3id.org/italia/env/onto/rendis)
La rete di ontologie ISPRA è stata estesa con il modulo ontologico RENDIS che modella la conoscenza riguardante il Repertorio Nazionale degli interventi per la Difesa del Suolo. Il namespace del modulo RENDIS è https://w3id.org/italia/env/onto/rendis/.

## Licenza
Tutti i moduli ontologici sono rilasciati sotto la licenza aperta Creative Commons Attribution 4.0