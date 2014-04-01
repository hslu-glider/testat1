# Objektorientierte Programmierung
* Sie können mindestens 3 Vorteile der Vererbung erklären

    * Einfache Wiederverwendung (von Implementation)
    * Vermeidung von Code-Duplikation
    * Einfachere Wartbarkeit
    * Einfachere Erweiterbarkeit

* Sie können einen schwergewichtigen Nachteil der Vererbung erläutern

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
        Dynamische Datentypen werden werden bei der Ausf�hrung definiert, also zur Laufzeit.

                ...
                k = new Konto();
                k = new Spare();
                k = new Giro();
                ...

* Sie können bestimmen, welche Implementation für einen bestimmten Methodenaufruf zur Ausführung gelangt.
* Sie können Polymorphie, d.h. Überladen und Überschreiben mittels Java - Code erklären und anwenden.
* Sie können Einfach - und Mehrfachvererbung erläutern und können diese im Klassendiagramm darstellen.
* Sie kennen Kriterien des modularen Entwurfs.
* Sie kennen die Prinzipien des modularen Entwurfs.
