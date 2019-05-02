# Structuur "data science"-cursus

## Overzicht leerstof

- Basisbegrippen
    - wetenschappelijke methode
    - beschrijvende statistiek
    - meetniveaus
- Analyse van 1 variabele
    - visualisatie
        - staafdiagram, frequentiediagram
        - box plot, histogram
    - analyse
        - centrummaten, spreidingsmaten
            - kwal: modus
            - quant: gemiddelde/standaardafwijking, mediaan/kwartielen
        - "vorm", bv. "is een verdeling normaal?" Scheefheid, kurtosis, QQ-plot
- Analyse van 2 variabelen
    - visualisatie
        - kwal/kwal: mosaic plot, geclusterde staafdiagrammen, rependiagram
        - kwal/quant: gegroepeerde boxplot
        - quant/quant: xy-diagram (scatterplot), regressierechte
    - analyse
        - kwal/kwal: chi-kwadraat, Cramér's V
        - kwal/quant: effectgrootte (Cohen's d)
        - quant/quant: covariantie, correlatiecoëff, determinatiecoëff, lineaire regressie
- Steekproefonderzoek
    - Steekproefmethodes en -fouten
    - Kansberekening in de normale verdeling
    - Centrale limietstelling
    - Betrouwbaarheidsintervallen
- Statistische toetsen
    - werkwijze
        - Nulhypothese, alternatieve hypothese
        - Teststatistiek
        - Kritiek gebied/overschrijdingskans p
    - z-toets
    - t-toets
    - t-toets van 2 steekproeven
    - chi-kwadraat-toets (voor associatie vs. goodness of fit)
    - Interpretatie, gevaren (zie <https://www.nature.com/articles/d41586-019-00857-9>)
- Tijdreeksen
    - Tijdreeksmodellen
    - Voortschrijdend gemiddelde
    - Exponentiële afvlakking

## In elk hoofdstuk

- Tutorial (met `learnr`, vb. `datascience-box/tutorials`)
    - Concrete leerdoelen
    - Hoofdtekst
        - met uitgewerkte toepassing op een dataset (in R, of .csv)
        - veel vraagjes tussendoor
    - Samenvatting
        - hoofdzaken herhalen
        - overzichtjes (bv. tabel overzicht meetniveaus + visualisatie/analysetechnieken)
- Slides (met `xaringan::moon_reader`, vb. `datascience-box/slides`)
- Labos (oefeningen uit te voeren tijdens de contactmomenten)
    - Voor elk type labo minstens één uitgewerkt voorbeeld met uitgeschreven redenering
    - Uitkomsten van alle oefeningen waar berekeningen bij te pas komen
- Taken (aanvullende oefeningen, zelfstandig uit te voeren buiten de contactmomenten, voorbereiding op het examen)
    - "Uitbreidings"oefeningen: kunnen helpen bij beter begrip van de leerstof, thuis te maken, eerder bijzaak m.b.t. de leerdoelen
    - Oefeningen die helpen bij de voorbereiding op het examen: bv. retrieval practice ("Neem een leeg blad, noteer alle meetniveaus, beschrijf de eigenschappen van elk en illustreer met een voorbeeld.")
    - Voorbeeldexamen
    - Uitkomsten van alle oefeningen waar berekeningen bij te pas komen


## Inhoud

1. Inleiding
    - Lecture
        - Motivatie data science
        - Wetenschappelijke methode
        - Meetniveaus
        - belang van visualisatie, voorbeelden
    - Tutorials
    - Labo
        - Toolset leren kennen: R (cloud), ggplot-voorbeelden uitvoeren
    - Taken
        - Retrieval practice: meetniveaus
        - Rekenen met R, wiskundige formules in R omzetten (learnr tutorial)
2. Analyse van 1 variabele
    - Lecture
        - Visualisatietechnieken (volgens meetniveau)
        - Analysemethoden (centrummaten, spreidingsmaten)
    - Tutorials
        - Intro ggplot
        - Visualisatie- en analysetechnieken in R voor elk meetniveau
    - Labo
        - Oefeningen op visualisatie-/analysetechnieken (incl. voorbeeldoplossingen)
    - Taken
        - Retrieval practice: visualisatie-/analysemethoden t.o.v. meetniveaus
        - Omgaan met dataframes (learnr tutorial)
3. Steekproefonderzoek
    - Lecture
        1. Steekproefmethoden (a/select), steekproeffouten, kansverdeling normale verdeling, schatters (punt~, betrouwbaarheidsinterval)
        2. Centrale limietstelling
    - Tutorial
        - Kansverdeling normale, Student-t verdeling
        - Betrouwbaarheidsintervallen: grote/kleine steekproef en steekproeffractie
    - Labo
        - Casussen steekproefmethoden: Is dit aselect? Welk soort fout wordt hier gemaakt? Kan je steekproefmethode aanpassen zodat fouten vermeden kunnen worden?
        - Kansverdeling normale, t-verdeling: rekenen met `pnorm`, `qnorm`, `pt`, `qt`
        - Betrouwbaarheidsintervallen: grote/kleine steekproef en steekproeffractie
        - Demo centrale limietstelling?
    - Taken:
        - Retrieval practice:
            - geef overzicht van de mogelijke steekproeffouten, leg ze uit en geef een voorbeeld van elk
            - Schets een gausscurve en duid aan: mu, sigma
            - Geef formule voor een betrouwbaarheidsinterval
4. Statistische toetsen
    - Lecture:
        - Terminologie, procedure, overschrijdingskans vs kritiek gebied
        - z-toets (3 varianten), t-toets
        - toetsingsfouten
    - Tutorial
        - z-toets, t-toets in R
    - Labo
        - Oefeningen z-toets, t-toets
    - Taken:
        - Retrieval practice:
            - Schets de Gausscurve van de normale verdeling en duid aan: populatiegemiddelde, steekproefgemiddelde (voorbeeld), overschrijdingskans, aanvaardings/kritiek gebied, kritieke grenswaarde
            - Geef een overzicht van de 3 verschillende varianten van de z-toets: vorm hypothesen, formules voor overschrijdingskans/kritieke grenswaarden
            - Geef een overzicht van de mogelijke toetsingsfouten
5. Analyse van 2 variabelen
    - Lecture
        1. Intro: onafhankelijk vs afhankelijk, correlation is not causation
        2. kwal/kwal: visualisatie (gegroepeerd staafdiagram, rependiagram, mozaïek), analyse (chi-kwadraat, Cramér's V), toets (chi-kwadraattoets voor 2 variabelen)
        3. kwal/quant: visualisatie (boxplot, staafdiagram gemiddelde + errorbar stdev), analyse (Cohen's d), toets (t-test voor 2 steekproeven, [ANOVA](http://www.endmemo.com/program/R/aov.php))
        4. quant/quant: visualisatie (spreidingsdiagram), analyse (lineaire regressie, cov/cor/determinatie), toets (niet in deze cursus)
    - Tutorial
        - voor elke combinatie een uitgewerkte casus
        - aandacht voor analyse onafh/afh variabele afzonderlijk!
    - Labo:
        - Oefeningen op elke combinatie
    - Taken:
        - Retrieval practice:
            - geef overzicht van de mogelijke combinaties onafh/afh variabele
            - geef voor elke combinatie:
                - geschikte visualisatietechnieken
                - geschikte analysemethoden
                - geschikte statistische toets
6. ??? Steekproefonderzoek - vervolg ???
    - Lecture
        - Chi-kwadraat goodness of fit test
        - Is de verdeling van een steekproef normaal? Skewness/kurtosis/QQplot

## Andere aanpassingen

- Voorbeelden uit andere cursussen vervangen (bv. catering.sav)
- Betere integratie slides/R-code/PDF-cursus

## Interessante datasets

- enquête ivm project Gent Sint-Pieters: <https://data.stad.gent/dataset/761> (Codeboek: <https://data.stad.gent/devzone/docs/codeboek-dataset-survey-project-gent-sint-pieters-2018>). Veel categorische data, dus interessant voor kruistabellen, chi-kwadraat.
- Fietstelpaal Visserij: <https://data.stad.gent/data/264>. Tijdreeksanalyse

## Info

- Top 50 ggplot2 visualizations: <http://r-statistics.co/Top50-Ggplot2-Visualizations-MasterList-R-Code.html>
- <https://github.com/rstudio-education/datascience-box>
- <https://datasciencebox.org/>
- <https://evamaerey.github.io/ggplot_flipbook/ggplot_flipbook_xaringan.html#1>
- <https://bookdown.org/yihui/blogdown/>