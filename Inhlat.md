#  1. Einleitung

### herlich willkom, Mein Name ist Atréus Engelniederhammer, ichs telle euch Heute 
### meine Projektarbeit zum Thema Entwicklung eines Chatbots für Microsoft Teams und die dazugehörige Middleware vor 
### gerichtet ist diese vorstellung an den den Prüfungsauschluss nach dieser kleinen Begrüßung könenn wir auch direkt anfangen

### Ziel war es Informationen zu finden welche wichtig sind für den tägliche gebrauch im Seitwerk und
### um diese dann intuitiver und schneller bereitzustellen als über das Intranet des Seitwerks

# 2. Agenda zeigen

#  3. Projektumfeld 
### die Seitwerk gmbh ist eine Medienagentur mit aktuell 80 Mitarbeitern in den Berreichen Grafikdesign, Multimedia und Entwicklung zu den Dienstleistungen gehören Webseiten sowie Mobile Apps
### gegründet wurde das seitwerk 2004 und liegt derzeit in Uffing am staffelsee 

# Agenda zeigen

# 4. IST zustand
### im Seitwerk wird  alsHauptinformaton quelle das local gehostet Intranet verwendet bzw die weboberfläche davon 
### doch die informations beschaffung gestalltet sich dort nicht sehr effzient und intuitiv verschuldet durch veraltete oberfläche und CMS system 
### nur von innherhalb des netwerks erreichbar und sommit informationenbeschaffung nur begrenzt möglich 

# 5. Soll zustand
### Wichtige Informationen herausfinden um diese dann bereitzustellen 
### Intuitiver und efiizzentes erlangen der informationen 
### Informtionen sicher auch von außen bereitstellen 


# 6. Risikoanalyse 
### dort habe ich versucht alle Risiko Punkte zu erkennen mit den während des Projekts Gerechnet werden muss so  
### Datenschutzrisiken,--- Zugriff von außerhalb auf interne Netzwerke,---- Sicherheitslücken verwendeter systeme ---Sichere Datenübertragung
### diese punkte habe ich zu einer risikoanalyse zusammnegafsst um sie dann mit meinem Projektbegeliter während der Projektplanung zu besprechen wie damit umgegangen werden kann

# 7. Die Projektplanung 
### die projektplannung lief wie folgt ab ich habe mich mit meinem Abteilungsleitern besprochen der viel auf informationen im Intranet zugreifen muss
### sowie Mitarbeitern die überwiegend im support mit kunden arbeiten und mit diesen informationen gesammelt welche öft abgerufen werden müssen und/oder umständlich zu erreichen 
### dabei haben wir uns auf drei verschiedene information gruppen beschrenkt
### persönliche teilnahme an Projekte
### Spezifische informationen zu einem Projekt 
### Informationen über Kunden 



### während der Projektplanung viel noch die entgültige entscheidung als benutzeroberfläche teams zu verwenden da dies als haupt kommunikation mittel in der firma bereits verwndet wird 
### nachdem ich einen groben überblick hatte habe ich dann Aufagben packete erstellt die ich dann abarbeiten konnte bzw vertiefen  


# 8. die architektur planunng 
###  die architektur planunng fand direkt anschluss der besprechung mit den Projektbegleiter statt da ich nun die anforderungen hatte welche umgesetzt werden müssen
### bevor ich darauf eingehe warum ich mich für diese Architektur entschieden habe erkläre ich erstmal an hand des bildes wie der ganze datentransver funktioniert 
### um den vorgegebenen sicherheitsstandarts gerechts zu werden habe ich mich für den einsatz einr Middleware entschieden warum diese in zusammenarbeit mit einer firewall den sicheren transfer von Daten gewährleisten kann 
###  zeige ich nun an diesem Arichtekturplan, """"erklären von wo die daten kommen und wo sie hingehen"""""
### wie hier, wie hier zusehen ist sind die gefahren punkte markiert bei diesem in der mitte ist natürlich das größte risiko da dort jegliche Anfragen aus dem internet kommen können,
### dafür wurde aber die schon vorhandenen firewall so eingestellt dass nur ein fester IP-adressen Berreich von Azure an den port der middlware anfragen darf, dieser ip berreich wird von azure vorgegeben 
wwwwwwwwwww
### nach dem ich dann einen festen Archtektur plan hatte habe ich mich noch für die technologien entschieden die ich dafür brauche da es viele möglichkeite gäbe es umzusetzten 
### grundsätzlich ist alles in javascript geschireben udn ich habe veraschieden erweiterungen noch zusaätzlich verwendet wie 
### nodejs als grundlegende javascript enviroment 
### express.js, ist ein erweiterung für nodejs und bringt funktionien mit um einen http server zu erstellen
### Microsoft bot Framework ist die grundlage für den Teams bot auch eine nodejs erweiterung 
### und das Microsoft tools kit eine erweiterung für den visualstudio Code Editor, die für das testen und deployen des bots benötigt wird 



### NUN KOMMEN WIR zur implentationphase hier werde ich kurz jeden von !!!! die funktiunalität bespechen und auf die sicherheitsvorkehrungen einghen 
### starten wir mit der middlware diese wurde wie schon erwähnt mit node.js und express umgesetzt die express erweiterung gibt einen die möglichkeite routen für einen http server sehr simpel und schnell anzlegen 
### jede route ist jeweils für eine Informations gruppe zusändig also eine die route gibt die informationen für ein spezifische Projekt zurück und einnmal für die kunden und die eignen projkete
### diese routen können in meinem fall über die http methode get erreicht werden und führen dann den dazugehörigen code aus der dann die gewünschtendaten im intranet anfägt 

### das funktioniert so das wenn jemand bzw in dem fall der bot per http methode get und der richtigen routen url an die middlware anfrägt wird der code innherhalb der route ausgeführt  der dann in meinem fall die anfrage der gwüschten daten im Intranet ausführt 
### die schnittstellen im intranet waren bereits vorhanden und es mussleiglich mit den richtigen parametern angefragt werden 
###
