* use double quotes

```java
String name = "Rohit";
/// it is equivalent to 
String name = new String("Rohit");
System.out.println(name); // $Rohit
System.out.println(name.hashCode()); // $79138838 // address 
System.out.println("Hello" + name); // concatenation
```

* as type has first letter capital it is a `class`
* there are 2 types of strings in java
	1. String
	2. StringBuffer 
	3. StringBuilder
# BTS
* whenever you create a string it gets stored in `String Constant pool`
```java
String fname = "Rohit";
String lname = " Kumar";
String name = "Rohit Kumar";
String name2 = fname + lname;

sout(fname.hashCode());
sout(lname.hashCode());
sout(name.hashCode());
sout(name2.hashCode());

/* output - Immutable
79138838
72857492
-1484295414
-1484295414
*/
```
* observe that `name` and `name2` has same address, this means name and name2 points to same object in the memory. 
* whenever a string is to be refered with same value it is referred to same object. 
* There will be no 2 object of String with same value
# StringBuilder
```java
StringBuffer sb = new StringBuffer("Rohit");
```
* it creates a <b> MUTABLE </b> string
* for string buffer objects allocated size is dataSize + 16B by default in order to minimise the need of reallocation of string by having extra space for expanding.
* it is <b> Thread Safe </b> 
```java
StringBuffer sb1 = new StringBuffer();
StringBuffer sb2 = new StringBuffer("Rohit");
sb1.capacity(); // 16
sb2.capacity(); // 21
sb2.length(); // 5
```
there are many methods that can be applied on StringBuffer
```java
StringBuffer sb = new StringBuffer("Mighty");
sb.insert(6, "Java ");   /// MightyJava
sb.ensureCapacity(30);   // minimum size allocated will be 30B
```

# StringBuilder
* it's NOT **Thread Safe** 