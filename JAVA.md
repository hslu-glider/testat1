# Java
* Sie wissen, wie toString() arbeitet und angepasst werden kann.
		public String toString()

		Returns a string representation of the object. In general, the toString method returns a string that "textually represents" this object. The result should be a concise but informative representation that is easy for a person to read. It is recommended that all subclasses override this method.

		The toString method for class Object returns a string consisting of the name of the class of which the object is an instance, the at-sign character `@', and the unsigned hexadecimal representation of the hash code of the object. In other words, this method returns a string equal to the value of:

		getClass().getName() + '@' + Integer.toHexString(hashCode())
     

Returns:
    a string representation of the object.
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
