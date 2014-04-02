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

				* Sie k�nnen Einfach - und Mehrfachvererbung erl�utern und k�nnen diese im Klassendiagramm darstellen.

* Sie kennen Kriterien des modularen Entwurfs.
* Sie kennen die Prinzipien des modularen Entwurfs.
