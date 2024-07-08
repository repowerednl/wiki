---
title: Release notes
description: Versie informatie van de Battery Simulation Tool
published: true
date: 2024-06-17T13:30:00.000Z
tags: 
editor: markdown
dateCreated: 2024-06-17T13:30:00.000Z
---

# Battery Simulation Tool

_Onderaan de pagina staat welke versie van de BST je nu gebruikt. Komt dit niet overeen met de nieuwste versie? Vernieuw dan de pagina (Ctrl + R)._

## 7 juli: Versie 1.0.00
- Tooltips worden nu gevuld met inhoud uit de Wiki
- Typische zomer- en winterdag SOC (state of charge) van het lopende jaar toegevoegd aan de resultaten pagina. 
- Demo (trial) label is toegevoegd. Dit is voorsorteren op de daadwerkelijke demo versie. 
- Cypress E2E testing is toegevoegd.
- De kleuren van de Sankey grafieken zijn aangepast (PV: #FFC700, Net: #C8D3D9) 
- Titel van de Sankey grafiek in de Energetische Situatie op de resultaten pagina is veranderd van 'Energie Flows' naar 'Energiestromen op jaarbasis'
- Het deployen van de code naar de Dev omgeving is geautomatiseerd middels een workflow. 
- We hebben styling (logo en kleuren) van Novar toegevoegd.
- NTB is verwijderd onder de kolomtekst "Aansturing en optimalisatie".
- Definities vervangen in het Energie Profiel:
    Energie (kWh) = Vermogen (kW)
    Productie = Afname
    Terugleveringcapaciteit = Teruglevering
    Verbruik = Productie
- Extra kleuren toegevoegd voor gebruik in grafieken (#ff870a, #1fc84a en '#408c8b')
- De beschikbaarheid van de aansluiting voor (terug)levering wordt nu getoond bij de resultaten.

#### Bugfixes
- Het is nu mogelijk om simulaties met hoofdletters te zoeken. 
- Het is nu mogelijk om een PV installatie toe te voegen i.c.m geuploade ODN data

## 14 juni: Versie 0.1.29
- De PDF Export is uitgebreid en efficiënter
- Sankey grafieken toegevoegd
- Mogelijkheid om het jaar (2022/2023) en de daarbij horende tarieven te kiezen
- Grafiek met de verwachte SOC (State of Charge) van een typische zomer- en winterdag
- Het is nu mogelijk om screenshots te maken van de gebruikte tabellen

#### Bugfixes
- Het bewerken van een bestaande simulatie mét een geüpload bestand is nu mogelijk.
