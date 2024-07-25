	#### extends keyword

## Polymorphism
		
######         Same name Different usage
* method overloading - compile time poly
```java
class calc {
	public void add(int a, int b){ return a+b; }
	public void add(int a, int b, int c){ return a+b+c; }
}
```

* method overriding - runtime poly
```java
class A {
	public void foo() {
		System.out.println("in A foo");
	}
}
class B extends A {
	public void foo() {
		System.out.println("in B foo");
	}
}
```

## Important examples

```java

class A {  
    public A() {  
        System.out.println("In A constructor");  
    }  
    public void show() {  
        System.out.println("In A show");  
    }  
    public void show1() {  
        System.out.println("In A show-1");  
    }  
}  
class B extends A {  
    public B() {  
        System.out.println("In B constructor");  
    }  
  
    @Override  
    public void show() {  
        System.out.println("In B show");  
    }  
  
    public void show2() {  
        System.out.println("In B show-2");  
    }  
}  
```

```java
// overriding
public class LearnPolymorphism {  
    public static void main(String[] args) {  
        A obj = new A();  
        obj.show();
		
		B obj2 = new B();
		obj2.show();
    }  
}
/*
In A constructor
In A show
In A constructor
In B constructor
In B show
*/
```

```java
public class LearnPolymorphism {  
    public static void main(String[] args) {  
        A obj = new B();  
        obj.show();
    }  
}
/*
In A constructor
In B constructor
In B show
*/
```

```java
public class LearnPolymorphism {  
    public static void main(String[] args) {  
	    // upcasting
        A obj = new B(); // EQUIVALENT TO: A obj = (A) new B();
        obj.show();  
		
        obj.show1();
        // obj.show(); // will give error
        System.out.println("obj: " + obj);
	    
	    // down casting
        B obj1 = (B) obj;  
        System.out.println(obj + "  " + obj1);  
        obj1.show2();  
    }  
}
/*
In A constructor
In B constructor
In B show
In A show-1
obj: telusko.B@2a84aee7
telusko.B@2a84aee7  telusko.B@2a84aee7
In B show-2
*/
```
