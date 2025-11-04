

# PROG VIII: Dijkstra Algoritme

Student:

Studentnummer:

## Dijkstra's kortste pad

De bekende Nederlandse informaticus Dijkstra heeft een beroemd algoritme ontwikkeld om het kortste pad te bepalen tussen twee plaatsen. 
Bijvoorbeeld een treinreis tussen Utrecht en Enschede, wel of niet via Amersfoort, een autorit tussen Amsterdam en Marseille, via Brussel of Maastricht, 
maar je kunt "kortste" ook lezen als goedkoopste, bijvoorbeeld bij vliegreizen, of beste, bijvoorbeeld de minste kans op vertragingen. 
Je kunt het Dijkstra-algoritme uitstekend gebruiken om te laten zien dat je OO programmeren goed begrijpt door verschillende type verbindingen te implementeren.

## Opdracht

Implementeer het Dijkstra algoritme om voor een reis het kortste pad te bepalen. 
Je project moet voldoen aan een aantal eisen:
- Je hebt een class diagram in UML gemaakt en geëxporteerd naar pdf
- Het algoritme maakt gebruik van std::priority_queue. Bedenk daarbij: 
  - Waar in de code deze precies voorkomt 
  - Het type dat je aan priority_queue meegeeft moet "comparable" zijn  [zie docs](https://en.cppreference.com/w/cpp/container/priority_queue.html)
- Je maakt gebruik van polymorphism om verschillende soorten verbindingen te kunnen vergelijken en om verschillende implementaties van verval van routes te implementeren. Hiervoor geldt: 
  - Er is in ieder geval een abstract class die een edge representeert, met drie subclasses die staan voor een autorit, treinrit of vlucht.
  - Er is een bewuste keuze gemaakt over wat allemaal vergelijkbaar is met wat
  - Wanneer je een route wil vinden, geef je aan welk type verbindingen allemaal gebruikt mogen worden
  - Er is een functie verval die de graaf update. Deze roep je aan vanuit de graaf, en itereert over alle nodes en edges:
    - Een autorit wordt 1.2x zo lang
    - Een treinrit heeft een kans van 50% om 2x zo lang te worden
    - Een vlucht vervalt niet
    - Reset de benodigde waardes zodat je dijkstra algoritme opnieuw gedraaid kan worden
- Je hebt een oplossing met een testframework dat gebruik maakt van Catch2 die minimaal aantoont dat je algoritme voor onderstaande graaf het juiste antwoord geeft. Waarvoor geldt:
  - Dit moet ook een antwoord zijn dat makkelijk leesbaar is voor anderen bij het draaien
  - Je tests moeten aantonen dat je bepaalde type edges kan uitsluiten
  - Je tests moeten aantonen dat verval degelijk werkt. Voor het testen van functies met random erin is extra zelfstandig onderzoek vereist.
  - Je tests testen zowel randgevallen als de "happy flow"
  - Voor het opzetten van je testframework kan je afkijken bij prog-V Statistically Typed Programming voor de header-only versie of als je geïnteresseerd bent in extra uitdaging en een mogelijk datapunt voor je coding skills leeruitkomst kan je de conventionele manier van het toevoegen van een package aan je C++ project gebruiken en de instructies volgen op [catch2 github](https://github.com/catchorg/Catch2)
  - ![dijkstra](dijkstra_v5.png) 



