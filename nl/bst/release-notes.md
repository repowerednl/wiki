---
title: Release notes
description: Versie informatie van de Battery Simulation Tool
published: true
date: 2024-09-27T14:30:00.000Z
tags: 
editor: markdown
dateCreated: 2024-06-17T13:30:00.000Z
---

# Battery Simulation Tool

_Onderaan de pagina staat welke versie van de BST je nu gebruikt. Komt dit niet overeen met de nieuwste versie? Vernieuw dan de pagina (Ctrl + R)._

## 16 mei: Versie 4.0.0

### Features
- **Marktdata** is geüpdatet t/m april 2025.
- **Data template 2024** toegevoegd.
- De **cashflow diagram** o.b.v. Montel forward curves is nu ook beschikbaar voor de strategie financiële optimalisatie **day-ahead markt**.
- We hebben extra foutmeldingen toegevoegd als er data ontbreekt of niet klopt in het Excel bestand dat is geüpload.
- We hebben de naam van de naam van de strategie ‘Energetische optimalisatie zelflevering’ veranderd naar **‘Optimalisatie uitgestelde levering zonne-energie’.**
- We hebben de omschrijving sectie in het resultaten scherm geüpdatet zodat je een beter overzicht hebt van de gebruikte inputs.
- We hebben de berekening van een aantal financiële KPI’s in de conclusie sectie aangescherpt. Hier kwamen soms verwarrende getallen uit en dat is nu opgelost.



## 14 november: Versie 1.5.00
Vandaag hebben we een nieuwe versie van de BST beschikbaar gemaakt. Het is nu mogelijk om een cashflow diagram te maken o.b.v. Price Forward Curves van Montel en je kunt de inzet van een batterij simuleren op de EPEX day-ahead markt. Daarnaast hebben we een veel gevraagde feature toegevoegd: Geavanceerde instellingen. Hieronder een overzicht van alle updates.

### Features
- Cashflow diagram toegevoegd waarin de netto contante waarde van het batterijsysteem wordt weergegeven wanneer deze wordt ingezet op de onbalansmarkt. De opbrengsten in de toekomst zijn berekend m.b.v. Montel Price Forward Curves. Klik op deze link (Price Forward Curves for energy trading risk management) voor meer info. Op deze manier kunnen we een betere inschatting geven van de terugverdientijd van de investering.
- Strategie toegevoegd waarbij de inzet van de batterij wordt geoptimaliseerd op de EPEX day-ahead markt. Met deze strategie wordt elektriciteit zo goedkoop mogelijk ingekocht en zo duur mogelijk verkocht op de day-ahead markt. Deze strategie wordt (nog) niet toegepast op het Repowered platform wat betekent dat het geen algoritme is dat ook in de praktijk wordt toegepast (zoals dat wel het geval is met de strategie voor de onbalansmarkt).
- Navigatie menu toegevoegd waarmee de gebruiker kan terugkeren naar het hoofdscherm met alle simulaties en een nieuws en contact pagina met informatie over de nieuwste updates.

Ten slotte hebben we geavanceerde instellingen toegevoegd. We geven gebruikers nu nog meer controle over simulaties door meer inputs zelf te kunnen kiezen en invullen. De geavanceerde instellingen kunnen worden geselecteerd in stap 7 en bevatten de volgende parameters:
- Kosten aansturing en optimalisatie
- Vaste maandelijkste kosten (NIEUW: Je kan er nu voor kiezen om additionele vaste maandelijkse kosten mee te nemen)
- Investeringsjaar (NIEUW: Het jaar waarin de investering wordt gedaan (jaar 0). Operatie start vanaf 1 januari in het daarop volgende jaar. Dit wordt meegenomen in het cashflow overzicht wanneer de financiele optimalisatie onbalansmarkt wordt gekozen)
- Disconteringsvoet (NIEUW): Het rekenpercentage dat gebruikt wordt om toekomstige kasstromen contant te maken, om de netto contante waarde te bepalen.
- EIA toepassing
- Onbalansfactor levering (NIEUW): De factor waarmee een inschatting wordt gemaakt van de onbalanskosten voor levering.
- Onbalansfactor teruglevering (NIEUW): De factor waarmee een inschatting wordt gemaakt van de onbalanskosten voor terugleveren.
- Cycli totale levensduur NIEUW: De technische levensduur van de batterij. Deze is afgeschreven na het uitvoeren van dit aantal cycli.
- Teruglevercapaciteit nieuwe situatie (NIEUW): Vul in wanneer de teruglevercapaciteit verandert t.o.v. de huidige situatie.
- Afnamecapaciteit nieuwe situatie (NIEUW): Vul in wanneer de afnamecapaciteit veranderd t.o.v. de huidige situatie. Op deze manier kan rekening worden gehouden met verschillende transportkosten in de huidige en nieuwe situatie.

## 7 november: Bericht over nieuwe features in versie 1.5.00
We gaan volgende week een aantal grote updates doorvoeren in de BST. Ik wil jullie alvast op de hoogte brengen van deze updates en de impact die het zal hebben op de resultaten van simulaties.

### Cashflow diagram over de levensduur van de batterij met inzet op de onbalansmarkt
De afgelopen maanden zijn we bezig geweest met het ontwikkelen van een nieuwe methode voor het berekenen van de terugverdientijd en totale inkomsten van een batterij welke op de onbalansmarkt wordt ingezet. We gaan Price Forward Curves (PFC) van Montel inzetten om een betere inschatting te kunnen maken van de toekomstige inkomsten. Montel is in Europa een gerenommeerde partij voor het leveren van energy market intelligence en het maken van toekomstige markt representaties. We gaan de forward curve van scenario ‘Central’ om een betere inschatting te kunnen geven van de terugverdientijd van een batterij welke op de onbalansmarkt handelt. Elk kwartaal update Montel deze PFC om altijd up-to-date curves te kunnen leveren waar ontwikkelingen op de energiemarkten in zijn meegenomen. Meer informatie over deze PFC en Montel is hier te vinden.

De volgende onderdelen worden meegenomen in de berekening:
Kosten:
- Investeringskosten (CAPEX)
- Operationele kosten (1% van CAPEX),
- Aansturing en optimalisatie
- Transportkosten (We gaan prognose voor toekomstige transportkosten op een later moment toevoegen)
- Vaste maandelijkse kosten (eventueel)

Inkomsten:
- Inkomsten door handel op de onbalansmarkt

Ten slotte, het wordt mogelijk om een Excel bestand te downloaden waar deze kosten en inkomsten per jaar in worden weergegeven.

### Strategie Day-ahead markt
We hebben de afgelopen maanden ook gewerkt aan een nieuwe strategie: optimalisatie op de day-ahead markt. Ten eerste is het belangrijk om te vermelden dat we (nog) geen batterijen daadwerkelijk aansturen op deze markt. Om al wel inzicht te kunnen bieden wat een batterij op deze markt zou kunnen verdienen hebben we een optimalisatie algoritme ontwikkelt speciaal voor de BST. Deze geeft niet perfect weer hoe de batterij in de praktijk zou handelen, maar zit hier wel in de buurt (90-100%). Daarnaast hebben we een aantal aannames moeten doen, welke we in de toekomst verder zullen aanscherpen en verbeteren.

In het financiële overzicht worden de kosten voor inkoop van elektriciteit door de batterij opgeteld bij de ‘Leveringskosten stroom’ en de extra inkomsten worden opgeteld bij ‘Inkomsten teruglevering’.

Met deze update kun je straks dus kiezen tussen 3 verschillende optimalisaties:
- Financiële optimalisatie onbalansmarkt                 (voorheen: Financiële optimalisatie)
- Energetische optimalisatie zelflevering                (voorheen: Zelfvoorzienendheid)
- Financiële optimalisatie day-ahead markt               (Nieuw)

Ik houd jullie op de hoogte wanneer deze features volgende week zijn toegevoegd. Als jullie in de tussentijd vragen of opmerkingen hebben dan hoor ik het graag.

## 27 september: Versie 1.4.00

### Features
Nu de zomerperiode achter ons is draait de ontwikkeling van de BST weer op volle toeren. We werken aan een aantal grote updates welke in de komende maand beschikbaar zullen komen. 

Vanmorgen hebben we de volgende updates doorgevoerd:
- We hebben de mogelijkheid toegevoegd om simulaties uit te voeren met recente markt data uit 2024. In stap 1 bij het aanmaken van een nieuwe simulatie kun je nu een maand te selecteren van januari 2020 t/m juli 2024. Bij het selecteren van bijv. juli 2024 zal automatisch marktdata worden opgehaald tot een jaar terug, in dit geval van augustus 2023 t/m 2024. Zo kunnen nu simulaties uitgevoerd worden met de meest recente beschikbare data. De marktdata zullen we periodiek blijven updaten.
- We hebben een aantal tekstuele wijzigingen doorgevoerd in de financiele situatie op het resultaten scherm zodat duidelijker is wat er onder transportkosten, onbalanskosten en energiebelasting valt.
- We hebben in de achterkant de API structuur aangepast wat zal zorgen voor een stabielere verbindingen.

Als je vragen hebt over deze updates of andere vragen over de BST dan hoor ik het graag.


## 3 september: Versie 1.3.00

### Features
Deze week hebben we weer een aantal bugfixes en updates gerealesed voor de Battery Simulation Tool. In verhouding wat minder nieuwe toevoegingen, omdat we bezig zijn met een aantal grotere projecten. Hier zullen we na de zomer meer over laten weten.

De volgende updates zijn live gezet:
- Waarschuwing negatieve ODN en BPM waarden. Wanneer er negatieve waarden zijn ingevuld in de Excel template zal er nu een waarschuwing worden gegeven aan het einde van stap 3. Daarnaast is aan de Excel template toegevoegd dat in deze kolommen positieve waarden ingevuld moeten worden.

### Bugfixes
- Negatieve terugverdientijd: Wanneer er geen terugverdientijd mogelijk is zal een '-' worden weergegeven
- Wijzigen naam simulatie: In sommige situaties werd bij het wijzigen van de simulatie naam deze niet overal gewijzigd. Dat is nu opgelost.
- De waarde van het geselecteerde marktjaar wordt nu goed doorgegeven. 
- Het probleem met de 'wachtwoord vergeten' functie is verholpen.
- Het veranderen van het marktjaar in een bestaande simulatie zorgt er voor dat de tussentijdse berekening opnieuw wordt gedaan.

## 7 juli: Versie 1.0.00

### Features
Vandaag hebben we een nieuwe versie van de Battery Simulation Tool gereleased. We hebben de volgende features toegevoegd of gewijzigd:
- Financiële berekening zelfvoorzienende strategie is gecorrigeerd;
- Energiebelasting voor het laden van de batterij van het net wordt niet meer meegenomen vanwege vrijstelling op energiebelasting;
- De beschikbaarheid van de aansluiting voor de batterij wordt nu getoond bij de resultaten.

Aanpassingen aan grafieken:
- Y-as label energieprofiel aangepast naar vermogen in kW;
- Naamgeving van grafieken in energieprofiel aangepast;
- Y-as van grafiek zomer- en winterdag aangepast;
- Titel van de Sankey diagram in de Energetische situatie veranderd naar 'Energiestromen op jaarbasis';
- De kleuren van de Sankey diagram zijn aangepast;

Later deze week implementeren we ook de volgende aanpassingen:
- Power signal van de batterij wordt toegevoegd aan de zomer- en winterdag;
- ‘Levensduur batterij’ wordt verwijderd en vervangen door ‘Resterende cycli na bereiken terugverdientijd’;
- Mogelijkheid om kosten voor aansturing en optimalisatie mee te nemen in de financiële berekening.

### Bugfixes
- De tooltips zijn nu uitgelijnd met de bijbehorende tekst
- Het is nu mogelijk om simulaties met hoofdletters te zoeken. 
- Het is nu mogelijk om een PV installatie toe te voegen i.c.m geuploade ODN data

## 14 juni: Versie 0.1.29
- De PDF Export is uitgebreid en efficiënter
- Sankey grafieken toegevoegd
- Mogelijkheid om het jaar (2022/2023) en de daarbij horende tarieven te kiezen
- Grafiek met de verwachte SOC (State of Charge) van een typische zomer- en winterdag
- Het is nu mogelijk om screenshots te maken van de gebruikte tabellen

### Bugfixes
- Het bewerken van een bestaande simulatie mét een geüpload bestand is nu mogelijk.
