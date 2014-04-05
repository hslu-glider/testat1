# Datenstrukturen - methods
* Sie können einen AVL Baum definieren. 
* Sie kennen 3 verschiedene Betrachtungsweisen für Gleichheit und können je ein konkretes Beispiel dazu erläutern. 
	
	* Gleiche Werte
	
	 Farben -> gleicher RGB-Wert
	 Zahl -> gleiche Zahlenwerte
	
	* Gleiche Identität (Name)
	
	 Studierende -> evt studierende mit dem Gleichen Namen	 
	
	* Gleiche Klasse
	
	 Studium -> wir sind alle von der Klasse HSLU T&A PRG 2 FS 14
	
* Sie können die Wichtigkeit von equals() begründen. 
	
	Mit der Mehtode equals() kann man feststellen ob Objekte die gleiche Idendität. die Werte müssen hier nicht übereinstimmen.
	Jedoch lässt sich die Methode equals() für spzielle Anwendungen umschreiben.

* Sie können equals() gemäss 4 - Schritt - Schema adäquat implementieren.

	* Test auf Identität 
	* Test auf null
	* Test auf Typen-Vergleichbarkeit
	* Vergleich aller relevanter Felder:
		* Gewöhnliche Variablen: Vergleich mit ==
		* Referenzvariablen: Vergleich wiederumg mit equals()
 
* Sie können die Vorteile einer Hashtabelle benennen. 

	* Die Hashtabelle ist eine Vernünftig implementierte Hashfunktion mit sehr effizienter Datenstruktur
		* Einfügen O(1)
		* Suchen O(1)
		* Entfernen O(1)
		* Keine Nachfolger oder Vorgänger bezüglich der Ordnung
		* Nicht sortiert 
		
* Sie können die 3 Punkte des hashCode() - Contractes erläutern 
* Sie können die Methode hashCode() für einfache Fälle implementieren.
* Sie können den Collection - Begriff erläutern und mindestens zwei Vorteile nennen, die der Einsatz des Java Collections Frameworks mit sich bringt. 
* Sie kennen die Klassenstruktur der Java Collection Interfaces und können diese nutzen. 
* Sie kennen die verschiedenen Collection Views auf eine Map. 
* Sie können für ein gegebenes Problem die geeignete Collection - Klasse auswählen 

* Zusätzliches:
		* equals()
	
	* Comparable & comareTo()
	
	 Bei Comparable handet es sich um ein Interface mit der Methode compareTo(). Durch dieses Lässt sich für Objekte einer Klasse eine natürliche Ordnung festlegen.
	 CompareTo() vergleicht dabei die Namen von "this Object" mit einem "other object" und gibt Ausgaben nach dem folgende Schema;
	 
	 this "less than" other -> Negativer int Wert
	 
	 this "equal to" other -> 0

	 this "greater than" other -> positiver int Wert
	
	* Comparator
	 
	 Mit Hillfe des Interfaces Comparator<T> lassen sich beliebig viele spezielle Ordnungen festlegen. 
	 Das Interface kennt 2 Methoden. Zum einen "int compare(T o1, T o2)" welche 2 argumente oder objektvariabeln auf ihre anordnung überprüft und boolean equals()
	 welche überprüft ob 2 Objekte Identisch sind.
	 
		* compare() & equals()
		 
				import java.util.Comparator;
				
				public class SizeUpComparator implements Comparator<Balloon>
				{
					public int compare(Balloon o1, Balloon o2)
					{
					return(o1.getSize() - o2.getSize());
					}
					@Override
					public boolean equals(Object obj)
					{
						if(obj == null){
						return false;
						}
						return(this.getClass() == obj.getClass());
					}
				}