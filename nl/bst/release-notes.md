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

## 27 september: Versie 1.4.00

### Features
- Nieuwe versie van de API is in gebruik genomen.
- De mate van het vervagen van de tekst is verminderd bij de financiele situatie wanneer de gebruiker een demo profiel heeft 
- De versie wordt nu meegenomen als release in Sentry.
- De tekst in de tussentijdse berekening stap is aangepast om aan te geven van welke tijdsperiode de kosten zijn gebruikt
- De tekst is aangepast in de financiele situatie tabel. 
- Er is een tooltip toegevoegd voor de 'onbalanskosten' in de tabel van de financiele situatie
- Er zijn unit tests toegevoegd voor de services, helpers en composables
- Er is een 'datepicker' aan stap 1 toegevoegd om het eindjaar én de eindmaand van het financiele jaar te kiezen waarvan de kosten zullen worden gebruikt in de berekening
- De data in de batterij grafiek wordt nu dynamisch weergegeven


## 3 september: Versie 1.3.00

### Features
- Demo functionaliteit toegevoegd. Demo profielen kunnen nu worden aangemaakt. Gebruikers hebben hierbij een simulatie quotum welke een bepaalde tijd zijn te gebruiken. Hierbij zijn bepaalde functies uitgeschakeld. Na deze tijd heeft de gebruiker geen toegang meer tot de BST.


### Bugfixes
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
