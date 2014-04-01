# Objektorientierte Programmierung
* Sie können mindestens 3 Vorteile der Vererbung erklären

    * Einfache Wiederverwendung (von Implementation)
    * Vermeidung von Code-Duplikation
    * Einfachere Wartbarkeit
    * Einfachere Erweiterbarkeit

* Sie können einen schwergewichtigen Nachteil der Vererbung erläutern

    * Starke Kopplung

* Sie können Substitution und Casting korrekt anwenden.
* Sie können zwischen statischen und dynamischen Typen unterscheiden.
* Sie können bestimmen, welche Implementation für einen bestimmten Methodenaufruf zur Ausführung gelangt.
* Sie können Polymorphie, d.h. Überladen und Überschreiben mittels Java - Code erklären und anwenden.
* Sie können Einfach - und Mehrfachvererbung erläutern und können diese im Klassendiagramm darstellen.
* Sie kennen Kriterien des modularen Entwurfs.
* Sie kennen die Prinzipien des modularen Entwurfs.

# Java
* Sie wissen, wie toString() arbeitet und angepasst werden kann.

    * Name der Klasse \@ Speicheradresse im Heap
    * Kann überschrieben werden. 

* Sie verstehen das Konzept von abstrakten Klassen und abstrakten Methoden und können diese einsetzen.

    * Von abstrakten Klassen können keine Objekte instanziert werden.
    * Klassen, die von akstrakten Klassen abgeleitet werden müssen alle Methoden dieser Klasse implementieren oder sind selbst auch abstrakt.
    * Kein Konstruktor

* Sie kennen Java spezifische Eigenschaften der Vererbung.

    * Keine Mehrfachvererbung von Klassen

* Sie können erläutern, wozu Simulationen verwendet werden können.

    * Um Vorgänge nachzubilden

* Sie können ein Java Interface definieren.

        public interface NameDesInterfaces(){}

* Sie können ein Java Interface in abgeleiteten Klassen implementieren.
        
        @override

* Sie kennen Unterschiede zwischen konkreten und abstrakten Klassen sowie zwischen abstrakten Klassen und Interfaces.      
* Sie wissen, wie Sie in Java Mehrfachvererbung umsetzen können.      
* Sie wissen, wozu man Interfaces verwendet.      
* Sie verstehen das Konzept der inneren Klassen und können dieses für die Implementierung ereignisgesteuerter Java - Applikationen einsetzen. 

    * Eventhandler

# GUI Programmierung
* Sie können mindestens je 2 elementare GUI - Komponenten, Container und Layout - Manager benennen und identifizieren.

    * Label
    * Button
    * textfield
    * checkbox
    * scrollbar
    * list
    * choice
    * texarea
 
* Sie können prinzipiell den Aufbau eines GUI erklären.
* Sie können prinzipiell die Bildschirmausgabe in Windowsystemen erklären.

        paint()

    und

        repaint

* Sie kennen die Merkmale eines sequentiellen und eines ereignisgesteuerten Programms.

    * Sequentiell: Aneinanderreihung von Befehlen
    * Ereignisgesteuert: Erst bei Ereignis werden Befehle ausgeführt

* Sie können das Zusammenspiel zwischen Event - Quelle und Event - Listener erklären. 

    * Eventlistener registriert sich bei Eventquelle und wird bei einem entsprechenden Ereignis benachrichtigt

* Sie können ein einfaches Java - Programm mit GUI (AWT) und Event - Handling analysieren und implementieren.     
* Sie kennen Vor - und Nachteile von Swing und wissen, wie man graphische User - Interfaces mit Swing erzeugt.

    * Vorteile: 
        * Sieht auf allen Systemen gleich aus
        * Braucht keine Systembibliotheken 
    * Nachteile:
        * Ressourcenintensiv

* Sie kennen wichtige Komponenten von Swing und deren Einsatzmöglichkeit.

    * J... von AWT
    * JRadiobutton
    * JCombobox
    * JRootPane

\section{Datenstrukturen}
\begin{itemize}
  \item Sie können mindestens 4 Eigenschaften von Datenstrukturen benennen und erklären. \\
        Zugriffsmöglichkeiten (Elementare Zugriffsmöglichkeit, Zugriffe über eine Ordnung) \\
        Zugriffsaufwand (Zugriffsaufwand in Abhängigkeit zu der Anzahl Elementen) \\
        statisch vs dynamisch (statisch = fixe Grösse, dynamisch = keine fixe Grösse) \\
        explizit vs implizit (explizit: Zugriff über Referenz, implizit: Zugriff ) \\
        direkt vs indirekt (direkt: Jedes Element direkt erreichbar, indirekt: Elemente teilweise über andere Elemente erreichbar)
  \item Sie können an einem Beispiel die gegenseitige Abhängigkeit von Algorithmus und Datenstruktur aufzeigen. \\
        
  \item Sie können für Array und Liste den Aufwand für die elementaren Zugriffsoperationen angeben. \\
        
  \item Sie können die Implementierung einer einfachen Liste im Detail verstehen und illustrieren. \\
        
  \item Sie können eine einfache Liste selber implementieren. \\
        
  \item Sie können begründen, weshalb Generics insbesondere bei Datenstrukturen vorteilhaft sind. \\
        
  \item Sie können erklären, wie die Stack (Stapel) Datenstruktur funktioniert. \\
        
  \item Sie können erklären, wie die Queue (Warteschlange) Datenstruktur funktioniert. \\
        
  \item Sie können eine Queue und einen Stack implementieren. \\

  \item Sie kennen Anwendungen für die Datenstrukturen Stack und Queue. \\

  \item Sie können die Funktionsweise und den Einsatz von doppelt verketteten Listen erläutern. \\

  \item Sie können Einfügen und Löschen in einer doppelt verketteten Liste mit einer Skizze detailliert erläutern. \\

  \item Sie können einen Baum definieren. Sie können den Grad und die Höhe eines Baumes und das Niveau eines Knotens bestimmen. \\

  \item Sie können die Funktionen insert(), print() und search() eines binären Suchbaumes implementieren. \\

  \item Sie kennen das Prinzip des Löschens in einem binären Suchbaum. \\

  \item Sie können einen AVL Baum definieren. \\

  \item Sie kennen 3 verschiedene Betrachtungsweisen für Gleichheit und können je ein konkretes Beispiel dazu erläutern. \\

  \item Sie können die Wichtigkeit von equals() begründen. \\

  \item Sie können equals() gemäss 4 - Schritt - Schema adäquat implementieren. \\

  \item Sie können die Vorteile einer Hashtabelle benennen. \\

  \item Sie können die 3 Punkte des hashCode() - Contractes erläutern \\

  \item Sie können die Methode hashCode() für einfache Fälle implementieren. \\

  \item Sie können den Collection - Begriff erläutern und mindestens zwei Vorteile nennen, die der Einsatz des Java Collections Frameworks mit sich bringt. \\

  \item Sie kennen die Klassenstruktur der Java Collection Interfaces und können diese nutzen. \\

  \item Sie kennen die verschiedenen Collection Views auf eine Map. \\

  \item Sie können für ein gegebenes Problem die geeignete Collection - Klasse auswählen \\
\end{itemize}

