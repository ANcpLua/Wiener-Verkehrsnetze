


# Wiener Verkehrsnetz-UE3-BIF-DUA-2-SS2023-ALGOS-DE

Alexander Nachtmann und Stephanie Rauscher ÜBUNG 3 - (GRAPHEN) aka guide to https://docs.python.org/3/tutorial/modules.html XD

After downloading the .zip extract the files, press the .exe and it should work. If it does not follow the steps below.

Environment PyCharm 2022.3.3 Manual:

1. Download zip by pressing on the green [<> Code] after it finished download drag its content into PycharmProjects
2. Open Pyhcharm select Wiener Verkehrsnetz-UE3-BIF-DUA-2-SS2023-ALGOS-DE-main under Projects
3. Press STRG+ALT+S a window will open where you type interpreter into the top left box
4. Click on Add Interpreter and selected Add Local Interpreter
5. Under Virtualevn Environment select Base interpreter Python310 and click on ok, 38+ should work also
8. Press Shift+F10 to start (recommend to change the hotkey 1.press STRG+ALT+S 2.type run b into the searchbox 3.right click run and select add keyboard shortcut)

    - [Beschreibung des verwendeten Algorithmus](#Beschreibung-des-verwendeten-Algorithmus)
    - [O-Notation](#O-Notation)
    - [Experimente und Messungen zur Laufzeit](#Experimente-und-Messungen-zur-Laufzeit)
  
## SHIFT+F10 in Pycharm  
```
Bitte geben Sie die Startstation ein: Praterstern
Bitte geben Sie die Zielstation ein: Hoechstaedtplatz
Start: Praterstern
Fahre von Praterstern nach Nordbahnstrasse mit Linie 5 (Kosten: 2)
Fahre von Nordbahnstrasse nach Am Tabor mit Linie 5 (Kosten: 4)
Umstieg auf Linie 2 an Station Rebhanngasse
Fahre von Am Tabor nach Rebhanngasse mit Linie 2 (Kosten: 10)
Fahre von Rebhanngasse nach Innstrasse mit Linie 2 (Kosten: 11)
Fahre von Innstrasse nach Traisengasse mit Linie 2 (Kosten: 12)
Fahre von Traisengasse nach Dresdner Strasse mit Linie 2 (Kosten: 14)
Fahre von Dresdner Strasse nach Hoechstaedtplatz mit Linie 2 (Kosten: 15)
Ende: Hoechstaedtplatz
Gesamtkosten: 15
Laufzeit: 0.00200 Sekunden
Möchten Sie weiterfahren (w), neu anfangen (n) oder beenden (x)? 

```  

#### Beschreibung des verwendeten Algorithmus
Der Algorithmus basiert auf einer modifizierten Version des Dijkstra-Algorithmus, wobei eine Vorrangwarteschlange (Heap) verwendet wird, um die Knoten mit den niedrigsten Kosten zu priorisieren. Der Graph wird aus einer Datei eingelesen und in einer dictionay-basierten Datenstruktur gespeichert. Die Funktion shortest_path implementiert den modifizierten Dijkstra-Algorithmus, indem sie die Vorrangwarteschlange verwendet, um den aktuellen Knoten (Station) mit den geringsten Kosten zu finden und diesen Knoten zu erkunden. Um das Umsteigen zwischen Linien zu berücksichtigen, wird eine zusätzliche Kostenkomponente, line_switch_penalty, hinzugefügt, wenn ein Umstieg erforderlich ist. Der Algorithmus terminiert, sobald das Ziel erreicht ist oder keine weiteren Knoten zu erkunden sind.
#### O-Notation
 O(|V|log|V|): 
Einfügen und Entfernen der Knoten aus der Prioritätswarteschlange. Im schlimmsten Fall werden alle Knoten zur Warteschlange hinzugefügt und aus der Warteschlange entfernt, was für jeden Knoten eine Zeit von O(log|V|) in Anspruch nimmt.
O(|E|log|V|):
 Verarbeitung jeder Kante. Im schlimmsten Fall verarbeitet der Algorithmus alle Kanten. Für jede Kante aktualisiert der Algorithmus die Prioritätswarteschlange mit neuen Kosten. Die Aktualisierung der Prioritätswarteschlange kostet O(log|V|) pro Kante.
Daher ergibt sich aus der Kombination dieser Teile die insgesamt Zeitkomplexität von O(|V|log|V| + |E|log|V|).
#### Experimente und Messungen zur Laufzeit
Um die Laufzeit des Algorithmus zu messen, können verschiedene Experimente mit unterschiedlichen Eingabedateien und U-Bahn-Netzwerken durchgeführt werden. Die Laufzeit kann mithilfe der Python time-Bibliothek gemessen werden, indem die Start- und Endzeit vor und nach der Ausführung des Algorithmus erfasst werden. Dabei sollte beachtet werden, dass die tatsächliche Laufzeit von verschiedenen Faktoren abhängt, wie z.B. der Größe des Netzwerks, der Anzahl der Umstiege und der Hardware des Computers, auf dem der Code ausgeführt wird.

Any questions you can contact me on Discord Alex22#8812


