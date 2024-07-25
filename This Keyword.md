
```java
class Student {
	int age;
	
	public void setAge(int age, Student stu) {
		Student st = stu;
		st.age = age;
	}
}
main() {
	Student s = new Student;
	s.setAge(20, s);
}
```

These two codes are equivalent

```java
class Student {
	int age;
	
	public void setAge(int age, Student stu) {
		this.age = age;
	}
}
main() {
	Student s = new Student;
	s.setAge(20);
}
```