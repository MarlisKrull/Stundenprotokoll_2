<h1 style="color:Navy;"><a id="Übe">Stundenprotokoll zum Projekt: Ladybug-Quest</a></h1>

<hr>
<p><a href="https://marliskrull.github.io/predator-prey-simulation">Den Quelltext sowie die Implementierung finden Sie auf unserer Projekt-Website! </a></p>

<hr>

<table>
<thead>
<tr>
<th>Datum</th>
<th align="center">Fortschritt in den Unterrichtsstunden</th>
</tr>
</thead>
<tbody>
<tr>
<td>16.02.17</td>
<td align="center">Bereits vor der Abgabe der 2. Klausur haben wir uns Gedanken über ein neues Projekt gemacht. Inspiriert vom Biologieunterricht kam die Idee auf, als neues Projekt eine <mark> Räuber-Beute-Simulation </mark> zu gestalten. Dass die Umsetzung dieser Simulation erneut mit Greenfoot erfolgen sollte, war uns von Beginn an klar, da wir uns nun in das Programm gut eingearbeitet haben. Aufgrund der geringen Anzahl der restlichen Unterrichtsstunden, wäre ein Zeitverlust durch das Einarbeiten in ein anderes Programm erheblich gewesen.</td>
</tr>
<tr>
<td>23.02.17</td>
<td align="center">In dieser Stunde haben wir die Simulation mit Greenfoot erstellt. Wir haben <mark> Blattläuse und Marienkäfer </mark> als Actors eingefügt und in der World-Class definiert, dass zu Begin 80 Läuse und 15 Käfer an zufälligen Plätzen in der Welt spawnen. Den Hintergrund der Welt haben wir zudem als grünes Blatt festgelegt. Auch für die Läuse und die Marienkäfer haben wir passende Bilder gesucht und diese zu dem jeweiligen Actor eingefügt. Für beide Actors haben wir eine Bewegungsmethode erstellt, durch welche sie sich zufällig durch die Welt bewegen. Die Marienkäfer laufen schneller als die Läuse, um diese "fangen" zu können. <br> Anschließend haben wir eine <mark> Vermehrungsmethode </mark> erstellt. In dieser vermehren sich die Actors beim Aufeinandertreffen zu einer bestimmten Wahrscheinlichkeit, um es naturgetreu zu halten. Wichtig ist dabei in Hinsicht auf die Simulation, dass sich die Läuse deutlich schneller - also zu einer größeren Wahrscheinlichkeit - vermehren, als die Käfer. <br>
Im anschließenden Testversuch kam es zu einer Überpopulation, sodass wir im nächsten Schritt eine Zeitvariable zur Bestimmung des <mark> Lebensalters </mark> erstellt haben. Sobald diese eine bestimmte Zeit erreicht hat, stirbt der Actor und verschwindet vom Bildschirm. Die Läuse besitzen somit ein sehr kurzes Leben, während die Marienkäfer lange leben. <br> Des Weiteren haben wir eine <mark> Fress-Methode </mark> für die Marienkäfer erstellt, die beim Treffen auf eine Laus abläuft.</td>
</tr>
<tr>
<td>01.03.17</td>
<td align="center">Um alle Faktoren des Lebens zu betrachten, haben wir zunächst eine <mark> "Altersbestimmung" </mark> durch eine Zeitvariable erstellt. Erst ab einem bestimmten Alter , sollten sich die Actors vermehren können, dieses Alter haben wir nach naturgetreuem Verhältnis festgelegt. Das Fortpflanzungsalter der Käfer ist dabei erneut höher, als das der Läuse. Damit die Actors sich dann allerdings nicht alle schlagartig auf einmal vermehren, haben wir das Alter jedes Actors per Zufall definiert. Zudem brauchen die Läuse eine Art Vorlaufzeit, da sie sonst von den Marienkäfern direkt zu Begin gefressen werden, ohne sich vermehren zu können. Diese Zeit haben wir in der Käfermethode als "Zeit zum Fressen" definiert. <br> Weiterhin haben wir <mark> männliche und weibliche Charactere </mark> für beide Actor erstellt. Das Geschlecht wird dabei direkt beim Eintreten eines neuen Actors in die Welt durch Zufall bestimmt. Nur wenn ein männlicher auf einen weiblichen Actor trifft, vermehren sich diese zu der bestimmten Wahrscheinlichkeit. </td>
</tr>
<tr>
<td>02.03.17</td>
<td align="center">Da die Marienkäfer die Blattläuse nicht "erkennen", wenn sich eine Ansammlung von Blattläusen bildet, bevölkern die Läuse stets die gesamte Welt. Um dies zu verhindern, haben wir einen <mark> neuen Actor "Pheromone" </mark> erstellt. Diese Pheromone sollen als Lockspur dienen, sodass die Käfer zu einer vermehrten Anzahl an Läusen laufen. Die Läuse lassen diese Pheromone alle paar Tics "liegen". Für die Pheromone haben wir auch noch eine Zeitvariable erstellt, sodass diese nach einer gewissen Zeit -, wenn der Duft verflogen ist, - automatisch vom Bildschirm verschwinden. <br> Die Marienkäfer registrieren stets die Anzahl der sich in einem Radius um sie befindenen Pheromone. Sobald diese Zahl eine bestimmte Größe erreicht hat, wird zufällig ein Pheromon ausgewählt, zu welchem sich der Marienkäfer schließlich bewegt.</td>
</tr>
<tr>
<td>08.03.17</td>
<td align="center">Nach einem ähnlichen Prinzip haben wir eine Methode erstellt, durch welche sich die Läuse <mark> "tottrampeln" </mark> können, wenn sie zu dicht beieinander sind. Eine Laus registriert dabei alle anderen Läuse, die sich in einem bestimmten Radius um sie befinden. Sobald diese Größe eine bestimmte Anzahl überschreitet, wird mit einer bestimmten Wahrscheinlichkeit die Laus aus der Welt entfernt. <br> Anschließend kam jedoch bei jedem Durchlauf der Simulation die Fehlermeldung: "Actor not in World" mit dem Verweis auf den Befehl, die Läuse in einem Radius aufzulisten. Das Problem hierbei war, dass wir in der "Public void act"-Methode beider Actor die Sterbemethode nicht am Ende verortet hatten. Somit hat Greenfoot stetig versucht Läuse aufzulisten, die bereits gestorben waren. <br> Des Weiteren haben wir in dieser Stunde über den nächsten Abgabetermin der Klausur gesprochen. </td>
</tr>
<tr>
<td>09.03.17</td>
<td align="center">Nach der Einführung der vom 02.03.17 beschrieben Methode, hatten wir das Problem, dass sich die Marienkäfer sobald sie von den Pheromonen angelockt waren, alle komplett identisch verhielten. Sie liefen alle quasi "übereinander" den gleichen Weg ab. Um dies zu ändern, haben wir uns überlegt, dass die Marienkäfer alle paar Tics zufällig ein neues Pheromon zugewiesen bekommen, zu dem sie sich bewegen und nicht wie vorher so lange dorthin laufen, bis sich dieses aufgelöst hat. Dafür haben wir einen neuen Timer erstellt. <br> Desweiteren haben wir eine <mark> "verhungern"-Methode </mark> eingeführt. Bei dieser zählt jeder Marienkäfer, wie viele Läuse er in einem bestimmten Zeitraum gefressen hat. Wenn der Marienkäfer zu wenig gefressen hat, stirbt er. Beim Erstellen dieser Methode haben wir beobachtet, dass die Marienkäfer die Läuse gar nicht mehr fressen, sondern nur über sie hinweglaufen. Im Quelltext haben wir den Fehler gefunden. Die Marienkäfer sollten, wie bereits beschrieben, erst fressen, wenn sie ein bestimmtes Alter erreicht hatten. Da wir den Timer hierfür gleich dem Alter gesetzt hatten, fraßen sie nur bei genau diesem Alter und nicht wenn sie älter waren. Dieses Problem haben wir behoben.</td>
</tr>
<tr>
<td>14.03.17</td>
<td align="center">Es kam die Überlegung auf, die Population beider Actor in einem Diagramm graphisch festzuhalten. Auf diese Weise lässt sich besser erkennen, welche Population sich gerade vermehrt oder dezimiert. Dafür haben wir eine Methode definiert, die alle Objekte in der Welt zählt. Diese Anzahl muss für den neuen Actor <mark> "Graph" </mark> ersichtlich sein. Leider haben wir die Umsetzung des Graphen nur mit drei neuen Actorn zustande gebracht. So gibt es für den Balken jeder Population jeweils einen Actor, der je nach Populationsgröße steigt oder sinkt. Den dritten Actor stellt der Hintergrund hinter dem Graphen dar, da dieser nicht das Blatt, sondern ein einfacher weißer Hintergund sein sollte. <br> Die Einführung dieses Graphen war uns sehr wichtig, sodass wir durch dieses positive Erlebnis weiter gestärkt wurden.</td>
</tr>
<tr>
<td>16.03.17</td>
<td align="center">In dieser Stunde haben wir uns der <mark> Dokumentation </mark> unseres Projektes gewidmet. Wir haben bereits Überschiften erstellt und diese verlinkt. Zudem haben wir dieses Stundenprotokoll verlinkt und einige Texte geschrieben.</td>
</tr>
<tr>
<td>21.03.17</td>
<td align="center">Wir haben uns in dieser Stunde damit befasst, den Actor <mark> "Hintergrund" als Actor zu entfernen </mark> . Um den Hintergrund des Graphen dennoch zu gewährleisten, haben wir in dem World-Editor einen weißen Streifen definiert und diesen lokalisiert. Anschließend kam jedoch das Problem auf, dass die Käfer und Läuse über diesen Hintergrund rübergelaufen sind, als wäre es ein Blatt. Dies sollte jedoch nicht so sein. Wir haben das Problem gelöst indem wir definiert haben, dass sich die Läuse und Käfer um 180° drehen, sobald sie die Grenze des Hintergrundwechsels (x-Achse) erreicht haben.</td>
</tr>
<tr>
<td>23.03.17</td>
<td align="center">Wir haben letzte Änderungen an unserem Projekt und an der Dokumentation getätigt. Die <mark> Abgabe der Klausur </mark> hat stattgefunden.</td>
</tr>
</tbody>
</table>

<hr>

<p style="color:CadetBlue;"><a href="#Übe">zum Seitenanfang</a></p>
