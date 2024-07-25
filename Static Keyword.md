* `static` keyword is used for creating variables and methods that are shared by all the objects of that class

```java
class Mobile {
	String brand;
	int price;
	static String name;
	public void show1() {
		System.out.println(brand + " : " + price + " : " + name);
	}
}
public class Demo {
	main() {
		Mobile obj1 = new Mobile();
		obj1.brand = "A";
		obj1.price = 10000;
		obj1.name = "mobile";
		
		Mobile obj2 = new Mobile();
		obj2.brand = "B";
		obj2.price = 15000;
		obj2.name = "phone";
		
		obj1.show(); // A : 10000 : phone
		obj2.show(); // B : 15000 : phone
	}
}
```

#### Note
>static variables should be accessed with class name
```java
System.out.println(obj1.name); // wrong
System.out.println(Mobile.name) // correct
```

## Static Mehtods
```java
class Mobile {
	String brand;
	int price;
	static String name;
	
	public void show() {
		System.out.println(brand + " : " + price + " : " + name);
	}
	
	public static void show1(Mobile obj) {
		System.out.println(obj.brand + " : " + obj.price + " : " + name);
	}
}

main () {
	Mobile.show1(obj1);
}
```

> you can access static variables inside static methods but to access local variables you should pass the object itself to the static method