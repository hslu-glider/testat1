# Datenstrukturen - methods
* Sie können einen AVL Baum definieren. 

	 Ein AVL - Baum ist dann gegeben wenn Die Teilbäume des Suchbaumesausgehend von jedem knoten nicht weiter auseinander sind als 1.
	 Der Balancefaktor beschreibt die umstände im jeweiligen knoten mittels bal(v)= Höhhe rechten Teilbaum von v - Höhhe linker Teilbaum von v.
	 

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

	1. Bestimmte Programmausführung und bestimmtes Objekt -> immer derselbe Rückgabewert.
	2. Zwei gleiche Objekte im Sinne von equals() -> dieselben Rückgabewerte
	3. Zwie ungleiche Objekte im sinne von equals() -> nicht zwingend verschiene Rückgabewerte (idealerweise jedoch schon)
	
* Sie können die Methode hashCode() für einfache Fälle implementieren.

	Um Hascode zu verwenden muss equals() auf Identität überprüfen. hashCode() muss hingegen so programmiert sein, dass sie die Adresse des Objekts als rückgabewert liefert.
	
			public int hashCode()
			{
				return text.hashCode(); // hashCode() von String wird aufgerufen
			}						// (siehe auch nächste Seite)
			
			public String toString()
			{
				return text;
			}
			public static void main(String[] args)
			{
				Balloon b1 = new Balloon("Hochschule Luzern");
				Balloon b2 = new Balloon("Hochschule Luzern");
				Balloon b3 = new Balloon("Modul Programmieren 2");
				...
				Set<Balloon> set = new HashSet<Balloon> (); // Ballone in HashSet einf.
				set.add(b1);
				set.add(b2);
				set.add(b3);
				set.add(b1);
				for(Balloon b : set){
					System.out.println(b);
				}
			}	
	
* Sie können den Collection - Begriff erläutern und mindestens zwei Vorteile nennen, die der Einsatz des Java Collections Frameworks mit sich bringt. 

	Eince Collection, auch Container genannt, ist ein Objekt das viele Elemente aufnehemn kann, wie z.B. ArrayList, HahsSet oder OriorityQueue.
	Diese Objekte haben meist einen sehr geringen programieraufwand, sind schnell und gut, fördent die Weiderverwendung im Code und vereinfacht die Zusammenarbeit zwischen den Datenstrukturen.	

* Sie kennen die Klassenstruktur der Java Collection Interfaces und können diese nutzen. 

		int size();
		boolean isEmpty();
		boolean contains(Objecto);
		Iterator<E> iterator();
		Object[] toArray();
		<T> T[] toArray(T[] a);
		boolean add(E o);
		boolean remove(Object o);
		boolean containsAll(Collection<?> c);
		boolean addAll(Collection<? extends E> c);
		boolean removeAll(Collection <?> c);
		boolean retainAll(Collection <?> c);
		void clear();
		boolean equals(Object o);
		int hashCode();

* Sie kennen die verschiedenen Collection Views auf eine Map. 

		Set<K> keySet();
		Collection<V> values();
		Set<Map.Entry<K,V>>	entrySet();

* Sie können für ein gegebenes Problem die geeignete Collection - Klasse auswählen 

	* HashMap für nicht geordnete objekte mit Schlüssel
	* HashSet für nicht geordnete objekte ohne duplikate
	* TreeMap für intern geordnete objekte mit Schlüssel
	* TreeSet für intern geordnete objekte ohne Schlüssel	
	* Arraylist für Objekte ohne Schlüssel die nicht intern geordnet sind und nicht oft geändert werden.
	* Arraylist für Objekte ohne Schlüssel die nicht intern geordnet sind und nicht geändert werden.
	
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