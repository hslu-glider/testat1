# Aufgabe 1

## a)
```java
public class StackFullException extends Exception
{
	public StackFullException(String s) 
	{
		super("Stack full " + s);
	}
}


public class StackEmptyException extends Exception
{
	public StackEmptyException(String s) 
	{
		super("Stack empty " + s);
	}
}
```

## b)
```java
public Stack(int size) throws IllegalArgumentException
...
		throw new IllegalArgumentException("Illegal Argument - size: " + size);
```
## c)
```java
public void push(T o) throws StackFullException{
	...
	else {
		throw new StackFullException(stack.length + " items");
	}
}
```

## d)

```java
try{
	s.push(7);
} catch (StackFullException e){
	e.printStackTrace();
}
```

# Aufgabe 2

## a)

```java
new File(fileName);
if(aFile.exists()){
	try{
		FileInputStream aFileInputStream = new FileInputStream(aFile);
		...
		for(...){
			System.out.println(aDataInputStream.readInt());
		}
	} catch (IOException e) {
		...
	}
	
}
```

# Aufgabe 3

## a)

```java
public int compareTo(SailingShip other){
	if(this == other) return 0;
	return (shipName.compareTo(other.shipName));
}
```

## b)

```java
public class BRTComperator implements Comparator<CargoShip> {
	public int compare (CargoShip s1, CargoShip s2){
		return (s1.getRegisterTin()-s2.getRegisterTon());
	}
	
	public boolean equals(Object o){
		/* Implementierung der equals-Methode
		1. Null
		2. Identität
		3. Klassengleichheit
		4. Wertevergleich
		*/
	}

}
```

# Aufgabe 4

| Beschreibung | Zeile |
|--------------|-------|
| Ein Thread wird erzeugt | 58 |
|  | 59 |
|  | run Methode |
|  | 42 |
|  | 11, (40) |
|  | 14 |
|  | nicht möglich (beachte Lebenszyklus) |
|  | 21 (61 löst aus) |
|  | nicht möglich |
|  | 47 |

# Aufgabe 5

## a)

den der Klasse Person

## b) 

den des Objekts uniqueID

## c)

den des aktuellen Objekts (this)

## d) 

niemand (Syntaxfehler - nur Objekte können locks stellen)


# Aufgabe 6

```java
...
	private Thread thread;
	
	public void start() {
		if(thread == null){
			thread = new Thread(this);
			thread.start();
		}
	}
```

Tipp: Wie erzeugt man Threads

  * implements Runnable
    * Untervariante 1
    * Untervariante 2
  * extends Thread

# Aufgabe 7

## a) 

Drei Varianten:
  * normale benannte äussere Klasse
  * benannte innere Klasse
  * anonyme innere Klasse

Die vorliegende Variante ist die anonyme innere Klasse auf Zeile 31-36

Das Event heisst ChangeEvent

## b)

Zeile 43

## c)

Zeile 42

## d)

Zeile 25 

## e)

BorderLayout

# Aufgabe 8

## a)

bedient einen Client nach dem anderen

Der TimeServer ist blockierend, d.h. er kann nur einen Client nach dem 
anderen bedienen. Weitere Clients können zwar Kontekt aufnehmen, erhalten 
aber kein Datum und keine Zeit.

## b)

Zeile 12-18 als Thread ausführen

## c)

Die genaue Port-Nummer ist egal, sollte aber grösser als 1023 sein


## d)

Grösse der Warteschlange (backlog) für anstehende Clients wird definiert

## e)

Der Port ist bereits durch einen anderen Server belegt

## f)

telnet localhost port

## g)

Nichts (nach dem Verbindungsaufabau erhält man sofort den Datum+Zeit String)

## h)

Nur als localhost

## i)

```java
new Socket(host, port);
```

# Aufgabe 9

  * 2
  * 4
  * 1
  * 6
  * 3
  * 5













































