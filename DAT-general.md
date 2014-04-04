# Datenstrukturen - general
* Sie können mindestens 4 Eigenschaften von Datenstrukturen benennen und erklären.

    * Zugriffsmöglichkeiten (allgemein)
        * Einfügen
        * Entfernen
        * Suchen

    * Zugriffsmöglichkeiten (bezüglich Ordnung, d.h. Grösse, Priorität usw.)
        * nachfolgendes Element
        * vorangehendes Element
        * grösstes Element
        * ...
 
    * Zugriffsaufwand *Big O Notation*
        * Einfügen in unsortiertes Array hat *O(1)*
        * Entfernen aus unsortiertem Array hat *O(n)*
        * ...

    * statisch vs. dynamisch

        | statisch                      | dynamisch                         |
        |-------------------------------|-----------------------------------|
        | fixe Grösse                   | keine fixe Grösse                 |
        | vor dem Kompilieren fixiert   | Grösse variiert während Laufzeit  |
        | Bsp.: Array                   | Bsp.: ArrayList                   |
         
    * explizite vs. implizite Datenstrukturen

        | explizit                      | implizit                          |
        |-------------------------------|-----------------------------------|
        | Beziehungen mit Referenzen    | Beziehungen mit Formeln           |
        | Bsp.: List, Baum              | Bsp.: Array, Heap                 |
     
    * direkter vs. indirekter Zugriff

        | direkt                        | indirekt                          |
        |-------------------------------|-----------------------------------|
        | unmittelbarer Zugriff         | kein direkter Zugriff             |
        | Technik: Index                | Technik: Iterator                 |
        | Bsp.: Array                   | Bsp.: Set                         |

* Sie können an einem Beispiel die gegenseitige Abhängigkeit von Algorithmus und Datenstruktur aufzeigen.

    Die Fibonacci-Zahlenfolge kann iterativ oder rekursiv implementiert werden (Algorithmus).
    Je nach dem wie man die Zahlen arrangiert (Datenstruktur) verändern sich der Aufwand benötigter 
    Ressourcen

    * Rekursive Implementierung
        * benötigt viel Speicher (Stack)
        * ist langsam (da gleiche Werte mehrfach gerechnet werden)
        * sehr einfacher (eleganter) Algorithmus

                static int fibonacci(int n){
                    if (n == 0) return 0;
                    if (n == 1) return 1;

                    return fibonacci(n-1) + fibonacci(n-2);
                }

    * Iterative Implementierung (mit Array)
        * benötigt viel Speicher 
        * ist sehr schnell
        * etwas umständicher (nicht eleganter) Algorithmus 

                stativ int fibonacci(int n){
                    if (n == 0) return 0;
                    if (n == 1) return 1;

                    int a = 0;
                    int b = 0;
                    int result = 0;

                    for(int i = 2; i <= n; i++){
                        result = a + b;
                        b = a;
                        a = result;
                    }
                }

    | n         | Rekursiv                  | Iterativ      |
    |-----------|---------------------------|---------------|
    | 5         | 5 ticks                   | 9 ticks       |
    | 10        | 36 ticks                  | 10 ticks      |
    | 20        | 2315 ticks                | 10 ticks      |
    | 30        | 180254 ticks              | 10 ticks      |
    | 100       | too long/stack overflow   | 11 ticks      |
    | 1000      | too long/stack overflow   | 27 ticks      |
    | 10000     | too long/stack overflow   | 190 ticks     |
    | 100000    | too long/stack overflow   | 3952 ticks    |
      
 
* Sie können für Array und Liste den Aufwand für die elementaren Zugriffsoperationen angeben.

    | Datenstruktur     | Einfügen  | Suchen    | Entfernen | Nachfolger    | Vorgänger | sortierte Ausgabe |
    |-------------------|-----------|-----------|-----------|---------------|-----------|-------------------| 
    | Array unsortiert  | *O(1)*    | *O(n)*    | *O(n)*    | nein          | nein      | nein              |
    | Array sortiert    | *O(n)*    | *O(log n)*| *O(n)*    | ja            | ja        | ja                |
    | Liste unsoertiert | *O(1)*    | *O(n)*    | *O(n)*    | nein          | nein      | nein              |
    | Liste sortiert    | *O(n)*    | *O(n)*    | *O(n)*    | ja            | nein      | ja                |
 
* Sie können die Implementierung einer einfachen Liste im Detail verstehen und illustrieren.

    Eine einfache (einfach verkettete) Liste besteht aus **nodes** welche Daten und einen Pointer zur
    nächsten node enthalten.

    ![alt text](linked-list.png "linked list")
 
* Sie können eine einfache Liste selber implementieren.

    Um eine einfach verkettete List zu implementieren braucht es 
        * eine Klasse für die nodes
        * eine Klasse für die Liste

    Node.java

            public class Node{
                private String data;    // the data is of type String in this example
                private Node next;      // pointer to the next node in the list
                
                public Node(Node n, String d){
                    next = n;
                    data = d;
                }

                public void setData(String d){
                    data = d;
                }

                public String getData(){
                    return data;
                }

                public void setNext(Node n){
                    next = n;
                }

                public Node getNext(){
                    return next;
                }

            } 

* Sie können begründen, weshalb Generics insbesondere bei Datenstrukturen vorteilhaft sind.
* Sie können erklären, wie die Stack (Stapel) Datenstruktur funktioniert. 
* Sie können erklären, wie die Queue (Warteschlange) Datenstruktur funktioniert. 
* Sie können eine Queue und einen Stack implementieren. 
* Sie kennen Anwendungen für die Datenstrukturen Stack und Queue. 
* Sie können die Funktionsweise und den Einsatz von doppelt verketteten Listen erläutern. 
* Sie können Einfügen und Löschen in einer doppelt verketteten Liste mit einer Skizze detailliert erläutern. 
