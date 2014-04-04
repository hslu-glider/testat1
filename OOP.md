# Objektorientierte Programmierung
* Sie können mindestens 3 Vorteile der Vererbung erklären

    * Einfache Wiederverwendung (von Implementation)
    * Vermeidung von Code-Duplikation
    * Einfachere Wartbarkeit
    * Einfachere Erweiterbarkeit

* Sie können einen schwergewichtigen Nachteil der Vererbung erlÃ¤utern

    * Starke Kopplung

* Sie können Substitution und Casting korrekt anwenden.

    * Substitution

            public void printName(Animal a){
                    System.out.println(a.name);
            }
            ...
            public static void main(String[] args){
                    ...
                    myDog.printName();
                    myCat.printName();

    * Casting

            public static void main(String[] args) {
                    ....
                    Animal myPet = new Dog();
                    Dog myDog = (Dog) myPet;
                    ...
            }
            

* Sie können zwischen statischen und dynamischen Typen unterscheiden.
    * Statische Typen
    
		Statische Datentype werden bei der Kompilierung und nicht zur Laufzeit festgelegt.
                
				Konto k;

    * Dynamische Typen
    
		Dynamische Datentypen werden werden bei der Ausführung definiert, also zur Laufzeit.

                ...
				k = new Konto();
				k = new Spare();
				k = new Giro();
                ...

* Sie können bestimmen, welche Implementation für einen bestimmten Methodenaufruf zur Ausführung gelangt.
	
    * Stichwort Überladung von Konstruktoren und Methoden.
        
        Es gilt, sobald ein Konstruktor oder Methodenkopf auf dei Eingabe passt
        wird er ausgeführt. Dabei werden zuerst die Unterklassen durchsucht und 
        danach in aufsteigender Reihenfolge die übergeordneten Klassen.
        Siehe Beispiele "Überschreibung" im darauffolgenden Block.
        

* Sie können Polymorphie, d.h. Überladen und Überschreiben mittels Java - Code erklären und anwenden.
	
	* Überladung
		
		Überladene Funktionen oder Konstruktoren erkennt man, dass sie den selben Namen haben, jedoch 
		unterschiedliche Parameter in bezug auf Anzahl, Art und Reihenfolge. (schwache Polymorphie)
				
				...
				public void print(){
				}
				...
				public void print(int space){
				}
				...
				
	* Überschreiben
		
		In abgeleiteten Klassen können Methoden der Oberklasse bei Bedarf verändert (Überschrieben) werden.
		Welche Methode verwendet wird hängt von der Klasse selbst ab.
		
				Konto konto2 = new Konto();
				konto2.print(); // Es wird die print Methode von Konto ausgeführt.  
				
				Giro giro2 = new giro();
				giro2.print(); // Es wird die print Methode von Giro ausgeführt. 
		
				konto2 = giro2;
				konto2.print(); // konto2 ist jetzt ein Giro konto und kennt die print funktion von Giro.
				//die suche nach der Methode Giro startet bei der untersten abgeleiteten Kalsse und endet,
				//sobald die erste methode mit diesem Namen und paramtern gefunden wurde.
				//Überschreibende Methoden können das ausführen von Überschriebenen methoden mit dem Befehl:
				//super.methodenname(); ausführen.

* Sie können Einfach - und Mehrfachvererbung erläutern und können diese im Klassendiagramm darstellen.

	* Vererbung
            
            Wie bereits bekannt, erben Unterklassen Methoden und Variabeln von 
            der Oberklasse und werden mit extends deklariert.
            Java erlaubt jedoch keine Mehrfachvererbung von Klassen (heisst eine
            Klasse erbt von mehrern überklassen). Jedoch erlaubt Java die 
            Mehrfachvererbung von Interfaces, welche mit implements in die Klasse
            integriert werden. (siehe OOP3)

                    public interface Drawable3
                    {
                        void draw();
                        void resize(int value);
                    }
                    public class House implements Drawable3
                    {
                        // instance variables
                        public House() {...}
                        public void draw() {...}
                        public void resize(int value){...}
                        // 
                    }
       
	
* Sie kennen Kriterien des modularen Entwurfs.

    * 

* Sie kennen die Prinzipien des modularen Entwurfs.

    * 

