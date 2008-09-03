==========================================================================

= = = = = = = = = = = = =  SeaMonkey Read Me   = = = = = = = = = = = = = =

==========================================================================

Die Benutzung von SeaMonkey ist an die Bedingungen der beiliegenden 
Lizenzvereinbarung gebunden.

Diese ReadMe-Datei enth�lt Informationen �ber System-Voraussetzungen 
sowie Installations-Anweisungen f�r SeaMonkey unter IBM OS/2. 

Mehr Informationen �ber SeaMonkey finden Sie unter 
http://www.seamonkey-project.org/. 
Mehr Informationen �ber den OS/2-Port von SeaMonkey finden Sie unter
http://www.mozilla.org/ports/os2.
Um Fehler und sonstiges Feedback zu melden, sehen Sie sich
http://www.seamonkey-project.org/dev/get-involved an. Sehen Sie sich auch 
Bugzilla unter der Adresse  https://bugzilla.mozilla.org/ an, um bereits 
bekannte Fehler, Richtlinien zum Erstellen von Fehlerbereichten und mehr zu 
finden. 
Um Hilfe mit Bugzilla zu bekommen, k�nnen Sie Sich auch mit Ihrem 
IRC-Client in #mozillazine auf irc.mozilla.org melden.
Probleme welche speziell OS/2 betreffen k�nnen sie auf #warpzilla und in der
Newgroup mozilla.dev.ports.os2 auf news.mozilla.org diskutieren.


====================================================

                 SeaMonkey erhalten

====================================================

Sie k�nnen Sich sogenannte "nightly builds" von SeaMonkey vom mozilla.org 
FTP-Server herunterladen.

  http://ftp.mozilla.org/pub/mozilla.org/seamonkey/nightly/contrib/

Die aktuellsten Builds finden Sie unter

  http://ftp.mozilla.org/pub/mozilla.org/seamonkey/nightly/contrib/latest-trunk/

Beachten Sie, dass es sich bei diesen "nightly builds" um Entwicklungsversionen 
handelt, welche von mozilla.org-Entwicklern zum Testen verwendet werden und 
somit Fehler enthalten k�nnen. Wenn Sie lieber eine stabile Version von 
SeaMonkey benutzen m�chten, empfiehlt es sich die offiziellen Release-Versionen
zu verwenden, welche vom SeaMonkey-Projekt in regelm��igen Abst�nden 
herausgegeben werden. Diese finden Sie unter

  http://www.seamonkey-project.org/releases/
 
Lesen Sie auch die Release-Notes f�r SeaMonkey in denen Sie Informationen zu 
bekannten Problemen und m�glichen Problemen bei der Installation von SeaMonkey
nachlesen k�nnen. Die Release-Notes finden Sie unter der oben angef�hrten URL, 
unter der Sie auch die Release-Versionen finden.

OS/2 Releases werden nicht vom SeaMonkey-Projekt oder mozilla.org
selbst erstellt und scheinen auf der Seite http://www.mozilla.org/ports/os2
vor der offiziellen Freigabe auf. Lesen Sie auf jeden Fall die
Release-Notes auf welche von der Release-Seite verwiesen wird.
In diesen stehen bekannte Probleme und Hilfestellungen
zur Installation von SeaMonkey.

====================================================

               Systemvoraussetzungen

====================================================

* OS/2
   - Diese Version ben�tigt die C runtime DLLs (libc-0.6.1) von
     ftp://ftp.netlabs.org/pub/gcc/libc-0.6.1-csd1.zip
     um lauff�hig zu sein. Sie k�nnen diese einfach in das Verzeichnis
     Ihrer SeaMonkey-Installation oder in ein anders Verzeichnis entpacken,
     welches in Ihrer LIBPATH aufscheint. Der SeaMonkey-Installer installierte
     diese C runtime DLLs nicht, ben�tigt diese jedoch um selbst um
     gestartet werden zu k�nnen.

   - Minimale Hardware-Anforderung
     + Intel Pentium Prozessor (oder vergleichbar)
     + 64 MiB RAM sowie 64 MiB freier Swap-Speicher
     + 35 MiB freien Speicher auf der Festplatte f�r die Installations
       sowie weiteren Festplatten-Speicher zum Speichern von Mails und 
       Cache-Daten.

   - Empfohlene Hardware-Voraussetzungen f�r akzeptable Performance
     + 500 MHz Prozessor
     + 256 MiB RAM sowie 64 MiB freier Swap-Speicher
       HINWEIS: Die Performance von SeaMonkey sowie dessen Stabilit�t erh�hen 
       sich je mehr physikalischer RAM-Speicher verf�gbar ist. Insbesondere 
       wenn Sie l�nger im Internet s�rfen oder IRC verwenden, wird mindetens
       512 MiB RAM empfohlen.

   - Software-Anforderungen
     + Installation auf einem Dateisystem, welches lange Dateinamen unterst�tzt
       (z.B. HPFS oder JFS jedoch nicht FAT)
     + OS/2 Warp 4 mit Fixpack 15 oder h�her
     + MPTS Version 5.3
     + TCP/IP Version 4.1
     + INETVER: SOCKETS.SYS=5.3007, AFOS2.SYS=5.3001, AFINET.SYS=5.3006
       HINWEIS: Versuchen Sie nicht eine MPTS und TCP/IP Version �lter als die 
       oben genannten INETVER-Levels zu verwenden. Auch wenn Seamonkey mit 
       diesen �lteren Netzwerk-Stacks startet und normal zu funktionieren 
       scheint. Einige Funktionen von Seamonkey sind in diesen Versionen nicht 
       korrekt vorhanden und k�nnen zu einem Absturz oder Datenverlust f�hren.

     + Convenience-Pack 2, eComStation 1.0 und sp�ter erf�llen diese 
       Voraussetzungen bereits.


====================================================

            Installationsanleitung

====================================================
Es wird empfohlen, alle Programme zu schlie�en bevor Sie das Setup starten.
Sie sollten weiterhin alle Antivirus-Software f�r die Dauer der Installation
deaktivieren.

Installieren Sie in ein sauberen (neues) Verzeichnis. Wenn Sie eine bestehende
Installation �berschreiben kann dies zu Problemen f�hren.

Hinweis: Diese Anleitung erkl�rt nicht, wie Sie SeaMonkey selbst bauen k�nnen.
Informationen, wie Sie SeaMonkey aus dem mozilla.org - Sourcecode selbst 
erstellen k�nnen, finden Sie unter

  http://developer.mozilla.org/en/docs/Build_Documentation


OS/2 Installationanleitung
------------------------------

   Um SeaMonkey �ber den heruntergeladenen SeaMonkey-Installer
   zu installieren, folgen Sie folgenden Schritten:

   1. Klicken Sie auf den Verweis zu "Installer" auf der Seite von welcher 
      Sie SeaMonkey herunterladen, um den SeaMonkey-Installer zu bekommen. 
      Die Datei wird �blicherweise seamonkey-x.xx.en-US.os2.installer.exe 
      benannt, wobei "x.xx" der entsprechenden SeaMonkey-Version entspricht.

   2. �ffnen Sie den Ordner in welchem Sie die Datei abgespeichert
      haben, stellen Sie sicher, dass sich die C runtime DLL's im
      selben Ordner oder im LIBPATH befinden und doppelklicken Sie
      die Datei um das Setup-Program zu starten.

   3. Folgen Sie den Anweisungen des Setupprogramms am Bildschirm.
      Das Setup-Program beendet selbstst�ndig alle offenen 
      SeaMonkey-Instanzen und erstellt einen SeaMonkey-Ordner am Desktop.
      Um SeaMonkey zu starten m�ssen Sie wiederum sicherstellen, da�
      die C runtime DLL's im Installations-Verzeichnis oder im LIBPATH
      vorhanden sind. Dannach k�nnen Sie SeaMonkey mit einem Doppelklick
      auf das SeaMonkey-Symbol im Ordner starten.

    Um Mozilla manuell duch die heruntergeladene .zip-Datei zu installieren, 
    folgen Sie folgenden Schritten:
    
   1. Klicken Sie auf den Verweis zu "Zip" auf der Seite von welcher Sie
      SeaMonkey herunterladen, um das SeaMonkey-ZIP Packet zu bekommen. Die 
      Datei wird �blicherweise seamonkey-x.x.x.en-US.os2.zip  benannt, wobei
      "x.xx" der entsprechenden SeaMonkey-Version entspricht.

   2. �ffnen Sie den Ordner in welchem Sie die Datei abgespeichert haben
      und entpacken Sie die ZIP-Datei mein einem Enpacker-Programm Ihrer Wahl.

   3. Beachten Sie, da� beim Entpacken ein Verzeichnis Namens "seamonkey" 
      unterhalb des Zielordners erstellt. z.B.
      unzip seamonkey-1.7.5.en-US.os2.zip -d c:\seamonkey-1.7.5
      entpacket SeaMonkey in das Verzeichnis c:\seamonkey-1.7.5\seamonkey.

   4. Stellen Sie sicher, da� Sie nicht in das Verzeichnis einer alten
      Installation entpacken. Dies kann zu Problemen f�hren.

   5. Um SeaMonkey zu starten, wechseln Sie in das Verzeichnis in welches
      Sie SeaMonkey entpackt haben, stellen sicher, da� sich die C runtime
      DLL's im Verzeichnis oder im LIBPATH befinden und doppelklicken
      auf das seamonkey.exe - Objekt.


Mehrere Versionen von SeaMonkey gleichzeitig verwenden
------------------------------------------------------

Da verschiendene Progamme der Mozilla-Familie (z.B. SeaMonkey, Mozilla,
Firefox, Thunderbird, IBM Web Browser) verschiedene, nicht kompatible
Versionen der selben DLL's verwenden, sind einige extra-Schritte notwendig
um diese Programme nebeneinander laufen zu lassen.

Eine M�glichkeit ist die LIBPATHSTRICT-Variable. Um Mozilla-basierende
Programme zu starten, kann man ein CMD-Script wie im folgenden Beispiel
(wo angenommen wird, dass SeaMonkey im Verzeichnis d:\internet\seamonkey
installiert wurde) angegeben erstellen:

   set LIBPATHSTRICT=T
   rem Die n�chste Zeile ist notwendig, wenn mehrere Mozilla-Programm im 
   rem LIBPATH aufgef�hrt sind.
   rem set BEGINLIBPATH=d:\internet\seamonkey
   rem Die n�chste Zeile wird nur ben�tigt, wenn zwei Versionen des selbene
   rem Programms zu starten.
   rem set MOZ_NO_REMOTE=1
   d:
   cd d:\internet\seamonkey
   seamonkey.exe %1 %2 %3 %4 %5 %6 %7 %8 %9

Sie k�nnen auch ein Programm-Objekt erstellen, mit welchem Sie Seamonkey mit
den folgenden Einstellungen starten:

   Pfad und Dateiname: *
   Parameter:         /c set LIBPATHSTRICT=T & .\seamonkey.exe "%*"
   Ausf�hren in:  d:\internet\seamonkey

(Abh�ngig von der System-Konfiguration kann es notwendig sein, die Parameter 
MOZ_NO_REMOTE und/oder BEGINLIBPATH wie im CMD-Script oben angef�hrt
einzuf�gen.)

Schlussentlich, die einfachste Methode ist die "Run!"-Tool von Rich Walsh 
welches im Hobbes Software Archive zu finden ist:

   http://hobbes.nmsu.edu/cgi-bin/h-search?key=Run!

Lesen Sie die Dokumentation des Tools f�r detailierte Information.

Profile-Verzeichnis vom Installtions-Verzeichnis trennen
--------------------------------------------------------

Um das Benutzerprofile (welches die Lesezeichen und alle anderen Modifikationen
enth�lt) vom Installations-Verzeichnis zu trennen, was es Ihnen erm�glicht,
Ihre Einstellungen zu behalten, auch wenn Sie auf eine aktuellere Version 
mittels ZIP-Files updaten, setzen Sie die Variable MOZILLA_HOME auf das 
Verzeichnis Ihrer Wahl.
Sie k�nnen das entwender in der Config.sys tun, oder sie benutzen ein Script
wie oben beschrieben. Wenn Sie zum Beispiel

   set MOZILLA_HOME=f:\Data

hinzuf�gen, werden Ihre Benutzerprofile unter "f:\Data\Mozilla\Profiles" 
erstellt.


Andere wichtige Umgebungs-Variablen
-------------------------------------

Es existieren ein paar Umgebungsvariablen, mit welchen Sie das Verhalten von
SeaMonkey unter OS/2 steuern k�nnen:

- set NSPR_OS2_NO_HIRES_TIMER=1
  Dies bewirkt, dass SeaMonkey nicht den hochaufl�senden Timer von OS/2 
  benutzt. Setzen Sie diese Variable wenn anderen Programme, welche den
  hochaufl�senden Timer (Mutlimedia-Programme) ungewohnt reagieren.

- set MOZ_NO_REMOTE=1
  Benutzen Sie diese Umgebungsvariable um zwie Instanzen von SeaMonkey
  gleichzeitig zu starten (z.B. ein Debug-Build und eine normale Version).

Mehr Informationen �ber dieses Thema unde andere Tipps finden Sie unter
   http://www.os2bbs.com/os2news/Warpzilla.html (english)


Bekannte Probleme der OS/2 Version
----------------------------------

Cross-Plattform Probleme werden normalerweise in den Release-Notes einer jeden
Version erw�hnt.

- SeaMonkey gibt einen Beep-Ton von sich, wenn Sie mehr als 64 kB Text in die
  Zwischenablage kopieren.  Dies ist ein Hinweis dass viele Programme 
  (wie zum Beispiel der Sytem-Editor, EPM sowie Programme welche im 
  VIO Fenster laufen) nicht mehr als dies einf�gen k�nnen.

- SeaMonkey kann OS/2 Schriftarten wie WarpSans oder andere welche
  nicht als Type1 oder TrueType-Format vorhanden sind nicht nutzen.
  Es wird daher empfohlen, die Schriftart "Workplace Sans" von
     http://users.socis.ca/~ataylo00/creative/fonts/
  oder
     http://hobbes.nmsu.edu/cgi-bin/h-search?key=wpsu_ttf
  zu installieren. Diese wird von SeaMonkey als Ersatz f�r
  WarpSans verwendet.

Andere bekannte Probleme finden Sie unter dem Link "Current Open Warpzilla Bugs" 
auf der OS/2 Mozilla-Seite <http://www.mozilla.org/ports/os2/> (Englisch).
