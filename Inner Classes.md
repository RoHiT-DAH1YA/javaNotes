# What?
* Classes inside other classes
```java
class A{
	int age;
	public void showAge() {
		System.out.println("Age: " + age);
	}

	Class B() {
		pubic void config() {
			System.out.println("in Config.")
		}
	}
}
```

# Creating object of inner class
```java
class A{
	class B {}
}

public class MainClass {
	pubilc static void main(String args[]) {
		A obj = new A();
		B obj2 = new obj.B();
	}
}
```

# Static inner class
```java
class A{
	static class B {}
}

public class MainClass {
	pubilc static void main(String args[]) {
		A obj = new A();
		B obj2 = new A.B();
	}
}
```
> We cannot have static class by itself. Static classes must be inner classes

# Anonymous Inner class

* suppose you want to create an object but with only one method needs a new implementation for just one particular instance of that class
* **Way-1** of doing it is to create a child class with new implementation
```java
class A {
	public void show() {
		System.out.println("In A show");
	}
}
class B extends A {
	public void show() {
		System.out.println("Something new");
	}
}
public class MainClass {
	pubilc static void main(String args[]) {
		A obj = new B();
		obj.show();
	}
}
```
* **Way-2** is to use anonymous inner class
```java
class A {
	public void show() {
		System.out.println("In A show");
	}
}
public class MainClass {
	public static void main(String args[]) {
		A obj = new A()
		{
			public void show() {
				System.out.println("Something new");
			}
		};
		obj.show();
	}
}
```

#### Q- to which class the inner class is made in prev code?
Ans - the obj is an instance of some inner class of MainClass and not of A. We can observe it by compiling it and checking the name of class files
```
MainClass.class
MainClass$1.class
```

# Abstract Anonymous inner class

```java
abstract class A {
	abstract public void show();
}
public class MainClass {
	public static void main(String args[]) {
		A obj = new A()
		{
			public void show() {
				System.out.println("Something new");
			}
		};
		obj.show();
	}
}
```