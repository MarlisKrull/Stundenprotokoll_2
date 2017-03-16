<h1 style="color:Navy;"><a id="Übe">Stundenprotokoll zum Projekt: Ladybug-Quest</a></h1>

<hr>
Den Quelltext sowie die Implementeirung finden Sie auf unserer Projekt-Website:

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
<td align="center">Bereits vor der Abgabe der 2. Klausur, haben wir uns Gedanken über ein neues Projekt gemacht. Inspiriert vom Biologieunterricht kam die Idee auf, als neues Projekt eine Räuber-Beute-Simulation zu gestalten. Dass die Umsetzung dieser Simulation erneut mit Greenfoot erfolgen sollte, war uns von Begin an klar, da wir uns nun in das Programm gut eingearbeitet haben. Aufgrund der geringen Anzahl der restlichen Unterrichtsstunden, wäre ein Zeitverlust durch das Einarbeiten in ein anderes Program erheblich gewesen.</td>
</tr>
<tr>
<td>23.02.17</td>
<td align="center">In dieser Strunde haben wir die Simulation mit Greenfoot erstellt. Wir haben Blattläuse und Marienkäfer als Actor eingefügt und in der World-Class definiert, dass zu Begin 80 Läuse und 15 Käfer an zufälligen Plätzen in der Welt spawnen. Den Hintergrund der Welt haben zudem als grünes Blatt festgelegt. Auch für die Läuse und die Marienkäfer haben wir passende Bilder gesucht und diese zu dem jeweiligen Actor eingefügt. Für beide Actor haben wir eine Bewegungsmethode erstellt, durch welche sie sich zufällig durch die Welt bewegen, jedoch laufen die Marienkäfer schneller als die Läuse, um diese "fangen" zu können. <br> Anschließend haben wir eine Vermehrungsmethode erstellt. In dieser vermehren sich die Actor beim Aufeinandertreffen zu einer bestimmten Wahrscheinlichkeit, um es naturgetreu zu halten. Wichtig ist dabei in Hinsicht auf die Simulation, dass sich die Läuse deutlich schneller - also zu einer größeren Wahrscheinlichkeit - vermehren, als die Käfer. Im anschließenden Testversuch kam es zu einer Überpopulation, sodass wir im nächsten Schritt eine Zeitvariable zur Bestimmung des Lebensalters erstellt haben. Sobald diese eine bestimmte Zeit erreicht hat, stirbt der Actor und verschwindet vom Bildschirm. Die Läuse besitzen somit ein sehr kurzes Leben, während die Marienkäfer lange leben. <br> Desweiteren haben wir eine Fress-Methode für die Marienkäfer erstellt, die beim Treffen auf eine Laus abläuft.</td>
</tr>
<tr>
<td>01.03.17</td>
<td align="center">Um alle Faktoren des Lebens zu betrachten, haben wir zunächst eine "Altersbestimmung" durch eine Zeitvariable erstellt. Erst ab einem bestimmten Alter , sollten sich die Actor vermehren können, dieses Alter haben wir nach naturgetreuem Verhältnis festgelegt. Das Fortpflanzungsalter der Käfer ist dabei erneut höher, als das der Läuse. Damit die Actor sich dann allerdings nicht alle schlagartig auf einmal vermehren, haben wir das Alter jedes Actors per Zufall definiert. Zudem brauchen die Läuse eine Art Vorlaufzeit, da sie sonst von den Marienkäfern direkt zu Begin gefressen werden, ohne sich vermehren zu können. Diese Zeit haben wir in der Käfermethode als "Zeit zum Fressen" definiert. <br> Weiterhin haben wir männliche und weibliche Charactere für beide Actor erstellt. Das Geschlecht wird dabei direkt beim Eintreten eines neuen Actors in die Welt durch Zufall bestimmt. Nur wenn ein männlicher auf einen weiblichen Actor trifft, vermehren sich diese zu der bestimmten Wahrcsheinlichkeit. </td>
</tr>
<tr>
<td>02.03.17</td>
<td align="center">Da die Marienkäfer die Blattläuse nicht "erkennen", wenn sich eine Ansammlung von Blattläusen bildet, bevölkern die Läuse stets die gesamte Welt. Um dies zu verhindern, haben wir einen neuen Actor "Pheromone" erstellt. Diese Pheromone sollen als Lockspur dienen, sodass die Käfer zu einer vermehrten Anzahl an Läusen laufen. Die Läuse lassen diese Pheromone alle paar Tics "liegen". Für die Pheromone haben wir auch noch eine Zeitvariable erstellt, sodass diese nach einer gewissen Zeit -, wenn der Duft verflogen ist, - automatisch vom Bildschirm verschwinden. <br> Die Marienkäfer registrieren stets die Anzahl der sich in einem Radius um sie befindenen Pheromone. Sobald diese Zahl eine bestimmte Größe erreicht hat, wird zufällig ein Pheromon ausgewählt, zu welchem sich der Marienkäfer schließlich bewegt.</td>
</tr>
<tr>
<td>08.03.17</td>
<td align="center">Nach einem ähnlichen Prinzip haben wir eine Methode erstellt, durch welche sich die Läuse "tottrampeln" können, wenn sie zu dicht beieinander sind. Eine Laus registriert dabei alle anderen Läuse, die sich in einem Bestimmten Radius um sie befinden. Sobald diese Größe eine bestimmte Anzahl überschreitet, wird mit einer bestimmten Wahrscheinlichkeit die Laus aus der Welt entfernt. <br> Anschließend kam jedoch bei jedem Durchlauf der Simulation die Fehlermeldung: "Actor not in World" mit dem Verweis auf den Befehl, die Läuse in einem Radius aufzulisten. Das Problem hierbei war, dass wir in der "Public void act"-Methode beider Actor die Sterbenmethode nicht am Ende verortet hatten. Somit hat Greenfoot stetig versucht Läuse aufzulisten, die bereits gestorben waren. <br> Desweiteren haben wir in dieser Stunde über den nächsten Abgabetermin der Klausur gesprochen. </td>
</tr>
<tr>
<td>09.03.17</td>
<td align="center">... </td>
</tr>
<tr>
<td>14.03.17</td>
<td align="center">In dieser Stunde haben wir unsere Projekt-Website gestartet. Wir haben bereits Überschiften erstellt und diese verlinkt. Zudem haben wir dieses Stundenprotokoll verlinkt und mit dem Schreiben der Texte gestartet.</td>
</tr>
<tr>
<td>16.03.17</td>
<td align="center">In dieser Stunde haben wir uns erneut der Dokumentation unseres Projektes gewidmet.</td>
</tr>
<tr>
<td>21.03.17</td>
<td align="center">...</td>
</tr>
<tr>
<td>23.03.17</td>
<td align="center">Abgabe der Klausur</td>
</tr>
</tbody>
</table>

<hr>

<p style="color:CadetBlue;"><a href="#Übe">zum Seitenanfang</a></p>
