# Java
* Sie wissen, wie toString() arbeitet und angepasst werden kann.
		
		public String toString()

		Returns a string representation of the object. 
		In general, the toString method returns a string that "textually represents" this object. 
		The result should be a concise but informative representation that is easy for a person to read. 
		It is recommended that all subclasses override this method.

		The toString method for class Object returns a string consisting of the name of the class 
		of which the object is an instance, the at-sign character `@', 
		and the unsigned hexadecimal representation of the hash code of the object. 
		In other words, this method returns a string equal to the value of:

		getClass().getName() + '@' + Integer.toHexString(hashCode())
     
		Returns:
		a string representation of the object.
		
	* Gibt wie oben zu sehen den Namen der Klasse welche aus der \@ Speicheradresse im Heap zusammengestellt wird.
    * Kann überschrieben werden. Bsp:
		
			@override 
			public String toString()
			{
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

    * Programme werden oft verwendet, um reale Systeme zu simulieren
	* Simulationen betreffen oft nur einen Teil des realen Systems
	* Simulationen enthalten Vereinfachungen
		* Grössere Detailtreue kann genauere Resultate liefern.
		* Grössere Detailtreue verlangt nach mehr Ressourcen.
	* Validierung durch Messungen notwendig
	* Anwendungsbereiche:
		* Vorhersagen (Wetterprognosen, Funktionsnachweise etc.)
		* Experimente ("Unmögliche" und gefährliche Experimente werden möglich)
		

* Sie können ein Java Interface definieren.

        public interface Drawable()
		{
			//alle Felder eines Interfaces sind public static final (also Konstanten, Schlüsselwörter können entfallen)
			
			//Keine Konstruktoren erlaubt
			
			void draw(); //Einträge sind autom. public abstract (die entsprechenden Schlüsselwörter können entfallen)
			void resize(int value);
		}

* Sie können ein Java Interface in abgeleiteten Klassen implementieren.
        
		public class House implements Drawable
		{
			//instance variables
			
			public House(){...}
			public void draw() {...}
			public void resize(int value){...}
			
			//other methods
		}

* Sie kennen Unterschiede zwischen konkreten und abstrakten Klassen sowie zwischen abstrakten Klassen und Interfaces.

	* Von abstrakten Klassen können im gegensatz zu konkreten Klassen keine Objekte instanziiert werden.
	* Abstrakte Klassen können Implementationen enthalten, Interfaces nicht.
	* Interfaces können ebenfalls nicht instanziiert werden. 
	
* Sie wissen, wie Sie in Java Mehrfachvererbung umsetzen können

	* Java erlaubt keine Mehrfachvererbung von Klassen
	* Interfaces jedoch beherrschen das Konzept von Mehrfachvererbung
	* Beispiel zu Erben von einer Klasse und Implementierung eines Interfaces:
	
			public class MyClass extends BaseClass implements MyInterface {...}
			
	* Beispiel zur Implementierung von mehreren Interfaces:
	
			public class MyClass2 implements MyInterface, MyInterface2 {...}
			
	* Beispiel zu Erben von einer Klasse und Implementierung mehrerer Interfaces:
	
			public class MyClass3 extends BaseClass implements MyInterface, MyInterface2 {...}
			
* Sie wissen, wozu man Interfaces verwendet.

	* Ein Interface spezifiert ein Verhalten (Menge von Methodenköpfen) ohne Implementation zu beinhalten (nur das WAS)
	* Ein Interface beinhaltet keinen Konstruktor und kann daher auch nicht instanziiert werden
	
* Sie verstehen das Konzept der inneren Klassen und können dieses für die Implementierung ereignisgesteuerter Java - Applikationen einsetzen. 

	* innere Klasse: Die Klasse wird in eine andere Klasse hinein genommen.
	* Beispiel für die Implementation einer inneren Klasse mit Ereignissteuerung:
	
			public class InnerClassDemo extends JFrame
			{
				private JButton button1; //Instanzvariable button1 vom Typ JButton
				
				public InnerClassDemo() //Konstruktor
				{
					button1 = new JButton("Drück mich"); //Initialisierung des Buttons
					button1.addActionListener( new MyActionListener() ); //Hinzufügen des ActionListeners mit Aufruf der inneren Klasse
					add(button1); //Hinzufügen des Buttons zum JFrame
				}
				
				//Hier nun die eigentliche Implementierung der Inneren-Klasse MyActionListener
				private class MyActionListener implements ActionListener
				{
					public void actionPerformed(ActionEvent e)
					{
						button1.setText("Ich wurde gedrückt");
					}
				}
			}
			
	* anonyme innere Klasse: Ein namenloses Objekt einer namenlosen Klasse wird direkt beim Anmelden des Listeners erzeugt
		* vereinfachte Variante der inneren Klasse
		* bei langen Ereignis-Handlern unübersichtlich
	* Beispiel für die Implementation einer anonymen inneren Klasse mit Ereignissteuerung
	
			public class AnonymousClassDemo extends JFrame
			{
				public AnonymousClassDemo()
				{
					JButton button1 = new JButton("Drück mich");
					button1.addActionListener(
						//Die anonyme Innere-Klasse wird hier implementiert
						new ActionListener()
						{
							public void actionPerformed(ActionEvent e)
							{
								button1.setText("Ich wurde gedrückt");
							}
						}
						//Ende der Implementation
					);
					add(button1);
				}
			}
			