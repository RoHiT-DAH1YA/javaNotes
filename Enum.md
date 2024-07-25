# Example 
* suppose you want to send status of the http request to client
```java
enum Status {
	Running, Failed, Pending, Success;
}

public class Demo
{
	public static void main(String args[]){
		Status s = Status.Success;  
		Status sarr[] = Status.values();  
		System.out.println(s);  
		System.out.println(s.ordinal());  
		for (Status st : sarr) {  
		    System.out.println(st);  
		}
	}
}
/* OUTPUT
Success
3
Running
Failed
Pending
	Success
*/
```

* Status is a class here
* And Running, Failed, Pending and Success are named constants.
* just like int i = 10;

## Enum are classes

```java
enum Laptop {
	Macbook(90000), Asus(70000), Hp(65000);
	
	private Laptop(int price) {
		this.price = price;
	}
	
	public int setPrice(int price) {
		this.price = price;
	}
	
	public int getPrice() {
		return price;
	}
}

public class Demo
{
	public static void main(String args[]){
		Laptop lapi = Laptop.Macbook;
		System.out.println(lapi.price);
	}
}
/* OUTPUT
90000
*/
```