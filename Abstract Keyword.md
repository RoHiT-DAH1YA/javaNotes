There are two thing that can be abstract
* class
* method

* an abstract method or variable can only be a part of abstract class. Normal class can't have abstract methods or variables

* You can't make object of an abstract class
* A class needs to extend abstract class and then implement all abstract methods and then an object can be made for that derived class
* If even one abstract method is left unimplemented that that derived class will also become an abstract class

```java
abstract class Computer {
	String name;
	abstract public void run();
	publiv void displayName() {
		System.out.println("Name: " + name);
	}	
}

class Laptop extends Computer {
	public void run() {
		System.out.println("Running on laptop");
	}
}
```