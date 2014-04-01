# GUI Programmierung
* Sie können mindestens je 2 elementare GUI - Komponenten, Container und Layout - Manager benennen und identifizieren.

    | GUI-Komponente    | Container | Layout-Manager |
    |-------------------|-----------|----------------|
    | Label             | Frame     | GridLayout     |
    | Button            | Applet    | FlowLayout     |
    | Textbox           | Dialog    | BoxLayout      |

* Sie können prinzipiell den Aufbau eines GUI erklären.

    GUIs bestehen aus drei Grundlegenden Systemkomponenten 
    * elementare GUI Komponenten (Label, Button usw.)
    * Container (unsichtbare wie Panel und sichtbare wie Frame)
    * Layout-Manager (dieser arrangiert Container-Inhalte z.B. Buttons)

* Sie können prinzipiell die Bildschirmausgabe in Windowsystemen erklären.

    * Jede Component (Button usw.) hat eine Methode `pain(Graphics g)` zum Zeichnen der Komponente
    * Das Fenstersystem ruft die Methode `paint()` automatisch auf
    * Ein Java-programm kann ein neuzeichnen forcieren mit `repaint()` (was schlussendlich ein `paint()` ausführt) 

    

        repaint

* Sie kennen die Merkmale eines sequentiellen und eines ereignisgesteuerten Programms.

    * Sequentiell: Aneinanderreihung von Befehlen (Bsp.: SBB Billetautomat)
    * Ereignisgesteuert: Erst bei Ereignis werden Befehle ausgeführt (Bsp.: Games)

* Sie können das Zusammenspiel zwischen Event-Quelle und Event-Listener erklären. 

    * Eventlistener registriert sich bei Eventquelle und wird bei einem entsprechenden Ereignis benachrichtigt

* Sie können ein einfaches Java - Programm mit GUI (AWT) und Event - Handling analysieren und implementieren.  
   
* Sie kennen Vor - und Nachteile von Swing und wissen, wie man graphische User-Interfaces mit Swing erzeugt.

    | Vorteile                            | Nachteile          |
    |-------------------------------------|--------------------|
    | Sieht auf allen Systemen gleich aus | Ressourcenintensiv |
    | Braucht keine Systembibliotheken    | - |

* Sie kennen wichtige Komponenten von Swing und deren Einsatzmöglichkeit.

    * J... von AWT
    * JRadiobutton
    * JCombobox
    * JRootPane
