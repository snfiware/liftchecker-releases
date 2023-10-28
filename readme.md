# Liftchecker
Prüft Aufzüge und Rolltreppen der MVG + DB, benachrichtigt bei Störungen und bietet viele nützliche Barrierefrei-Infos. Diese können durch die integrierte Suche analysiert und mittels OrganicMaps visualisiert werden.

# Download und Installation

[![](https://github.com/snfiware/liftchecker-releases/blob/main/main/ic_launcher.png)](https://github.com/snfiware/liftchecker-releases/releases/download/v1.0.3/snflc-v1.0.3-Public-release.apk)
*    [Download APK](https://github.com/snfiware/liftchecker-releases/releases/download/v1.0.3/snflc-v1.0.3-Public-release.apk)
*    [Installationshinweise](https://github.com/snfiware/liftchecker-releases/blob/main/main/install.md)


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
    <!-- css filename is altered by the HelpActivity::onCreate-->
    <link href="styles_main.css" rel="stylesheet">
</head>
<body>

<br id="inhaltsverzeichnis"/>
<h1>Inhaltsverzeichnis</h1>
<ol>
    <li class="toc"><a href="#kurzbeschreibung">Kurzbeschreibung</a> </li>
    <li class="toc"><a href="#prüflabel">Prüflabel</a> </li>
    <li class="toc"><a href="#features">Features</a> </li>
    <li class="toc"><a href="#benachrichtigungen">Benachrichtigungen</a> </li>
    <li class="toc"><a href="#suche">Suche</a> </li>
    <li class="toc"><a href="#pläne-und-karten">Pläne und Karten</a> </li>
    <li class="toc"><a href="#geodaten">Geodaten</a> </li>
    <li class="toc"><a href="#datenschutz">Datenschutz</a> </li>
    <li class="toc"><a href="#rechtliches">Rechtliches</a> </li>
    <li class="toc"><a href="#hinweise">Hinweise</a> </li>
</ol>
<br/>
<p>Stand: Oktober 2023</p>
<br id="kurzbeschreibung"/>
<h1>Kurzbeschreibung</h1>
<p>Barrierefrei unterwegs mit den Öffis - dafür haben wir Liftchecker erstellt! Wir bieten eine hochgradig integrierte App, um möglichst ohne Probleme durch den ÖPNV zu kommen und alle Informationen "auf einen Klick" zur Hand zu haben, die wichtig sind, wenn man trotz Mobilitätseinschränkung aktiv sein will.</p><p>Diese App ist für <b>Rollstuhlfahrer in und um München optimiert</b> und stellt die <a href="#prüflabel">selbst erstellten Inhalte</a> grundsätzlich aus dieser Perspektive dar.</p>
<p>Liftchecker</p>
<ol>
    <li><p>prüft den Status von Aufzügen und Rolltreppen auf Knopfdruck oder auch automatisch im Hintergrund und benachrichtigt bei Betriebsstörungen.</p></li>
    <li>nutzt dazu Online-Schnittstellen der MVG und der DB. Dadurch sind Liftstatus von ca. 4.500 Liften im Großraum München und auch - über die DB - von ganz Deutschland in Echtzeit verfügbar. Im Detail werden dafür JSON-APIs diese Dienste genutzt:
        <ul style="word-wrap: break-word;">
            <li>MVG: https://www.mvg.de/dienste/zoom.html </li>
            <li>DB: https://developers.deutschebahn.com/db-api-marketplace/apis/product/fasta </li>
        </ul><p>Unabhängig von den technischen Anlagen - "Lift" über die Online-APIs - werden Informationen zu Stationen direkt oder via Web-Navigation bereitgestellt. Damit sind insgesamt z.Zt. über 9.700 Einträge verfügbar.</p>
    </li>
    <li><p>ist kosten- und werbefrei, sowie auf minimalen Akku- und Bandbreitenverbrauch bei maximaler Offline-Funktionsfähigkeit ausgerichtet. Wir haben diese Software für eigene Zwecke erstellt und benutzen sie auch weiterhin selbst. Maximaler <a href="#datenschutz">Datenschutz und Privatsphäre</a> sind für uns selbstverständlich. Informationen zur Kompatibilität <a href="#kompatibilität">hier</a>.</p></li>
    <li><p>bietet neben den Online-Schnittstellen eine ausgeklügelte <a href="#suche">Suche</a> über die Offline-fähigen Informationen und besitzt kontextspezifische Navigationsmöglichkeiten zu Stations-/Lage-, Abfahrts-/Ankunftsplänen, Barrierefrei- und Bahnsteighöhe-Informationen, sowie selbst erhobene Informationen.</p></li>
</ol>

<div style="text-align:right;padding-right:20px;"><a href="#inhaltsverzeichnis">back to top</a></div>
<br id="prüflabel"/>
<h1>Prüflabel</h1>
<p>Damit's problemlos funktioniert, muss die Station entweder ohne Lifte stufenlos sein, oder es müssen alle benötigten Lifte funktionieren. Liftchecker ist ein Qualitätsprodukt aus dem Hause <a href="https://github.com/snfiware">Snfiware</a> und vergibt das Prüflabel SnfiCertified, um die Stationen unabhängig von der Lift-Online-Abfrage zu bewerten:</p>
<ul>
    <li>SC05: <i>alle</i> Bahnsteige des Bahnhofs sind <i>vollständig</i> stufenlos auch <i>ohne</i> technische Anlagen erreichbar</li>
    <li>SC04: wenn die technischen Anlagen OK sind, dann barrierefrei</li>
    <li>SC03: die Station ist nur teilweise oder eingeschränkt barrierefrei</li>
    <li>SC02: <i>kein einziger</i> Bahnsteig ist als barrierefrei eingestuft</li>
    <li>SC01: noch nicht geprüft</li>
</ul><p>Das Label stellt ab auf die Stufenlosigkeit von außen bis zum Bahnsteig, respektive den Bahnsteigen. Falls mehr als eine Einstufung möglich ist - da die Bahnsteige unterschiedlich sind - wird folgendermaßen bewertet: ein Bahnsteig SC05, einer SC04, Ergebnis SC04. Einer SC05/SC04, einer SC02, Ergebnis SC03. Die Bahnsteighöhe, aus der sich zusammen mit der eingesetzten Bahn die tatsächliche Einstiegsschwelle ergibt, bleibt hierbei für das Prüflabel zunächst unbeachtet. Es wird <i>angenommen</i>, dass alle baulichen Rampen, insbes. bzgl. ihrer Steilheit, tauglich für Handrollis sind. Umwege (relevant für Menschen mit Einschränkungen bzgl. Überwindung von Distanz) werden im Label nicht berücksichtigt, ggf. aber kommentiert.</p>
<p>Die Kommentare des Prüflabels beschreiben Details ("SnfiComment"). Damit verfügt man nun oft direkt (ohne eigene Prüfung der <a href="#pläne-und-karten">Pläne</a>) über die Information wo sich Rampen und Lifte befinden und kann gleich an der richtigen Stelle einsteigen.</p>
<p>Bahnsteighöhen aller MVV-S-Bahnhöfe wurden anhand der Bayern-Takt-Pläne erhoben und bereitgestellt. Für die MVG-U-Bahn-Stationen konnten diese Details bislang nicht erhoben werden, alle SC05-MVG-Bahnhöfe wurden aber kommentiert. Es empfiehlt sich bei der MVG generell ganz vorne einzusteigen, da sich dort inzw. an einigen Bahnsteigen, die noch zu niedrig sind, i.d.R. 5-10cm hohe, stationäre gelbe Mini-Rampen / Schwellen befinden, die ein "stufenloseres" Einsteigen bieten, und die neueren Fahrzeuge auch mehr Platz.</p>
<p>Weitere generelle Aussagen zu der konkreten Stufenlosigkeit für das Ein-/Aussteigen sind stark abhängig von der eingesetzten Bahn, der "Kippfähigkeit des Rollstuhls", der verfügbaren Hilfe durch Begleitperson oder auch Passanten, sowie der Nutzbarkeit von mobilen Rampen oder auch des Mobility-Service. Deswegen haben wir uns auf die Bereitstellung von "hard facts" beschränkt und hoffen auf die Nützlichkeit dieser für eine eigene Einschätzung im Alltag. Verbesserungsvorschläge bzgl. des SnfiComments oder der Bahnsteighöhen gerne an die <a href="#fehler-melden">Support-Mailadresse</a>. Wir werden diese Meldungen für Folgeversionen prüfen.
</p>

<div style="text-align:right;padding-right:20px;"><a href="#inhaltsverzeichnis">back to top</a></div>
<br id="features"/>
<h1>Features</h1>
<p>Liftchecker</p>
<ol>
    <li>hat intuitive und flexible <a href="#suche">Suchmöglichkeiten</a> in der Liftliste. Mittels des Sternsymbols kann eine Liftauswahl - die Favoriten - zusammengestellt werden. Die Liftliste kann mit dem Filtersymbol zwischen "alle" und "nur gewählte" umgeschaltet werden. Ferner ist es möglich Suchabfragen zu speichern und sie wieder aufzurufen. </li>
    <li>zeigt im Hauptbereich und via <a href="#benachrichtigungen">Benachrichtigungen</a> auch auf dem Sperrbildschirm den Gesamtstatus der Favoriten an - somit ist man auf einen Blick über den Betriebszustand informiert. Ein Klick zeigt die Details.</li>
    <li>alarmiert auf Wunsch via Benachrichtigung automatisch über Störungen der ausgewählten Lifte.</li>
    <li>verfügt über Einstellmöglichkeiten zum Abfragen des Liftstatus nur zu bestimmten Wochentagen und Uhrzeiten. Es können bis zu sieben Zeitfenster festgelegt werden, die die automatische Hintergrundaktivität steuern.</li>
    <li>kann Liftalarme eine konfigurierbare Zeitspanne zurückstellen. Dies ist direkt über die Benachrichtigung als auch in der App möglich.</li>
    <li>fragt via "Liftstatus jetzt prüfen" oder im Hintergrund immer nur - um Datenvolumen zu sparen - die gewählten Favoriten ab. Da die APIs auf Ebene der Station arbeiten (und nicht mit Lift), werden alle Lifte der Station mit aktualisiert. Die übrige Gesamtliste veraltet, kann aber im Menü der Liftliste jederzeit aktualisiert werden.</li>
</ol>
<br id="symbol"/>
<p>In der Liftliste werden alle Lifte und Stationen dargestellt, auf der linken Seite eines Eintrags drei <b>Icons</b>. Diese entsprechen bestimmten <a href="#such-token">Such-Token</a></p>
<ul>
    <li>DeviceType: "Aufzug", "Rolltreppe" (wir nennen beides als Überbegriff Lift), "<a href="#spezialfälle">Bahnhof ohne Lift</a>", oder "?" (Unbekannt). Letzteres dient als Failover, falls der Anbieter etwas an der Online-Schnittstelle ändern sollte - eine aktuelle Version von Liftchecker sollte diesen Status nicht aufweisen. </li>
    <li>Provider: z.Zt. nur "MVG" und "DB". Hinweis: Dieser Such-Token wird für ein <a href="#stationsliste">Spezialfeature</a> genutzt.</li>
    <li>DeviceStatus: "OK" (passierbar/in Betrieb), "NBP" (Nicht barrierefrei passierbar/außer Betrieb), "TMT" (Timeout; wann die Information als veraltet gilt, kann man in den Einstellungen anpassen) und "?" (Unbekannt). Unbekannt kann tatsächlich vom Anbieter kommen, bei <a href="#spezialfälle">virtuellen</a> Einträgen aber auch für fehlende/unzureichende Daten stehen. Jeder Eintrag besitzt ein kontextabhängiges Popup-Menü mit weiteren nützlichen Optionen.</li>
</ul>
<p>Optionen in der Liftliste (Long-Klick):</p>
<ul>
    <li>Navigation zu <a href="#pläne-und-karten">Pläne und Karten</a>.</li>
    <li>Zurückstellen von Alarmen: manuelles Setzen und Aufheben.</li>
    <li>Such-String: siehe <a href="#suche">eigenes Kapitel</a>. </li>
    <li>Favoriten verwalten: Massenfunktionen und Einsortieren von nachträglich ausgewählten Liften zu den namensgleichen Stationen: Verfügbar am Listenende (des dort obersten) zum "Nach-oben-Verschieben" (Moni-Feature:)).</li>
    <li>Lift umbenennen (da die Informationen der Anbieter teilweise auslegungsfähig sind).</li>
    <li><a href="#geodaten">Geodaten nutzen</a></li>
    <li>Zusatz-Informationen sind in der Liftliste mit * gekennzeichnet. Hier kann man bei der MVG <a href="#vordefinierte-suchen">Planungsdaten</a> für die prognostizierte Wiederverfügbarkeit betrachten - die DB-Einträge bieten hier Stations-Informationen. Wenn dort entsprechende Textpassagen ausgewählt werden, bieten die meisten Mobiltelefone kontextspezifische Optionen wie: Karte öffnen, anrufen, ... </li>
</ul>

<div style="text-align:right;padding-right:20px;"><a href="#inhaltsverzeichnis">back to top</a></div>
<br id="benachrichtigungen"/>
<h1>Benachrichtigungen</h1>
<p>Liftchecker</p>
<ul>
    <li>sendet häufig Benachrichtigungen, damit der Liftstatus direkt und ohne das Handy zu entsperren bereits im Sperrbildschirm sichtbar ist.</li>
    <li>verfügt über folgende Kanäle, die unabhängig voneinander ein- und ausgeschaltet werden können:
        <ol>
            <li>Standard</li>
            <li>Störungsmitteilungen</li>
            <li>Spezialbericht über den Status "unbekannt"</li>
        </ol>
        <p>Standard und Störungen teilen sich eine Benachrichtigungs-ID - man sieht nie mehr als eine Benachrichtigung gleichzeitig. Spezialberichte werden parallel dazu angezeigt.</p>
    </li>
    <li>aktualisiert grundsätzlich <i>jedes Mal</i> die Benachrichtigungen, wenn der Liftstatus aktualisiert wird. Wenn das stört, bitte den Kanal Standard und die Spezialberichte ausschalten. Störungsmitteilungen sollte <i>nicht</i> ausgeschaltet werden, da sonst Alarme nicht mehr zugestellt werden können, selbst dann nicht, wenn man den Hintergrund-Job nachträglich einschaltet.</li>
    <li>kann die <b>Favoriten</b> vor versehentlichem Verändern <b>schützen</b>. Wenn die Option angeschaltet ist, wird beim Abwählen eine Bestätigung eingefordert und jede Änderung aktualisiert die Benachrichtigung(en). Das wurde als extra Option im Liftemenü implementiert, da nicht jeder Klick bei der initialen Zusammenstellung ständig Benachrichtigungen senden soll.</li>
    <li>bietet die Möglichkeit Störungsmitteilungen / die <b>Alarme zurückzustellen</b>. Erst nachdem die (in den Einstellungen konfigurierbaren) Zeit abgelaufen ist, werden für diesen Lift erneut Benachrichtigungen an den <i>Störungskanal</i> geschickt. Die Benachrichtigungen auf den anderen Kanälen sind unabhängig davon - ein Zurückstellen wirkt also z.B. <u>nicht</u> auf die Standardmitteilungen.</li>
</ul>
<p>Android</p>
<ol>
    <li>hat für Benachrichtigungen insbesondere ab höheren APIs sehr flexible Settings. Wenn sie <b>zu oft</b> erscheinen und dadurch stören, lang auf sie klicken: es öffnet sich ein Menü, Verwalten. Alternativ Long-Press auf dem App-Icon, App-Einstellungen, Benachrichtigungen. Für jeden Kanal können eigene Vorgaben gemacht werden. Es wird empfohlen den Kanal "Störungsmitteilungen" nicht vollständig auszuschalten.</li>
    <li>bietet - je nach Version ein wenig unterschiedlich benannt - unter <i>Bedienungshilfe/Eingabehilfe > Interaktionssteuerung/Erweiterte Einstellungen > Zeit zum Reagieren/Zeit für eine Maßnahme</i> die Option an, die <b>Anzeigedauer von Ausgaben</b> zu verändern. Wem also manche Meldungen zu kurz angezeigt werden, kann dort eine <b>Verlängerung</b> festlegen. Wenn man das nicht verstellen will, weil es generell wirkt, ist es vielleicht eine Alternative einen Screenshot zu machen (Tasten Aus+Leiser gleichzeitig drücken).</li>
</ol>

<div style="text-align:right;padding-right:20px;"><a href="#inhaltsverzeichnis">back to top</a></div>
<br id="suche"/>
<h1>Suche</h1>
<p>Die Suche in den Liften soll sowohl einfach zugänglich sein, als auch Spezialbedürfnisse befriedigen. Generell gilt:</p>
<ul>
    <li>Groß-/Kleinschreibung ist egal.</li>
    <li>Leerzeichen trennen die Eingabe in Such-Token. Jeder Token wird einzeln gesucht.</li>
    <li>Ein Bahnhof ist in der Liste nur dann als <b>Lift</b> enthalten, wenn die Online-API ihn mit mindestens einem Aufzug oder einer Rolltreppe zurückmeldet. Der Bahnhof wird anderenfalls "virtuell" aus den statisch eingebunden Stationsinformationen generiert (erkennbar am <a href="#symbol">Symbol</a> "Bahnhof ohne Lift")</li>
    <li>Worin und wie wird gesucht? Im sog. Such-String mit einem simplen "ist enthalten" - es wurde auf Wildcards (*,?) verzichtet.</li>
    <li>Wenn man einfach lostippt führt man eine Freitext-Suche - eine sog. "simple query" - aus. Ob damit im gesamten Such-String jedes einzelnen Liftes, oder nur gezielt nach Stationen gesucht wird, ist abhängig von der Einstellung "Einfache Stationssuche".</li>
</ul>
<br id="vordefinierte-suchen"/>
<p>Vordefinierte Suchen</p>
<ul>
    <li>Es sind einige, von uns als praktisch eingestufte Suchen vordefiniert. Man kann sie in der Liftliste bei geöffnetem Suchschlitz (Lupe-Symbol) über das entsprechende Menü auswählen.</li>
    <li>Vordefinierte Suchen haben das experimentelle Feature "Query Rewrite" implementiert. Es versucht möglichst viel der bestehenden Abfrage zu <i>erhalten</i> und Suchanteile intelligent umzuschreiben ("merge"), sodass der bestehende Abfragetext nur in den durch die Abfrage ergänzten Anteilen verändert und sie eben nicht einfach nur vollständig ersetzt wird. <a href="#fehler-melden">Feedback</a> erwünscht. </li>
</ul>
<p>Man kann gezielt bestimmte Anteile des Such-Strings (und nicht alles) abfragen:</p>
<ul>
    <li>Der Such-String kann via Popup-Menü eines Listeneintrags angezeigt werden. Er besteht grundsätzlich aus allen verfügbaren Textanteilen, die die App vom Anbieter aus der Online-Schnittstelle, aber auch von statisch eingebunden Listen bekommt. </li>
    <li>Die verfügbaren <a href="#such-token">Such-Token</a> sind im Such-String gelistet, beginnen mit einem zweistelligen Bezeichner, gefolgt von # und enden mit dem eigentlichen Inhalt.</li>
    <li>Falls z.B. nur Aufzüge von Interesse sind - der Such-Bezeichner "device type" leistet das: <i>dt#aufzug</i>. Tipp: Man muss Aufzug nicht ausschreiben, <i>dt#a</i> genügt.</li>
    <li>Mittels Such-Token kann logisches OR (mehrere gleiche Token angeben) und NOT (! einem Such-Token voranstellen) genutzt werden.</li>
</ul>
<p>Jede Suche besteht intern aus mehreren Schritten:</p>
    <ol>
        <li>Freitext-Suche ("simple query") ausführen</li>
        <li>Verbundene Stationen expandieren (je nach Einstellung "Einfache Stationssuche")</li>
        <li>Restliche Such-Token abfragen (alle XX# der eingegebenen Suche)</li>
    </ol>
<p>Damit kann so etwas formuliert werden:<br><i style="padding-left:10px">   hbf nch !si#4162 !si#4231 dd#1</i></p>
<p>Erklärung:</p>
<ul>
    <li>Mü<b>nch</b>en <b>Hbf</b> der DB wird durch die Freitext-Suche gefunden</li>
    <li>Diese Station ist (mittels interner Konfiguration) mit MVG Hauptbahnhof korreliert, deswegen werden alle Lifte dieser Station <i>zusätzlich</i> mit angezeigt. </li>
    <li>Freitext "nch" findet auch Mönchengladbach. Diese Stations-ID wird mit "!si#" komplett ausgeschlossen. Ebenso (Beispiel für logisches Verknüpfen) eine zweite Station:</li>
    <li>Freitext "hbf" findet (mit Einstellung: "Einfache Stationssuche"=aus) auch einen Lift an der Donnersbergerbrücke, da in der Liftbeschreibung "Ri Hbf" steht. Tipp: Der Ausschluss würde alternativ auch mit der "device id" <i>di#</i> oder auch anderen Bezeichnern möglich sein.</li>
    <li>dd#1 sucht in der Liftbeschreibung ("device description") nach der Ziffer 1. Damit verbleiben Einträge mit U1 (MVG) und mit "zum Gleis 1" (DB). Hinweis: "dd#1" im Vergleich zu einfach "1" macht im Ergebnis einen ziemlich großen Unterschied!</li>
</ul>
<h2>Suchen merken und verwalten</h2>
<ul>
    <li>Gespeicherte Suchen sind bei <i>geöffnetem</i> Suchschlitz über das Lupesymbol verfügbar. Bei einem Klick darauf wird ein Popupmenü angezeigt - Optionen:</li>
    <li>Der aktuell im Suchschlitz eingegebene Suchtext kann direkt gespeichert oder auch zusätzlich mit einem Namen versehen werden. Der Suchtext wird dadurch zur gespeicherten Suche (GS) und kann damit wiederhergestellt werden. Damit hat man z.B. die Möglichkeit - über die Favoriten hinaus - weitere Listen zu verwalten.</li>
    <li>GS können einfach als Suche wieder aufgerufen werden. Wenn man z.B. die aktuelle Liftauswahl (beim Herumspielen) nicht verlieren möchte (Gesamt-Backup-Feature gäbe es im Startfenster auch), kann man die Menüoption "Liste als Suchtext verwenden" wählen und sie als GS sichern. Dies ist nicht perfekt, da die "device identifiers" verwendet werden, diese aber von den Anbietern teilweise so gestaltet wurden, sodass sie tatsächlich alleine leider nicht eindeutig sind. Außerdem gibt es auch wenige Überdeckungen der IDs zw. den Anbietern. Man verliert aber dadurch nichts, sondern gewinnt etwas dazu :)</li>
    <li>Profi-Tipp: Im Popup der Lifteinträge befindet sich die Option "Favoriten verwalten". Zusammen mit den GS können damit einfach Mengenoperationen wie Vereinigen oder Schneiden zwischen Favoriten und den GS durchgeführt werden.</li>
    <li>Falls man aus Versehen seine aktuelle Suche im Suchschlitz verworfen hat (das X ist nah), kann der <b>Suchverlauf</b> helfen. Er speichert die letzten 10 Einträge.</li>
</ul>
<br id="such-token"/>
<h2>Such-Token</h2>
<ul>
    <li>Um mehr über die Bereichssuchen zu erfahren, sollte man im Liftmenü die Option "Such-String & Zusatz-Infos(*) anzeigen" wählen. Am konkreten Beispiel versteht man es am besten. Diese sind definiert:
        <p><ul>
            <li>PR provider - <a href="#symbol">Icon</a></li>
            <li>SN station name</li>
            <li>SI station id</li>
            <li>DT device type - <a href="#symbol">Icon</a></li>
            <li>DI device id</li>
            <li>DS device status - <a href="#symbol">Icon</a></li>
            <li>DD device description</li>
            <li>DR device replacement text</li>
            <li>BH barrier-free (platform) height</li>
            <li>AI additional information</li>
            <li>AZ alarm zzzleeps</li>
            <li>MX manual extension</li>
        </ul></p>
    </li>
    <li><i>Verschiedene</i> Token werden untereinander immer UND verknüpft - wenn man die <i>gleichen</i> Token mehrfach benutzt, wird nachfolgende Suchsemantik benutzt.</li>
    <li>Die IDs (SI, DI) werden nur exakt (also nicht fragmentarisch) gefunden und untereinander ODER verknüpft. Man kann somit Listen bilden.</li>
    <li>Wenn man DR# oder AZ# in den Suchschlitz eingibt, bekommt man alle Lifte, die umbenannt oder zurückgestellt sind.</li>
    <li>AI untereinander werden UND verknüpft. Innerhalb AI sind damit weitere Subsuchen möglich, z.B. nach DB-internen IDs oder der Bahnmeisterei.</li>
    <li>Alle anderen werden untereinander ODER verknüpft - dt#b dt#a würde beispielhaft "<b>B</b>ahnhöfe ohne Lifte" und die "<b>A</b>ufzüge" selektieren. Siehe auch <a href="#symbol">Icons der Liftliste</a> </li>
</ul>
<br id="stationsliste"/>
Spezialfeature Stationsliste
<p>Die Einträge der Liftliste sind (pro Station) durchnummeriert - mit PR#{1} bekommt man Provider-übergreifend den ersten Eintrag und damit quasi eine Liste aller Stationen, egal aus welcher Quelle sie stammt. "Stationsliste (1.Lift)" ist unter "Vordefinierte Suchen" verfügbar.
</p>

<div style="text-align:right;padding-right:20px;"><a href="#inhaltsverzeichnis">back to top</a></div>
<br id="pläne-und-karten"/>
<h1>Pläne und Karten</h1>
<p>Liftchecker bietet im Popupmenü jedes Listeneintrags kontextspezifische Informationen an, z.B. Station auf <a href="#geodaten">Karte</a> anzeigen. Ein Bahnhofsplan kann die Orientierung und die Einschätzung bzgl. der persönlichen Barrierefreiheit erleichtern, oder auch dazu benutzt werden, den Eintrag in der App einem Lift in der Realität zuzuordnen. Folgendes wird über das Popup-Menü in der Liftauswahl angeboten.
</p>
<ul>
    <li>Für alle MVG-Stationen ist die interaktive Zoom-Liftkarte und ein MVV-Bahnhofsplan aufrufbar.</li>
    <li>Bei der DB haben wir bahnhof.de eingebunden.</li>
    <li>Für die MVV-Pläne setzen wir die Klartextbezeichnungen der Stationen um und rufen deren zentrale PDF-Sammlung auf. Dies funktioniert für alle Stationen im Großraum München.</li>
    <li>Für die DB benutzen wir die Station-ID (im Such-String SI#) und lösen diese über Listen zur sog. DS100, IFOPT und zur Eva-Nr auf (im Such-String unter AI# ersichtlich) und rufen damit eine URL des jeweiligen Anbieters auf. </li>
    <li>Empfehlenswert für bayerische Stationen generell, auch wenn sie über den MVV-Bereich hinausgehen, sind die Bahnhofskarten von Bayern-Takt.</li>
    <li>Bei der DB konnten wir die bekannte blaue Bahnhofstafel (Ankunft- und Abfahrtszeiten der Züge) einbinden. </li>
    <li>Der MVV bietet Abfahrtsinformationen sogar bundesweit, im Großraum München ist das Angebot größer als außerhalb davon.</li>
</ul>
<p>Im Hauptmenü der Ansicht "Liftliste" befindet sich der Menüpunkt "Pläne und Links". Hier werden kontext-<i>un</i>spezifische Informationen bereitgestellt. Der bahnhofsspezifische Teil ist im Long-Klick-Menü des jeweiligen Listeneintrags. Folgende Links auf interessante Infos haben wir zusammengetragen:
</p>
<ul>
    <li>Von der MVG gibt es für den gesamten MVV-Bereich den bekannten Netzplan als PDF ergänzt um Einstiegshöhen und einer Einschätzung zur Barrierefreiheit</li>
    <li>Allgemeine Infos der DB für barrierefreies Reisen: Mobilitätsservice-Zentrale, Reiseplanung, Beratung, Angebote und Vergünstigungen, sowie Ihre Rechte und Reiseziele</li>
    <li>Stationslisten und Umbaupläne der Deutschen Bahn bzgl. der Barrierefreiheit der S-Bahn München</li>
    <li>Live Map: Wo befindet sich meine S-Bahn auf der Strecke gerade?</li>
</ul>

<div style="text-align:right;padding-right:20px;"><a href="#inhaltsverzeichnis">back to top</a></div>
<br id="geodaten"/>
<h1>Geodaten</h1>
<p>Unsere App</p>
<ul>
    <li>verfügt über eine Integration mit <i>OrganicMaps</i> (einem Fork von MapsMe), einem tollen Projekt mit ähnlichen Wertevorstellungen wie unsere. OM zu nutzen erfordert eine Installation (z.B. über einen Android-App-Store). OM ist eine Offline-Karten-App, welche aus Liftchecker heraus aufgerufen werden und so die Liftchecker-Stationen (und deren Sammelstatus) auf einer Karte visualisieren kann. Der Sammelstatus einer Station kann sein: a) grün - barrierefrei passierbar, b) rot - Barriere(n) vorhanden, c) grau - unbestimmt, d) braun - inaktuell. LC ruft OM aus dem <i>aktuellen</i> Kontext heraus auf, d.h. wenn man im LC nur Aufzüge in der Liste hat, wird im OM auch nur der Status dieser Aufzüge (zusammengefasst auf Stationen) angezeigt - Rolltreppen werden also dann nicht berücksichtigt. Man hat somit insbesondere über die <a href="#suche">Suche</a> selbst die Kontrolle, welchen Gesamtstatus man im OM sieht. Am besten öffnet man OM parallel zu LC und wechselt zwischen den Apps: Ein Long-Klick auf den Text einer Kartenmarkierung kopiert den Stationsnamen in die Zwischenablage, diesen Text dann im LC suchen - dort bekommt man die Details, warum ein Status nicht grün ist. Wer die Kartenmarkierungen wieder loswerden will, führt in OM eine Suche aus. </li>
    <li>bietet im Liftmenü (Long-Klick auf einen Eintrag in der Liftliste) die Möglichkeit Geodaten zu nutzen <i>ohne</i> dass Berechtigungen für den Standort erteilt werden müssen. Es kann ein Listeneintrag als Zentrum festlegt werden. Sodann werden in der Liftliste die Distanzen dieses Ortes zu den anderen sichtbaren berechnet und angezeigt. </li>
    <li>kann die Einträge der Liftliste entweder nach geografischer Distanz oder in alphabetischer Reihenfolge sortiert darstellen. Da die Distanz-Berechnung nicht unaufwändig ist - obwohl nur ein einfacher, ungenauer Algorithmus verwendet wird - kann das für umfangreiche Listen einen Moment lang Zeit benötigen. Deswegen haben wir auf eine automatische Umschaltung verzichtet. Man hat die Möglichkeit dies im Liftmenü über "Liste sortieren" anzustoßen. Wenn ein Geo-Bezugspunkt ausgewählt ist, wird nach der Distanz zu diesem sortiert. Falls nicht, nach alphabetischer Reihenfolge.</li>
    <li>ermöglicht Karten direkt aufzurufen: a) Google Maps b) Organic Maps c) Handy-spezifische Integration über die Textselektion der Geokoordinaten aus dem Such-String. Wenn man dort Text so auswählt <span style="font-family:courier;">geo:[ <span style="background-color:#AAAAAA;">52.67556, 13.59264</span> ]</span> sollte das Gerät erkennen, dass es sich dabei um Geokoords handelt und einen entsprechenden Menüpunkt, z.B. "Karte öffnen" anbieten. Tipp: dies funktioniert für Adressen, Telefonnummern (z.B. die in die App integrierten Nummern der 3S-Zentrale sowie des Mobility-Service), u.a. oft auch. </li>
    <li>hat uns ermöglicht die Geodaten der Lifte aus den Online-API-Calls einfach zu untersuchen - da dabei sich einige Detail-Infos als ziemlich irreführend herausstellten, haben wir uns entschieden nicht für jeden Lift diese Details zu verwenden, sondern statische Stationsdaten. Somit kann man also mit unserer App <i>keine</i> Annäherungsverfolgung an einen bestimmten Lift vornehmen - alle Lifte einer Station haben die gleiche Koordinate. </li>
    <li>besitzt <i>keine</i> Meldefunktionen (zur Datenverbesserung der <i>Anbieter-Informationen</i>), da wir leider selbst über keinen "direkten Draht" zu den Anbietern der Online-Schnittstellen verfügen, der solche Informationen verarbeiten könnte. Wenn SnfiCert-Bewertungen korrigiert werden sollen, kann man die <a href="#fehler-melden">Support-Mailadresse</a> nutzen.</li>
</ul>

<div style="text-align:right;padding-right:20px;"><a href="#inhaltsverzeichnis">back to top</a></div>
<br id="datenschutz"/>
<h1>Datenschutz</h1>
<p>Liftchecker</p>
<ol>
    <li>fragt die in der <a href="#kurzbeschreibung">Einleitung</a> genannten zwei Online-Liftstatus-Datenquellen im Internet ab - weitere Datenquellen werden durch die App nicht abgerufen. Die dadurch stattfindende Datenverwendung der jeweiligen Anbieter haben wir nicht unter Kontrolle - diese Schnittstellen sind aber offiziell - auch für die hier vorliegende Form der Nutzung - freigegeben. Falls man die Integrationsmöglichkeiten nutzt, sollte offensichtlich sein, dass hierzu im Browser die entsprechende URL, bzw. eine andere App aufgerufen wird, sowie welche Informationen dazu übermittelt werden müssen - Snfiware übermittelt hierbei stets nur die für den jeweiligen Zweck notwendigen Daten. </li>
    <li>selbst speichert und verwendet die Benutzereingaben, damit es seinen offensichtlichen Zweck - Liftstatus abfragen - erfüllen kann und in keinem Maße über die hier genannten Punkte hinaus. Die Auswahl der Lifte stellen keine personenbezogenen Daten im engeren Sinne dar und sind damit datenschutzrechtlich grundsätzlich als unbedenklich einzustufen. Die App fragt die Daten ab, so und wie sie eingestellt wurden. Es werden durch Liftchecker <i>keine anderen</i> Übertragungen oder Verarbeitungen durchgeführt. Snfiware ist Datenschutz und Privatsphäre sehr wichtig. Tatsächlich könnte natürlich beim jeweiligen Dienst durch die Abfrage und die dadurch übermittelte Liftauswahl in Verbindung mit Zeit und verwendetem Endgerät ein Rückschluss auf personenbezogene Informationen möglich sein. </li>
    <li>schreibt Protokolleinträge in den geräteinternen LogCat-Ringpuffer (dies ist ein Bereich fester Größe, der ständig im Hintergrund durch Android und die Apps geschrieben und regelmäßig wieder überschrieben wird). Durch Liftchecker werden nur in der und durch die App selbst verfügbare, sowie in die App eingegebene - als auch über die zwei Schnittstellen erlangten - Daten, App-interne Verlaufsinformationen und Informationen zum Zwecke der Fehleranalyse verarbeitet und ggf. ins Log geschrieben - es werden darüber hinaus weder lokal noch anderweitig verfügbare Infos erhoben noch verarbeitet. Wir bieten eine integrierte <a href="#fehler-melden">Funktion zur Fehlermeldung</a> an, welche daraus eine Logdatei erstellen und bereitstellen kann. Solange sie diese Funktion nicht nutzen, bleiben Log-Informationen vollständig lokal und werden regelmäßig überschrieben. Die aus dem LogCat erstellte Log-Datei <i>könnte tatsächlich</i> datenschutzrechtlich relevante Informationen enthalten, da sie mittels APIs des Betriebssystems zusammengestellt wird - diese Interna haben wir nicht unter Kontrolle. Die Logdatei kann aber vor einer Übermittlung an uns überprüft werden. Das Verhalten der Protokollierung kann in der App grundsätzlich eingestellt werden. Falls generellere Vorgaben gewünscht werden, empfehlen wir, sich mit "Android ADB LogCat" zu beschäftigen (googlen).</li>
</ol>

<div style="text-align:right;padding-right:20px;"><a href="#inhaltsverzeichnis">back to top</a></div>
<br id="rechtliches"/>
<h1>Rechtliches</h1>
<p>Copyright 2023 Snfiware</p>
<p>Licensed under the Apache License, Version 2.0 (the "License"); you may not use this software except in compliance with the License. You may obtain a copy of the License at: http://www.apache.org/licenses/LICENSE-2.0</p>
<p>Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.</p>
<p>Kurz zusammengefasst und in Deutsch:</p>
<ul>
    <li>Wir haben diese Software für eigene Zwecke erstellt und benutzen sie auch weiterhin selbst. Da wir der Meinung sind, dass sie auch für andere von Nutzen sein könnte haben wir entschieden sie zu veröffentlichen.</li>
    <li>Die Nutzung erfolgt auf eigene Gefahr.</li>
    <li>Der Sourcecode ist unser Eigentum und nicht veröffentlicht - eine Verwendung durch Dritte ist nicht erwünscht.</li>
    <li>Die App stellen wir kostenfrei, ohne Werbung und ohne andere Interessen zur <i>freien</i> Nutzung zur Verfügung, damit Mobilitätseingeschränkte hoffentlich durch sie seltener vor defekten Liften stehen werden. <b>Jede kommerzielle Nutzung der App ist untersagt.</b></li>
    <li>Trotz umfangreicher Tests und Umsicht kann Fehlverhalten nicht gänzlich ausgeschlossen werden. Wir übernehmen keine Haftung für jedwede entstandene Schäden.
    </li>
</ul>

<div style="text-align:right;padding-right:20px;"><a href="#inhaltsverzeichnis">back to top</a></div>
<br id="hinweise"/>
<h1>Hinweise</h1>
<p>Liftchecker benutzt folgende Software-Bibliotheken. Herzlichen Dank an die jeweiligen Hersteller für die Möglichkeit ihr Produkt kostenfrei nutzen zu können!</p>
<ul>
    <li>com.android.volley</li>
    <li>com.google.android.material</li>
    <li>com.google.code.gson</li>
    <li>org.apache.commons-csv</li>
</ul>
<p>Liftchecker hat statische Daten eingebunden. Ebenfalls herzlichen Dank für die kostenfreie Bereitstellung! Die Lizenzhinweise dazu:</p>
<ul>
    <li>Geokoordinaten aus https://www.mvv-muenchen.de/fahrplanauskunft/fuer-entwickler/opendata/index.html<br/>
        Abrufdatum 19.04.2023
        Creative Commons Attribution License (cc-by)
        Quellenangabe "Münchner Verkehrs- und Tarifverbund GmbH (MVV)"
        Datenstand gem. Übersicht: 29.12.2022
    </li>
    <li>Geokoordinaten, Adress- und Zusatzdaten https://data.deutschebahn.com/<br/>dataset/data-haltestellen.html<br/>sowie https://data.deutschebahn.com/<br/>dataset/data-stationsdaten.html</li>
</ul>
<br id="kompatibilität"/>
<h2>Kompatibilität</h2>
<p>
    Android 4.4 (API 19 - Kitkat) ist die älteste Version, die von Liftchecker unterstützt wird. In dieser Version ist ab Werk SSL veraltet, d.h. die in Liftchecker genutzten Online-SNITs werden mit Fehler abbrechen, da sie über HTTPS kommunizieren. Abhilfe kann ein Update der Google Play Services auf die Version 5.0 (API 21 - Lollipop) bringen - dies haben wir nicht verifiziert, haben aber wegen dieser Möglichkeit die Unterstützung für 4.4 erhalten.
</p>
<br id="spezialfälle"/>
<h2>Spezialfälle</h2>
<ul>
    <li>Kein Lift über die Online-Schnittstelle
        <p>Wenn von der Online-Schnittstelle gar keine Lift-Info zu einer Station geliefert wird, wird für sie ein virtueller Eintrag "<a href="#symbol">Bhf.o.Lift</a>" aus den statisch eingebundenen Stationsinformationen generiert. Da die MVG in jeder Station mindestens einen Lift hat, trifft dieser Fall nur für die DB zu. Wir arbeiten mit diesen sog. "virtuellen Einträgen" damit auch für liftlose Stationen die <a href="#pläne-und-karten">Möglichkeiten</a> der App genutzt werden können. </p>
    </li>
    <li>Statisch vs. Online
        <p>Warum haben wir uns dafür entschieden statische Stationsinformationen aufzubereiten und einzubinden? Die DB-Online-Listenabfrage liefert - um die Datenübertragung schlank zu halten - nur eine Station-ID (vgl. auch <a href="#such-token">Such-Token</a>). Diese ist für den Anwender zunächst nichtssagend und muss in Klartext aufgelöst werden. Außerdem sollen weitere Zusatzinformationen der Station verwendet werden, die nicht direkt über die Lift-API kommen. Diese Ermittlung hätten wir gerne gegen eine API durchgeführt, da sich die Informationen natürlich ändern können und man damit aktuell bliebe. Jedoch haben wir leider keine API gefunden, die dies vollständig für alle Stationen leistet und darüber hinaus haben wir bei Versuchen mit potenziellen Kandidaten festgestellt, dass wichtige Infos, wie z.B. "steplessAccess" zeitweise offensichtlich falsch waren.</p><p>Bei der MVG haben wir statische Infos eingebunden, da in der Online-Schnittstelle zwar x/y kommt, dies aber keinem uns bekannten Format entspricht und es damit für eine Anzeige der Stationen auf einer <a href="#pläne-und-karten">Karte</a> für uns nicht tauglich war.</p> </li>
    <li>Neuer Bahnhof
        <p>Wenn die Online-Schnittstellen eine Stations-ID liefern, die gegenüber den statischen unbekannt sind, wird zunächst beim <a href="#such-token">Stationsnamen</a> [<i>&lt;Stations-ID></i> N/A] angezeigt. Man kann sich damit behelfen, den Lift als Favoriten auszuwählen und ihn zu prüfen - hierbei wird zumindest der Name aktualisiert - vollständige Zusatzinformationen gibt es damit aber leider nicht. Snfiware bemüht sich dies nach Kenntniserlangung zeitnah ab- und eine neue Version <a href="#teilen">bereitzustellen</a>.</p>
    </li>
    <li>Fehlende Liftbeschreibung
        <p>Dies führt im Liftchecker zur Anzeige NO-DESC. Es sind leider in der Fasta-Schnittstelle der DB praktisch ständig solche Daten vorhanden (z.Zt. ca. 50 Lifte), die für den Anwender natürlich einigermaßen nichtssagend sind. Wir haben sie aber nicht ausgefiltert, da ansonsten der Liftstatus auch weg wäre - dieser könnte ggf. in der Gesamtschau aller Status einer Station noch Aufschluss geben. Bedauerlicherweise kann das Problem nicht von Snfiware gelöst werden. Man kann 'Lift umbenennen' im Liftmenü verwenden. Die DB-Schnittstelle stellt die sog. stateExplaination zur Verfügung - diese wird ggf. als Klammerzusatz [SE:<i>db-text-der-schnittstelle</i>] ausgegeben.</p>
    </li>
    <li>Status bei liftlosen Stationen mit DB-Stufenlos:ja
        <p>Ohne Zusatzinformationen wäre es falsch einen Listeneintrag eines liftlosen Bahnhofs nur aufgrund "DB-Stufenlos:ja" auf einen anderen Wert als "?" zu setzen. Der Bahnsteig mag wohl komplett stufenlos sein, wenn jedoch z.B. die Bahnsteighöhe zu niedrig wäre, dann kann man ggf. deswegen nicht in den Zug einsteigen. Tipp: Im Liftmenü bahnhof.de wählen. Mit ein wenig Glück kann dort unter "Ausstattung für Barrierefreiheit" die Option Bahnsteighöhen abgefragt werden. </p>
    </li>
</ul>
<br/>
<br/>
</body>
</html>
