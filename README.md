# Adventure-Spiel

Nachdem wir uns in unserem ersten Halbjahr gut in das Programm Star Logo TNG eingearbeitet hatten, entschlossen wir uns auch bei unserem  nächsten Projekt dieses Programm zu verwenden. 
Unser Ziel ist es ein Adventure Spiel mit verschiedenen Levels zu programmieren, in denen der Agent verschiedene Aufgaben, die mit der Höhe des Levels immer schwerer werden, bewältigen muss.

[Siebte Stunde](#sieben)

[Sechste Stunde](#sechs)

[Fünfte Stunde](#fünf)

[Vierte Stunde](#vier)

[Dritte Stunde](#drei)

[Zweite Stunde](#zwei)

[Erste Stunde](#eins)

## Siebte Stunde<a name="sieben"></a>

Leider konnten wir auf Grund von Stundenausfällen und Krankheitsfällen bei uns in den letzten Stunden nicht wirklich effektiv weiterarbeiten, sodass die Probleme (und Ziele...) der letzten Stunde bedauerlicherweise immer noch ausstehen. 
Allerdings haben wir es geschafft Mario durch einen speziellen Progammierblock ("wall ahead?"), den wir in StarLogoTNG gefunden haben, so programmieren, dass er nicht mehr durch die Wände des Labyrinths läuft. Nun muss sich der Spieler also den Weg durch das dritte Level suchen und finden. Dies wird aber leider durch die Farbe des Spacelandes stark eingeschränkt. Wir haben es nicht mehr geschafft den BOden vollständig einzufärben, weshalb es an einigen Stellen sehr schwer ist den Boden und die Mauern zu unterscheiden und man im warsten Sinne des Wortes in dem Irrgarten ohne jegliche Orientierung herum irrt.
Schafft es der Spieler dennoch aus dem Labyrinth springt er nicht in das von uns eigentlih angestrebte vierte Level, welches wir leider nicht mehr geschafft haben zu programmieren...
Auch die anderen aufgetretenen Konflikte konnten wir leider nicht mehr angehen und beheben.

Das alles hat uns gezeigt, dass manchmal Probleme, die noch so klein aussehen mögen, einen sehr lange in seinem Prozess aufhalten und einschränken können. Und obwohl wir trotz unserer vorher nicht vorhandenen Informatikkenntnisse bestimmt mehr hätten schaffen können, sind wir trotzdem einigermaßen zufrieden mit dem was wir in dem letzten Jahr gelernt und zu Stande gebracht haben.

## Sechste Stunde<a name="sechs"></a>

Heute haben wir das Labyrinth zu Ende gebaut und angefangen den Boden einzufärben. Da das alles sehr lange gedauert hat. Habe ich an unseren Stundenblogg weitergeschrieben, da wir hier noch einiges aufzuholen hatten.
Außerdem haben wir noch ein paar Probleme und Konflikte in unserer Programmierung offen, die wir demnächst angehen wollen. Zum Beispiel ist uns aufgefallen, dass wenn Mario in das erste Level zurück springt, weil er gestorben ist, und dann wieder in das zweite Level gespielt wird, alle Gegenstände, also die Mauer, die Fische und die Möhre, doppelt in dem Spaceland vorhanden sind. Desweiteren müssen wir Mario noch so programmieren, dass er nicht durch die Wände des Labyrinths lauen kann.

Auch haben wir schon einen Plan wie die nächsten Level aussehen sollen, aber ob wir das alles noch schaffen, was wir uns so vorstellen, bleibt abzuwarten.

## Fünfte Stunde<a name="fünf"></a>
 
In dieser Stunde haben wir die Grundsteine für das dritte Level gelegt. Damit Mario in das dritte Level gelangen kann, muss er allerdings die Mohrrübe aus dem zweiten Level einsammel. Nur wenn er sie besitzt kann er durch das Tor der Mauer in das dritte Level gelangen. Dafür haben wir nun wieder "Boolsche Variablen" benutzt. Diese nannten wir "Mario hat Wurzel" und setzten sie auf wahr.

![screenshot15](Bilder/screenshot15.png "15")

In dem "Forever"-Block mussten wir die Variable nun auf falsch setzen, denn die Möhre ist ja noch irgendwo in dem Spaceland und Mario muss sie erst einsammeln um sien besitzen zu können.

![screenshot16](Bilder/screenshot16.png "16")

Sobald jedoch Mario mit der Möhre kollidiert, besitzt er sie. Dafür setzten wir die Variable auf wahr und ließen die Möhre mit Hilfe eines "die"-Blockes verschwinden. Außerdem kann Mario nun in das dritte Level springen wenn er mit der Mauer kollidiert. Der "if"-Block stellt sicher, dass er allerdings nur das Level wechseln kann, wenn er die Möhre besitzt. Deshalb muss dafür die Boolsche Variable wahr sein.

![screenshot17](Bilder/screenshot17.png "17")

Schließlich haben wir heute noch angefangen das dritte Level zu bearbeiten. In diesem soll Mario durch ein Labyrinth gehen. Gelangt er auf die andere Seite kann er dort wieder etwas tun um darauf in das vierte Level zu gelangen. 

## Vierte Stunde<a name="vier"></a>

Heute haben wir uns damit beschäftigt unser "Canvas" zu sortieren. Einige Blöcke konnten wir entfernen, da wir sie gar nicht mehr benötigten. Außerdem konnten wir andere Blöcke einfacher programmieren und so unser "Canvas" übersichtlicher gestalten. Besonders unser großer "Kollisions"-Block von Mario und dem Auto ein Dorn im Auge. Vorher hatten wir, um zwei Fische in dem Spaceland zu erschaffen, zwei einzelnde "Hatch"-Blöcke programmiert, da die Fische unterschiedliche Positionen im Spaceland haben sollten. Herr Buhl hat uns darauf aufmerksam gemacht, dass es eine schönere Version gibt. Wir haben uns dafür entschieden die zwei "hatch"-Blöcke in einem "Procedure"-Block zusammen zu fassen, den wir "Hatchfisch" gennant haben. Um trotzdem noch für die beiden Fische unterschiedliche Koordinaten festlegen zu können, haben wir zunächst einmal Variablen für die x- und y-Achsen eingestzt. 

![screenshot13](Bilder/Screenshot13.png "13")

In den Kollisionsblock von Mario un dem Auto mussten wir nun nur noch zwei "Hatchfisch"-Blöcke einsetzen , in die wir dann nur noch unserer erwünschten Koordinaten für die Fische eingegeben haben. Dadurch wurde unser "Canvas" übersichtlicher. Das wird uns zu Gute kommen, wenn wir in den nächsten Stunden noch weitere Levels mit komplizierteren Abläufen programmieren werden.

![screenshot12](Bilder/Screenshot12.png "12")

Damit auch das zweite Level anspruchsvoll bleibt, muss Mario dieses Mal zwischen den ganzen Gräsern eine Mohrrübe finden. Allerdings ist die Mohrrübe nicht entstanden. Unser erster Verdacht war, dass sie zu klein war um in dem Spaceland gesehen zu werden. Aber als wir die Größe der Möhre vergrößert haben, konnten wir sie immer noch nicht finden. Deshalb kam uns die zündende Idee "Count"-Blöcke für alle Gegenstände in unserem Spaceland einzufügen. Jedoch zeigten uns die "count"-Blöcke, dass keine Möhre entstanden war. 

![screenshot14](Bilder/Screenshot14.png "14")  

Nachdem Herr Buhl uns bestätigt hatte, dass wir aber alles richtig programmiert hatten, änderten wir die Reihenfolge in dem Kollisionsblock und siehe da, die Möhrrübe war da.

![screenshot10](Bilder/Screenshot10.png "10")

Natürlich muss jetzt aber auch die Möglichkeit bestehen, dass Mario "stirbt" und in das vorherige Level zurückfällt. Das haben wir einfach wieder mit einem "Kollisions"-Block programmiert, in dem wir die "change-level"-Blöcke eingefügt haben.

![screenshot11](Bilder/Screenshot11.png "11")

Leider mussten wir heute auch feststellen, dass unser Programm sich öfters aufgehangen hat und wir es schließen mussten, sodass unsere programmierten Sachen verloren gegangen sind und wir die Sachen neu einfügen konnten. Deshalb haben wir uns vorgenommen ab sofort öfters unseren Programmierstand zu speichern.


## Dritte Stunde<a name="drei"></a>

Nachdem wir in der letzten Stunde festgestellt haben, dass unsere Programmierung nicht so funktioniert, wie wir uns das vorgestellte hatten, haben wir uns für diese Stunde vorgenommen, diesen Fehler zu beheben. Das Problem war, dass Mario zwar in das zweite Level springt, dieses aber nicht so erscheint, wie wir es vorher programmiert hatten. Denn wir hatten zuvor in einen zweiten "setup"-Block Agentenblöcke eingesetzt, um dann in dem zweiten Level weitere Gegenstände in dem Spaceland zu haben. Diese tauchten allerdings nicht auf wenn Mario in das zweite Level sprang, sondern sie entstanden erst dann wenn man den "setup"-Block für das zweite Level anklickte. Dann jedoch verschwand Mario. 
Nach etlichen gescheiterten Versuchen, wie man dies anders programmieren könnte, fragten wir schließlich Herrn Buhl um Hilfe. Da aber auch er sich bei der Programmierung von verschiedenen Leveln nicht ganz sicher war, mussten wir ein paar kleine Tricks anwenden. Herr Buhl erklärte uns zuerst, dass wenn man nicht weiß wie man etwas programmieren soll, dass man dann versuchen sollte das Programm auszutricksen, indem man sozusagen drumherum programmiert. Unsere Lösung das Programm zu umgehen war dann eine "hatch do"-Funktion zu verwenden. Den Block dafür setzten wir in den Kollisionsblock ein, in den wir  auch schon andere Bedingungen, wie die, dass Mario das Level bei der Kollison wechselt, eingefügt hatten. Somit legten wir also fest, dass wenn Mario mit dem Auto kollidiert, die Mauer und auch Gräser entstehen.

![screenshot4](Bilder/Screenshot04.png "4")

In die "hatch do"-Blöcke haben wir dann weitere Blöcke eingesetzt um die erwünschten Eigenschaften der neu entstehenden Objekte zu erschaffen. So sollte die Mauer an einer bestimmten Stelle stehen und die Gräser orange eingefärbt und zufällig im Raum verteilt sein.

Desweiteren hatten wir heute eine andere Idee, das zweite Level noch ein bisschen aufregender zu gestalten. In der in der letzten Stunde erschaffenden Schlucht soll jetzt Wasser mit Fischen sein. Falls Mario in diesen Graben fällt und möglicherweise mit einem Fisch kollidiert, soll er sozusagen "sterben" und in das erste Level zurückkehren.
Auch hier tauchten direkt von Anfang an Probleme auf. Erst einmal entstand kein Fische, obwohl wir diese Bedingung genau so programmiert hatten, wie auch zuvor bei der Mauer und den Gräsern. Wir hatten bereits die Idee, dass der Fisch, der entstanden ist, einfach zu klein war, um ihn erkennen zu können. Herr Buhl half uns schließlich, die Größe desFisches so zu verändern, sodass man ihn nun in dem Spaceland sehen kann. 

![screenshot5](Bilder/Screenshot05.png "5")  ![screenshot9](Bilder/Screenshot09.png "9")

Nun wollte wir ja aber auch, dass mehere Fische entstehen, die alle in dem Graben umher schwimmen. Uns war klar, dass wir dafür, zum einen eine willkürliche Bewegung der Fische festlegen müssen und zum anderen müssen wir diese Bewegung auf einen bestimmten Raum eingrenzen, da sie sich ja nicht aus dem Graben herausbewegen sollen. Da wir allerdings nicht wissen, wie man das genau programmieren kann, haben wir uns das als Ziel für die weiteren Stunden vorgenommen.

## Zweite Stunde<a name="zwei"></a>

Unser heutiger Plan war, das zweite Level zu bearbeiten. In diesem soll Mario nun einen, noch undefinierten, Gegenstand einsammeln und danach durch ein Tor in einer Mauer gehen um dann in das dritte Level zu gelangen.
Uns ist es wichtig, dass der Spieler mit jedem neuen Level eine neue Welt betritt. Deshalb haben wir begonnen das Terrain im zweiten Level zu verändern. Wir wollten das komplette Spaceland bräunlich einfärben, damit eine Art Savannen oder Wüsten Landschaft entsteht. Dazu haben wir mit HIlfe der Drawing-Funktion, welche in dem Spacelandfenster zu finden ist, unsere Wunschfarbe gemischt und damit den Boden des Spacelandes eingefärbt. 

![screenshot6](Bilder/Screenshot06.png "6")

Außerdem haben wir einen Teil des Spacelandes abgesenkt, sodass eine Art Schlucht entsteht.
Als nächstes haben wir eine Mauer mit einem "setup"-Block eingefügt. 

![screenshot7](Bilder/Screenshot07.png "7")

Allerdings wollten wir, dass die Mauer ganz am Rand des Spacelands, und nicht in der Mitte, steht. Da das Spaceland sich in einem Koordinatensystem befindet, welches nicht sichtbar ist, allerdings zur STandortfestlegung herangezogen werden kann, konnten wir dies durch spezielle Blöcke erreichen. In diesen setzten wir dann die erwünschten Standortkoordinaten der Mauer ein. So stand die Mauer am Ende genau da, wo sie sein sollte.

![screenshot8](Bilder/Screenshot08.png "8")

Unser Spaceland war allerdings noch ziemlich trist und langweilig, weshalb wir uns dazu entschlossen haben Gras einzufügen. Wie auch schon zuvor die Mauer, haben wir das Gras mit Hilfe des "setup"-Blocks kreiert und es durch einen "change colour"-Block orange eingefärbt. 
Am Ende dieser Stunde waen wir recht zufrieden mit der "Welt" des zweiten Levels, doch so einfach wie gedacht hatten funktionierte das Erstellen eines neuen Levels doch nicht, wie wir in der nächsten Stunde feststellen mussten...

## Erste Stunde<a name="eins"></a>

In der ersten Stunde haben wir die Basis für unser Spiel geschaffen, indem wir einen Agenten programmierten und das Terrain bearbeiteten. Wir erschufen Bäume und ein Auto, zu welchem der Agent gelangen muss um in das nächste Level (Level 2) aufzusteigen.  
Damit man die verschiedenen Gegenstände auf der Karte besser erkennen kann, haben wir die Bäume grün und das Auto blau eingefärbt. Allerdings verfärben sich nur die Punkte auf der Karte und nicht die Objekte selber, da sie eine "Haut" tragen. Als unseren Agenten wählten wir Mario, dessen Haut wir entfernten und ihn darauf rot einfärbten, um ihn in dem Spaceland besser erkennen zu können. Dies konnten wir mit Hilfe eines "model skin off"-Blockes verwirklichen.

![screenshot1](Bilder/Screenshot01.png "1")

Um unseren Arbeitsplatz bei Star Logo TNG übersichtlich und organisiert aufzubauen, programmierten wir die Steuerung von Mario in einem Block. Dazu verwendeten wir den "procedure"-Block und nannten ihn Bewegung. An diesen hängten wir mehrer "if"-Blöcke um die Bedingungen für die Steuerung festzulegen. Es muss also zum Beispiel die Pfeiltaste nach oben gedrückt werden, um Mario vorwärts laufen zu lassen. 

![screenshot3](Bilder/Screenshot03.png "3")
 
Das Ziel des ersten Levels ist es die "Tür" in das zweite Level zu finden. Die "Tür" ist in unserem Fall das Auto, wenn Mario mit diesem kollidiert, gelangt er automatisch in das zweite Level. Dafür benutzten wir "change level"- und "set level"-Blöcke. Der "change level"-Block sorgt dafür, dass der Spieler das zweite Level sieht, sich also das Terrain verändert, während der "set level"-Block sicherstellt, dass der Agent weiß, dass er sich in dem zweiten Level befindet.
 
![screenshot2](Bilder/Screenshot02.png "2")
