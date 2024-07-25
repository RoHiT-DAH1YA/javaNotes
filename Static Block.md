* First read Static Keyword
### What it is??
* there are two steps to create an object
	1. load a class
	2. create an object
* loading of class happens once for each class
* to run some code while loading a class we can use static block
```java
class Mobile {
	String brand;
	int price;
	static String name;
	
	static { // it runs whenever a class loads
		name = "phone";
		System.out.println("we are in static");
	}
	
	public Mobile() {
		System.out.println("We are in constructor");
	}
	public void show1() {
		System.out.println(brand + " : " + price + " : " + name);
	}
}
```

* Class will load only when the first object is needed to be created.
* we can load a class force fully by a following method of class `class`.
```java
main () {
	Class.forName("Mobile"); // loads the class forcefully
}
```

