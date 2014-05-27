# Aufgabe 1

## a)

## b)
```java
public Stack(int size) throw IllegalArgumentException
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
} catch (StackFullException){
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
  

































