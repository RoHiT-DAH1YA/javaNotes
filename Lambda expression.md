* whenever you have an interface with only one function we call it functionInterface.
* to make an object of such an interface we need to make a call or anonymous class. 
* Java 8 introduced lambda expression for only such cases to reduce the amount of code to be written

* Lambda Expression works only with Functional Interfaces
#### Example
```java
interface SomeClass {  
    void show();  
}  
public class LearningLambda {  
    public static void main(String[] args) {  
        SomeClass obj = new SomeClass() {  
            @Override  
            public void show() {  
                System.out.println("Inside show of Some Class.");  
            }  
        };  
        obj.show();  
    }  
}
```
#### With Lambda Expression
```java
@FunctionalInterface  
interface SomeClass {  
    void show();  
}  
public class LearningLambda {  
    public static void main(String[] args) {  
        SomeClass obj = () -> {  
                System.out.println("Inside show of Some Class.");  
        };  
        obj.show();  
    }  
}
```

#### without using block
```java
@FunctionalInterface  
interface SomeClass {  
    void show();  
}  
public class LearningLambda {  
    public static void main(String[] args) {  
        SomeClass obj = () -> System.out.println("Inside show of Some Class.");
        obj.show();  
    }  
}
```

## Example-2 return statement

	```java
@FunctionalInterface  
interface SomeClass {  
    int add(int i, int j);  
}  
public class LearningLambda {  
    public static void main(String[] args) {  
        SomeClass obj =(i, j) -> i+j;  
        System.out.println(obj.add(5, 6));  // 11
    }  
}
```