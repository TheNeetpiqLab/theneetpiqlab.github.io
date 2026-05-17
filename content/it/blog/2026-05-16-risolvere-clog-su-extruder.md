---
title: "Risolvere un blocco all'estrusore di una stampante 3D"
summary: "Nello specifico, come risolvere un clog all'estrusore di una Artillery SW X4 Plus S1."
date: 2026-05-16
author: kingsor
categories:
- 3D-Print
tags:
- lessons-from-field
---

Dopo aver fatto manutenzione alla stampante e aver stampato per alcune ore, ad un cambio filamento noto che l'estrusore non carica il filamento. Provo a capire il problema ma un po' per mancanza di tempo, un po' per il fastidio di dover nuovamente risolvere un problema di stampa, abbandono la stampante.

E per una quindicina di giorni non la tocco più. Lo so, non si dovrebbe fare. Ma con le stampanti 3D mi capita. Conto di migliorare e di non farmi più prendere dallo sconforto per così tanto tempo.

Fatto sta che domenica scorsa decido che voglio vedere funzionare nuovamente quella stampante. Quella con il più grande volume di stampa tra quelle che possiedo.

La [Artillery SideWinder X4 Plus S1](https://www.youtube.com/watch?v=19yOoCUahn8), che è una stampante 3D FDM di grande formato e ampio volume di stampa (300x300x400 mm), con [Klipper](https://www.klipper3d.org/) come firmware, guide lineari sugli assi X e Y e un estrusore direct drive dual gear con hotend in ottone.

{{< cards >}}

{{< card >}}
![printing](/img/solving-extruder-clog-on-sw-x4-plus/artillery-sw-x4-plus.jpg "Artillery SideWinder X4 Plus S1")
{{< /card >}}

{{< /cards >}}

Cerco quindi su YouTube un video che descriva come smontare e ripulire l'estrusore della stampante.

E trovo il video giusto dal titolo [Artillery Sidewinder X4 Series | Extruder Clog Troubleshooting Guide](https://www.youtube.com/watch?v=C9Nihv0KN9Y)

Me lo guardo un paio di volte e poi provo a riprodurre il tutto sulla stampante.

So che avrei dovuto fare le foto dei vari passi, ma me ne sono dimenticato perchè totalmente impegnato nelle varie operazioni. Quindi ho realizzato la sequenza fotografica prendendo degli screenshot dal video in questione.

{{< columns count=2 >}}
{{< column >}}
![Rimozione della cover](/img/solving-extruder-clog-on-sw-x4-plus/01-remove-the-cover.png "Rimozione della cover")
Svito le due viti a lato della testina di stampa e rimuovo la copertura.
{{< /column >}}
{{< column >}}
{{< /column >}}
{{< /columns >}}

{{< columns count=2 >}}
{{< column >}}
![Rimozione del motore dell'estrusore](/img/solving-extruder-clog-on-sw-x4-plus/02-remove-the-motor.png "Rimozione del motore dell'estrusore")
Svito le due viti sul motore dell'estrusore e lo rimuovo.
{{< /column >}}
{{< column >}}
{{< /column >}}
{{< /columns >}}

{{< columns count=2 >}}
{{< column >}}
![Sgancio blocco extruder](/img/solving-extruder-clog-on-sw-x4-plus/03-detach-the-extruder.png "Sgancio blocco extruder")
Svito le viti che tengono il blocco estrusore e hotend e li sgancio dal supporto.
{{< /column >}}
{{< column >}}
{{< /column >}}
{{< /columns >}}

{{< columns count=2 >}}
{{< column >}}
![Divido blocco estrusore da blocco hotend](/img/solving-extruder-clog-on-sw-x4-plus/04-take-out-the-extruder-part.png "Divido blocco estrusore da blocco hotend")
Svito le due viti che tengono uniti l'estrusore al blocco hotend.
{{< /column >}}
{{< column >}}
{{< /column >}}
{{< /columns >}}

{{< columns count=2 >}}
{{< column >}}
![Apertura dell'estrusore](/img/solving-extruder-clog-on-sw-x4-plus/05-opening-the-extruder-part.png "Apertura dell'estrusore")
Apro l'estrusore.
{{< /column >}}
{{< column >}}
{{< /column >}}
{{< /columns >}}

{{< columns count=2 >}}
{{< column >}}
![Estrazione ingranaggio estrusore](/img/solving-extruder-clog-on-sw-x4-plus/06-take-off-the-gear.png "Estrazione ingranaggio estrusore")
Estraggo l'ingranaggio dell'estrusore.
{{< /column >}}
{{< column >}}
{{< /column >}}
{{< /columns >}}

{{< columns count=2 >}}
{{< column >}}
![Pulizia dell'estrusore](/img/solving-extruder-clog-on-sw-x4-plus/07-clean-the-extruder.png "Pulizia dell'estrusore")
Rimuovo residui di filamento incastrati nell'estrusore
{{< /column >}}
{{< column >}}
{{< /column >}}
{{< /columns >}}

{{< columns count=2 >}}
{{< column >}}
![Allentare vite dell'hotend](/img/solving-extruder-clog-on-sw-x4-plus/08-loosen-hotend-screw.png "Allentare vite dell'hotend")
Allento la vite che tiene in sede l'hotend.
{{< /column >}}
{{< column >}}
{{< /column >}}
{{< /columns >}}

{{< columns count=2 >}}
{{< column >}}
![Estrazione dell'hotend](/img/solving-extruder-clog-on-sw-x4-plus/09-extract-the-hotend.png "Estrazione dell'hotend")
Estraggo l'hotend e rimuovo eventuali pezzi di filamento rimasti incastrati al suo interno.
{{< /column >}}
{{< column >}}
{{< /column >}}
{{< /columns >}}

{{< columns count=2 >}}
{{< column >}}
![Pulizia dell'hotend](/img/solving-extruder-clog-on-sw-x4-plus/10-clean-the-hotend.png "Pulizia dell'hotend")
Porto la temperatura dell'hotend a 200 gradi e rimuovo eventuali depositi di filamento con l'ago per la pulizia dell'hotend presente nel kit per la manutenzione della stampante
{{< /column >}}
{{< column >}}
{{< /column >}}
{{< /columns >}}

A questo punto dovrei aver rimosso ogni residuo di filamento dall'estrusore e dall'hotend. Rimonto tutto nell'ordine inverso e provo la stampa di un primo layer per capire se ci sono da fare delle configurazioni sul livellamento del piatto e lo z-offset.

Per verificare il livellamento del piatto e il comportamento dell'hotend eseguo la stampa di un primo layer 100x100x0.2 mm.

{{< columns count=2 >}}
{{< column >}}
![Stampa di test del primo layer](/img/solving-extruder-clog-on-sw-x4-plus/first-layer-calibration-02.jpg "Stampa di test del primo layer")
Il risultato di 4 stampe fatte in momenti successivi, con vari aggiustamenti tra una stampa e l'altra.
{{< /column >}}
{{< column >}}
{{< /column >}}
{{< /columns >}}

Il primo test (1) mostra degli spazi tra una linea di filamento e l'altra. Quindi eseguo un allineamento automatico del piatto e lancio la calibrazione dell'input shaping.
Dopo queste due procedure, stampo il secondo test (2). Va meglio ma nella parte centrale ci sono ancora degli spazi tra le linee di filamento.
A questo punto eseguo la calibrazione dello z-offset. Dopo questa calibrazione arrivo al terzo test (3). Le linee di filamento sono ben unite tra loro ma ci sono ancora dei difetti. Mentre sta stampando il terzo test modifico lo z-offset per migliorare il risultato della stampa. E finalmento al quarto test (4) ottengo un risultato per me soddisfacente.


ooOOoo