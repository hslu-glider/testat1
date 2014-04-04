# GUI Programmierung
* Sie können mindestens je 2 elementare GUI - Komponenten, Container und Layout - Manager benennen und identifizieren.

    | GUI-Komponente    | Container | Layout-Manager |
    |-------------------|-----------|----------------|
    | Label             | Frame     | GridLayout     |
    | Button            | Applet    | FlowLayout     |
    | Textbox           | Dialog    | BoxLayout      |

* Sie können prinzipiell den Aufbau eines GUI erklären.

    GUIs bestehen aus drei grundlegenden Systemkomponenten 
    * elementare GUI Komponenten (Label, Button usw.)
    * Container (unsichtbare wie Panel und sichtbare wie Frame)
    * Layout-Manager (dieser arrangiert Container-Inhalte z.B. Buttons)

* Sie können prinzipiell die Bildschirmausgabe in Windowsystemen erklären.

    * Jede Component (Button usw.) hat eine Methode `public void paint(Graphics g)` zum Zeichnen der Komponente
    * Das Fenstersystem ruft die Methode `paint()` automatisch auf (z.B. bei einer Änderung der Fensterfgrösse)
    * Ein Java-programm kann ein neuzeichnen forcieren mit `repaint()` (was schlussendlich ein `paint()` ausführt) 

* Sie kennen die Merkmale eines sequentiellen und eines ereignisgesteuerten Programms.

    | Sequentielle Programme            | Ereignisgesteuerte Programme  |
    |-----------------------------------|-------------------------------|
    | Aneinanderreihung von Anweisungen | Idle im Normalfall            |
    | (Wake-Up durch bestimmte Eingabe) | Wake-Up bei Event             |
    | Fester Programmablauf             | Ablauf hängt von Event ab     |
    | Bsp.: Billet und Selecta Automat  | Bsp.: Typische GUI-Anwendung  |

* Sie können das Zusammenspiel zwischen Event-Quelle und Event-Listener erklären. 

    * EventSource (z.B. Button) unterhält eine List mit interessierten EventListener
    * d.h. EventListener registrieren sich bei Eventquellen

    Bei einem eintreffendem Event geschieht folgendes: 
    * Die EventSource (z.B. Button) leitet das Event weiter an registriete Listener
    * Die Listener haben Methoden die bereitstehen um das Event zu verarbeiten
    * Diese bereitstehenden Methoden werden ausgeführt

* Sie können ein einfaches Java-Programm mit GUI (AWT) und Event-Handling analysieren und implementieren.

    Main.java

            public class Main {
                public static void main(String[] args){
                    
                    // create the GUI
                    Calculator cal = new Calculator();
                    
                    // start the ButtonListener
                    ButtonListener bl = new ButtonListener(cal);
                }
            }

    Calculator.java

            public class Calculator extends Frame implements WindowListener {
                    Button btn_Start = new Button("Start");
                    Button btn_End = new Button("End");
                    ...
                    GridLayout gl = new GridLayout(5, 4);
                    Panel keyboard = new Panel(gl);
                    ...
                    public Calculator(){
                        super("hslu-gliders' GUI");
                        ...
                        setSize(HEIGTH, LENGTH);
                        setResizable(false);
                        ...
                        setLayout(new BorderLayout());
                        ...
                        keyboard.add(btn_Start);
                        keyboard.add(btn_End);
                        ...
                        add(keyboard, BorderLayout.CENTER);
                        ...
                        addWindowListener(this);
                        ...
                        ButtonListener bl = new ButtonListener(this);
                        btn_Start.addActionListener(bl);
                        btn_End.addActionListener(bl);
                        ...
                        setVisible(true);
                            

    ButtonListener.java

            public class ButtonListener implements ActionListener{
                private Calculator gui;
                private Computer cp = new Computer();

                public ButtonListener(Calculator gui){
                    this.gui = gui;
                }

                public void actionPerformed(ActionEvent event){
                if(event.getSource() == gui.btn_Start){
                    cp.doStart();
                }
                ...
                if(event.getSource() == gui.btn_End){
                    cp.doEnd();
                }
   
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
