# Objektorientierte Programmierung
* Sie k�nnen mindestens 3 Vorteile der Vererbung erkl�ren

    * Einfache Wiederverwendung (von Implementation)
    * Vermeidung von Code-Duplikation
    * Einfachere Wartbarkeit
    * Einfachere Erweiterbarkeit

* Sie k�nnen einen schwergewichtigen Nachteil der Vererbung erläutern

    * Starke Kopplung

* Sie k�nnen Substitution und Casting korrekt anwenden.

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
            

* Sie k�nnen zwischen statischen und dynamischen Typen unterscheiden.
    * Statische Typen
    
		Statische Datentype werden bei der Kompilierung und nicht zur Laufzeit festgelegt.
                
				Konto k;

    * Dynamische Typen
    
		Dynamische Datentypen werden werden bei der Ausf�hrung definiert, also zur Laufzeit.

                ...
				k = new Konto();
				k = new Spare();
				k = new Giro();
                ...

* Sie k�nnen bestimmen, welche Implementation f�r einen bestimmten Methodenaufruf zur Ausf�hrung gelangt.
	
    * Stichwort �berladung von Konstruktoren und Methoden.
        
        Es gilt, sobald ein Konstruktor oder Methodenkopf auf dei Eingabe passt
        wird er ausgef�hrt. Dabei werden zuerst die Unterklassen durchsucht und 
        danach in aufsteigender Reihenfolge die �bergeordneten Klassen.
        Siehe Beispiele "�berschreibung" im darauffolgenden Block.
        

* Sie k�nnen Polymorphie, d.h. �berladen und �berschreiben mittels Java - Code erkl�ren und anwenden.
	
	* �berladung
		
		�berladene Funktionen oder Konstruktoren erkennt man, dass sie den selben Namen haben, jedoch 
		unterschiedliche Parameter in bezug auf Anzahl, Art und Reihenfolge. (schwache Polymorphie)
				
				...
				public void print(){
				}
				...
				public void print(int space){
				}
				...
				
	* �berschreiben
		
		In abgeleiteten Klassen k�nnen Methoden der Oberklasse bei Bedarf ver�ndert (�berschrieben) werden.
		Welche Methode verwendet wird h�ngt von der Klasse selbst ab.
		
				Konto konto2 = new Konto();
				konto2.print(); // Es wird die print Methode von Konto ausgef�hrt.  
				
				Giro giro2 = new giro();
				giro2.print(); // Es wird die print Methode von Giro ausgef�hrt. 
		
				konto2 = giro2;
				konto2.print(); // konto2 ist jetzt ein Giro konto und kennt die print funktion von Giro.
				//die suche nach der Methode Giro startet bei der untersten abgeleiteten Kalsse und endet,
				//sobald die erste methode mit diesem Namen und paramtern gefunden wurde.
				//�berschreibende Methoden k�nnen das ausf�hren von �berschriebenen methoden mit dem Befehl:
				//super.methodenname(); ausf�hren.

* Sie k�nnen Einfach - und Mehrfachvererbung erl�utern und k�nnen diese im Klassendiagramm darstellen.

	* Vererbung
            
            Wie bereits bekannt, erben Unterklassen Methoden und Variabeln von 
            der Oberklasse und werden mit extends deklariert.
            Java erlaubt jedoch keine Mehrfachvererbung von Klassen (heisst eine
            Klasse erbt von mehrern �berklassen). Jedoch erlaubt Java die 
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

