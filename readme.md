# Liftchecker
Prüft Aufzüge und Rolltreppen der MVG + DB auf Betriebsbereitschaft, damit Mobilitätseingeschränkte dadurch hoffentlich seltener vor defekten Liften stehen werden. 

Hol' Dir Liftchecker >>> <a href='https://github.com/snfiware/liftchecker-releases/releases/tag/v0.5.2'>v0.5.2</a> <<<
---

    Feststecken im Sperrengeschoss? Nie wieder!


# Screenshots
<div>
<image src="https://user-images.githubusercontent.com/63856302/225411538-ba473be5-f035-4067-9f87-e5792e709a87.png" width="200"/>
<image src="https://user-images.githubusercontent.com/63856302/225411543-829f8a9e-2a94-449e-8498-9d35f64bcbb2.png" width="200"/>
<image src="https://user-images.githubusercontent.com/63856302/225411548-0ba44651-9ab4-47ad-a5f7-2a9fffba2897.png" width="200"/>
<image src="https://user-images.githubusercontent.com/63856302/225411553-6538e5c0-d7a9-4254-883f-d2767240e430.png" width="200"/>
</div>

<!DOCTYPE HTML>
<html>
<head>
    <meta charset="utf-8" content="text/html"/>
    <!-- css filename is altered by the HelpActivity onCreate-->
    <link href="styles_main.css" rel="stylesheet">
</head>
<body>
<!--
<div style="text-align:right;padding-right:20px;"><a href="#hTopToc">back to top</a></div>
<li></li>
<li></li>
-->

<br id="hTopToc"/>
<h1>Inhaltsverzeichnis</h1>
<ol>
    <li class="toc"><a href="#hKeyFeatures">Kurzbeschreibung</a> </li>
    <li class="toc"><a href="#hSettings">Einstellungen</a> </li>
    <li class="toc"><a href="#hSearch">Suche</a> </li>
    <li class="toc"><a href="#hMaps">Pläne und Karten</a> </li>
    <li class="toc"><a href="#hPrivacy">Datenschutz</a> </li>
    <li class="toc"><a href="#hLicense">Rechtliches</a> </li>
    <li class="toc"><a href="#hBugsLog">Fehler melden</a> </li>
</ol>

<br id="hKeyFeatures"/>
<h1>Kurzbeschreibung</h1>
<p>Liftchecker</p>
<ol>
    <li>ist ein Qualitätsprodukt aus dem Hause <a href="https://github.com/snfiware">Snfiware</a>.</li>
    <li>prüft den Status von Aufzügen und Rolltreppen auf Knopfdruck oder auch automatisch im Hintergrund und benachrichtigt bei Betriebsstörungen.</li>
    <li>fragt dazu Online-Schnittstellen der MVG und der DB ab. Dadurch sind Statusinformationen von ca. 4.500 Liften im Großraum München und auch - über die DB - von ganz Deutschland verfügbar. Im Detail werden JSON-APIs diese Dienste genutzt:
        <ul style="word-wrap: break-word;">
            <li>MVG: https://www.mvg.de/dienste/zoom.html</li>
            <li>DB: https://developers.deutschebahn.com/db-api-marketplace/apis/product/fasta</li>
        </ul>
    </li>
</ol>

<br id="hSettings"/>
<h1>Features und Einstellungen</h1>
<p>Liftchecker</p>
<ol>
    <li>zeigt im Hauptbereich den Gesamtstatus an - somit ist man auf einen Blick über den Betriebszustand informiert. Ein Klick zeigt die Details.</li>
    <li>hat intuitive und flexible <a href="#hSearch">Suchmöglichkeiten</a> in der Liftliste und kann daraus Favoriten auswählen. Mittels dem Stern-Symbol kann eine Liftauswahl zusammengestellt werden. Die Liftliste kann mit dem Filtersymbol zwischen 'alle' und 'nur gewählte' umgeschaltet werden.</li>
    <li>alarmiert auf Wunsch via Benachrichtigung automatisch über Störungen der ausgewählten Lifte.</li>
    <li>kann Liftalarme eine konfigurierbare Zeitspanne zurückstellen. Dies ist direkt über die Benachrichtigung als auch in der App möglich.</li>
    <li>verfügt über Einstellmöglichkeiten zum Abfragen des Liftstatus nur zu bestimmten Wochentagen und Uhrzeiten. Es können bis zu sieben Zeitfenster festgelegt werden, die die automatische Hintergrundaktivität steuern.</li>
    <li>fragt via 'Liftstatus jetzt prüfen' oder im Hintergrund - um Datenvolumen zu sparen - immer nur die gewählten Favoriten ab. Da die APIs auf Ebene der Station arbeiten (und nicht mit Lift), werden alle Lifte der Station auch mit aktualisiert. Die gesamte Liftliste kann im Menü unter 'Lifte' aktualisiert werden.</li>
    <li>stellt in der Liftliste auf der linken Seite drei Icons dar, a) Aufzug oder Rolltreppe (wir nennen beides als Überbegriff 'Lift', intern 'device'), b) den Anbieter (Provider) und c) den Status des Lifts. Der Status kann sein: OK (in Betrieb), AUS (außer Betrieb), TMT (Timeout; wann die Information als veraltet gilt kann man einstellen) und ? (unbekannt). Jeder Eintrag besitzt ein kontextabhängiges Popup-Menü mit weiteren nützlichen Optionen.</li>
</ol>
<p>Optionen in der Liftliste:</p>
<ul>
    <li>Navigation zu <a href='#hMaps'>Stations- und Umgebungsplänen</a>.</li>
    <li>Anpassen der Lifttexte (da die Informationen der Anbieter teilweise auslegungsfähig sind).</li>
    <li>Zurückstellen von Alarmen: manuelles Setzen und Aufheben.</li>
    <li>Spezialisten-Suche: siehe <a href='#hSearch'>eigenes Kapitel</a>. </li>
    <li>Einsortieren von nachträglich ausgewählten Liften zu den namensgleichen Stationen: Verfügbar am Listenende (des dort obersten) zum 'Nach-oben-Verschieben'.</li>
    <li>Zusatz-Informationen sind in der Liftliste mit * gekennzeichnet. Hier kann man bei der MVG Planungsdaten für die prognostizierte Wiederverfügbarkeit betrachten - die DB-Einträge bieten hier Stations-Informationen.</li>
</ul>
<p>Android</p>
<ol>
    <li>hat für <b>Benachrichtigungen</b> insbesondere ab höheren APIs sehr flexible Settings. Wenn sie zu oft erscheinen und dadurch stören, lang auf sie klicken: es öffnet sich ein Menü, Verwalten. Alternativ Long-Press auf dem App-Icon, App-Einstellungen, Benachrichtigungen. Für jeden Kanal können eigene Vorgaben gemacht werden. Es wird empfohlen den Kanal 'Störungsmitteilungen' nicht vollständig auszuschalten. In der App besteht die Möglichkeit Alarme zurückzustellen, sodass eine erneute Benachrichtigung erst nach einer gewissen (konfigurierbaren) Zeit wieder erfolgt. </li>
    <li>bietet - je nach Version ein wenig unterschiedlich benannt - unter <i>Bedienungshilfe/Eingabehilfe > Interaktionssteuerung/Erweiterte Einstellungen > Zeit zum Reagieren/Zeit für eine Maßnahme</i> die Option an, die <b>Anzeigedauer von Ausgaben</b> zu verändern. Wem also manche Meldungen zu kurz angezeigt werden, kann dort eine <b>Verlängerung</b> festlegen. Wenn man das nicht verstellen will, weil es generell wirkt, ist es vielleicht eine Alternative einen Screenshot zu machen (Tasten Aus+Leiser gleichzeitig drücken).</li>
</ol>

<div style="text-align:right;padding-right:20px;"><a href="#hTopToc">back to top</a></div>
<br id="hSearch"/>
<h1>Suche</h1>
<p>Die Suche in den Liften soll sowohl einfach zugänglich sein, als auch Spezialistenbedürfnisse befriedigen. Generell gilt:</p>
<ul>
    <li>Ein Bahnhof ist in der Liste nur dann enthalten, wenn er über mindestens einen Aufzug oder eine Rolltreppe verfügt. Also nicht wundern, wenn manche fehlen.</li>
    <li>Groß-/Kleinschreibung ist egal.</li>
    <li>Leerzeichen trennen die Eingabe in Such-Token. Jeder Token wird einzeln gesucht.</li>
    <li>Worin und wie wird gesucht? Im sog. Such-String mit einem simplen "ist enthalten" - es wurde auf Wildcards (*,?) verzichtet.</li>
    <li>Wenn man einfach lostippt führt man eine Freitext-Suche - eine sog. "simple query" - im gesamten Such-String jedes einzelnen Liftes - aus.</li>
</ul>
<p>Man kann aber auch nur bestimmte Anteile des Such-Strings (und nicht alles) abfragen:</p>
<ul>
    <li>Der Such-String kann via Popup-Menü eines Listeneintrags angezeigt werden. Er besteht grundsätzlich aus allen verfügbaren Textanteilen, die die App vom Anbieter aus der Online-Schnittstelle, aber auch von statisch eingebunden Listen bekommt. </li>
    <li>Die verfügbaren Such-Token sind im Such-String gelistet, beginnen mit einem zweistelligen Bezeichner, gefolgt von # und enden mit dem eigentlichen Inhalt.</li>
    <li>Falls z.B. nur Aufzüge von Interesse sind - der Such-Bezeichner 'device type' leistet das: <i>dt#aufzug</i>. Tipp: Man muss Aufzug nicht ausschreiben, <i>dt#a</i> genügt.</li>
    <li>Mittels Such-Token kann logisches OR (mehrere gleiche Token angeben) und NOT (! einem Such-Token voranstellen) genutzt werden.</li>
</ul>
<p>Jede Suche besteht intern aus mehreren Schritten:</p>
    <ol>
        <li>Freitext-Suche ("simple query") ausführen</li>
        <li>Verbundene Stationen expandieren</li>
        <li>Restliche Such-Token abfragen (alle Bezeichner# der eingegebenen Suche)</li>
    </ol>
<p>Damit kann so etwas formuliert werden:<br><i style='padding-left:10px'>   hbf nch !si#4162 !si#4231 dd#1</i></p>
<p>Erklärung:</p>
<ul>
    <li>Mü<b>nch</b>en <b>Hbf</b> der DB wird durch die Freitext-Suche gefunden</li>
    <li>Diese Station ist (mittels interner Konfiguration) mit MVG Hauptbahnhof korreliert, deswegen werden alle Lifte dieser Station <i>zusätzlich</i> mit angezeigt. </li>
    <li>Freitext 'nch' findet auch Mönchengladbach. Diese Stations-ID wird mit '!si#' komplett ausgeschlossen. Ebenso (Beispiel für logisches OR) eine zweite Station:</li>
    <li>Freitext 'hbf' findet auch einen Lift an der Donnersbergerbrücke, da in der Liftbeschreibung 'Ri Hbf' steht. Tipp: Der Ausschluss würde alternativ auch mit der 'device id' <i>di#</i> oder auch anderen Bezeichnern möglich sein.</li>
    <li>dd#1 sucht in der Liftbeschreibung ('device description') nach der Ziffer 1. Damit verbleiben Einträge mit U1 (MVG) und mit 'zum Gleis 1' (DB). Hinweis: 'dd#1' im Vergleich zu einfach '1' macht im Ergebnis einen ziemlich großen Unterschied!</li>
</ul>


<div style="text-align:right;padding-right:20px;"><a href="#hTopToc">back to top</a></div>
<br id="hMaps"/>
<h1>Bahnhofspläne und Umgebungskarten</h1>
<p>Da die von den Anbietern gewählten Bezeichnungen der Aufzüge und Rolltreppen oftmals alleine nicht ausreichen, um die Zeile in der App einem Lift in der Realität zuzuordnen, wurde die Möglichkeit geschaffen, kontextbezogene Stations-Infos im Browser anzuzeigen. Folgendes wird über das Popup-Menü in der Liftauswahl angeboten. </p>
<ul>
    <li>Für alle MVG-Stationen ist die interaktive Zoom-Liftkarte und ein MVV-Bahnhofsplan aufrufbar.</li>
    <li>Bei der DB haben wir leider keine universelle Lösung gefunden, deswegen gibt es dort Möglichkeiten, die zumindest alle MVV-, bayerischen und großen Bahnhöfe abdecken sollte.</li>
    <li>Für die MVV-Pläne setzen wir die Klartextbezeichnungen der Stationen um und rufen deren zentrale PDF-Sammlung auf. Dies funktioniert für alle Stationen im Großraum München.</li>
    <li>Für die DB benutzen wir die Station-ID (im Such-String SI#) und lösen diese über Listen zur sog. DS100 und zur Eva-Nr auf (im Such-String unter AI# ersichtlich) und rufen damit eine URL des jeweiligen Anbieters auf. In Teilen wäre auch noch die IFOPT verfügbar - bislang wird sie aber nicht genutzt. Sollten hier Web-Ressourcen bekannt sein, die mit diesen IDs aufrufbar sind: bitte mitteilen - wir würden hier gerne weitere Möglichkeiten einbinden. </li>
    <li>Bei der DB konnten wir die bekannte blaue Bahnhofstafel (Ankunft- und Abfahrtszeiten der Züge) einbinden. Ähnliches würden wir gerne für die MVG tun - Erkenntnisse bitte mitteilen.</li>
</ul>

<div style="text-align:right;padding-right:20px;"><a href="#hTopToc">back to top</a></div>
<br id="hPrivacy"/>
<h1>Datenschutz</h1>
<p>Liftchecker</p>
<ol>
    <li>fragt die in der <a href="#hKeyFeatures">Einleitung</a> genannten Datenquellen im Internet ab. Die Datenverwendung der jeweiligen Anbieter haben wir nicht unter Kontrolle - diese Schnittstellen sind aber offiziell - auch für die hier vorliegende Form der Nutzung - freigegeben. </li>
    <li>selbst speichert und verwendet die Benutzereingaben, damit es seinen offensichtlichen Zweck - Liftstatus abfragen - erfüllen kann und in keinem Maße über die hier genannten Punkte hinaus. Die Auswahl der Lifte stellen keine personenbezogenen Daten im engeren Sinne dar und sind damit datenschutzrechtlich grundsätzlich als unbedenklich einzustufen. Die App fragt die Daten ab, so und wie sie eingestellt wurden. Es werden durch Liftchecker <i>keine anderen</i> Übertragungen oder Verarbeitungen durchgeführt. Snfiware ist Datenschutz und Privatsphäre sehr wichtig. Tatsächlich könnte natürlich beim jeweiligen Dienst durch die Abfrage und die dadurch übermittelte Liftauswahl in Verbindung mit Zeit und verwendetem Endgerät ein Rückschluss auf personenbezogene Informationen möglich sein. </li>
    <li>schreibt Protokolleinträge in den geräteinternen LogCat-Ringpuffer (dies ist ein Bereich fester Größe, der ständig im Hintergrund durch Android und die Apps geschrieben und regelmäßig wieder überschrieben wird). Durch Liftchecker werden nur in die App eingegebene Daten, App-interne Verlaufsinformationen und Informationen zum Zwecke der Fehleranalyse geschrieben. Wir bieten eine integrierte <a href="#hBugsLog">Funktion zur Fehlermeldung</a> an, welche daraus eine Logdatei erstellen und bereitstellen kann. Solange sie diese Funktion nicht nutzen, bleiben Log-Informationen vollständig lokal und werden regelmäßig überschrieben. Die aus dem LogCat erstellte Log-Datei <i>könnte tatsächlich</i> datenschutzrechtlich relevante Informationen enthalten, da es mittels APIs des Betriebssystems zusammengestellt wird - diese Interna haben wir nicht unter Kontrolle. Die Logdatei kann aber vor einer Übermittlung an uns überprüft werden. Das Verhalten der Protokollierung kann in der App grundsätzlich eingestellt werden. Falls generellere Vorgaben gewünscht werden, empfehlen wir, sich mit 'Android ADB LogCat' zu beschäftigen (googlen).</li>
</ol>
<div style="text-align:right;padding-right:20px;"><a href="#hTopToc">back to top</a></div>

<br id="hLicense"/>
<h1>Lizenz und Haftungsausschluss</h1>
<p>Copyright 2023 Snfiware</p>
<p>Licensed under the Apache License, Version 2.0 (the "License"); you may not use this software except in compliance with the License. You may obtain a copy of the License at: http://www.apache.org/licenses/LICENSE-2.0</p>
<p>Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.</p>
<p>Kurz zusammengefasst und in Deutsch:</p>
<ul>
    <li>Wir haben diese Software für eigene Zwecke erstellt und benutzen sie auch weiterhin selbst. Da wir der Meinung sind, dass sie evtl. auch für andere von Nutzen sein könnte, haben wir entschieden sie zu veröffentlichen.</li>
    <li>Die Nutzung erfolgt auf eigene Gefahr.</li>
    <li>Der Sourcecode ist unser Eigentum. Eine Verwendung durch Dritte ist nicht erwünscht.</li>
    <li>Die App stellen wir kostenfrei, ohne Werbung und ohne andere Interessen zur <i>freien</i> Nutzung zur Verfügung, damit Mobilitätseingeschränkte hoffentlich durch sie seltener vor defekten Liften stehen werden. Jede kommerzielle Nutzung ist untersagt.</li>
    <li>Trotz umfangreichen Tests und Umsicht kann Fehlverhalten nicht gänzlich ausgeschlossen werden. Wir übernehmen keine Haftung für jedwede entstandene Schäden.
    </li>
</ul>
<div style="text-align:right;padding-right:20px;"><a href="#hTopToc">back to top</a></div>

<br id="hBugsLog"/>
<h1>Fehler melden / <br/>Log erzeugen</h1>
<p>Fehler bitte melden, damit wir eine Chance haben sie abzustellen.</p>
<p>Die App besitzt eingebaute Funktionen, um aus dem LogCat-Ringpuffer (siehe auch <a href="#hPrivacy">Datenschutz</a>) ein Logfile zu erzeugen, ohne das schwerlich eine sinnvolle Fehleranalyse erfolgen kann:</p><p>Bitte lang auf den Zurück-Knopf drücken - ein Menü erscheint, Log anzeigen, bitte mit snuffo@freenet.de teilen. Wenn der Fehler reproduzierbar ist, würden wir uns freuen, wenn es mit einer frisch gestarteten App mit Loglevel-Einstellungen DEBUG erstellt wurde - dies erzeugt gegenüber der Standardeinstellungen erweiterte Auskünfte und hilft uns bei der Analyse.</p>
<p>So erzeugte Logfiles werden hier zwischengespeichert und werden nicht automatisch gelöscht:</p>
<pre>/storage/emulated/0/<b>Android/data/<br/>de.snfiware.liftchecker/cache/logs/</b></pre>
<p>Seit Android 11 ("scoped storage") können nicht mehr viele Dateimanager Apps direkt auf diesen Ablageort zugreifen. Um das Logfile näher zu betrachten kann man aber weiterhin der Download-Benachrichtigung folgen - Liftchecker hat den Pfad freigegeben.<br/>Falls man die Datei nur wieder löschen will, kann man in den Android-Einstellungen / Apps / Liftchecker / Speicher auch einfach nur den Cache der App leeren.</p>
<div style="text-align:right;padding-right:20px;"><a href="#hTopToc">back to top</a></div>
<br/>
<br/>
</body>
</html>
