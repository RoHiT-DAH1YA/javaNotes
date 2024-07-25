* They are blue-prints for class
* Interface contains only abstract methods

## example
* Suppose a company provides its devs a computer that can either be laptop or desktop
```java
interface Machine {  
    void run();  
}  
class Laptop implements Machine{  
    public void run() {  
        System.out.println("Runnign in laptop");  
    }  
}  
class Desktop implements Machine{  
    @Override  
    public void run() {  
        System.out.println("Running in Desktop but faster");  
    }  
}  
public class LearningInterfaces {  
    public static void main(String[] args) {  
        Machine obj = new Desktop();  
        Machine obj2 = new Laptop();  
        obj.run();  
        obj2.run();  
    }  
}
```

## Important Points
* all methods must be abstract
* by default every method is public abstract in interface
* All variables are only and only **final and static** inside an interface

```java
// wrong
interface A {
	int age;
	String city;
}
```

```java
// correct
interface A {
	int age = 24;
	String city = "Mumbai";
}
```


* say A is parent B is child then keyword used is:
	* A-class B-class  ==  extends
	* A-interface B-class  == implements
	* A-interface B-interface  ==  extends
## Creating object
##### Way-1
```java
interface A {
	void show();
	void config();
}
class B implements A {
	public void show() {
		System.out.println("Inside B show");
	}
	public void config() {
		System.out.println("Inside B config");	
	}
}
class MainClass {
	main() {
		A obj = new B();
		obj.show();
		obj.config();
	}
}
```