# Java
* Sie wissen, wie toString() arbeitet und angepasst werden kann.
		public String toString()

		Returns a string representation of the object. 
		In general, the toString method returns a string that "textually represents" this object. 
		The result should be a concise but informative representation that is easy for a person to read. 
		It is recommended that all subclasses override this method.

		The toString method for class Object returns a string consisting of the name of the class of which the object is an instance, 
		the at-sign character `@', and the unsigned hexadecimal representation of the hash code of the object. 
		In other words, this method returns a string equal to the value of:

		getClass().getName() + '@' + Integer.toHexString(hashCode())
     
		Returns:
		a string representation of the object.
		
	* Gibt wie oben zu sehen den Namen der Klasse welche aus der \@ Speicheradresse im Heap zusammengestellt wird.
    * Kann überschrieben werden. Bsp:
		@override 
		public String toString(){
			return "z.B Name des Objektes hier angeben";
		}

* Sie verstehen das Konzept von abstrakten Klassen und abstrakten Methoden und können diese einsetzen.

	* Abstrakte Methoden haben "abstract" im Methodenkopf
	* Abstrakte Methoden haben keinen Methodenrumpf (body).
	* Abstrakte Methoden machen auch die Klasse abstrakt.
	* Beispiel einer abstrakten Methode:
		public abstract void doSomething(int someIntegerParameter);
    * Von abstrakten Klassen können keine Objekte instanziert werden.
    * Die Implementation wird in konkreten Unterklassen realisiert.
    * Unterklassen können durch Überschreiben (@override) der abstrakten Methoden konkret (instanziierbar) werden.
	* Es gibt abstrakte Klassen die keine abstrakten Methoden enthalten.
	* Beispiel einer abstrakten Klasse:
		public abstract class Item
		{
			public Item(String theTitel)
			{...}
			public void setComment(String comment)
			{...}
			public String getComment()
			{...}
		}

* Sie kennen Java spezifische Eigenschaften der Vererbung.

    * Keine Mehrfachvererbung von Klassen (abhilfe mit dem Konstrukt der Interfaces)

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
