### SingleObject.java

```java
public class SingleObject{
    private static SingleObject instance = new SingleObject(); //early instantiation

    private SingleObject(){

    }
    public static SingleObject getInstance(){
        return instance;
    }
    public void showMessage(){
        System.out.println("The objcet is : " + instance);
     }

}
```
### SingletonObject.java

```java
public class SingletonObject{
    private static SingletonObject instance ;

    private SingletonObject(){

    }
    public static SingletonObject getInstance(){
        if(instance == null){
            synchronized(SingletonObject.class){
                if(instance == null){
                    instance = new SingletonObject(); //lazy Instantiation of Singleton Pattern
                }
            }
        }
        return instance;
    }
    public void showMessage(){
        System.out.println("The object is : " + instance);
     }

}
```

### SingletonObjectDemo.java

```java
public class SingletonObjectDemo {
    public static void main(String[] args) {
 
       
       SingletonObject object = SingletonObject.getInstance();
 
       //show the message
       object.showMessage();
    }
 }
```

### SingletonPatternDemo.java

```java
public class SingletonPatternDemo {
    public static void main(String[] args) {
 
       //Get the only object available
       SingleObject object = SingleObject.getInstance();
 
       //show the message
       object.showMessage();
    }
 }
```
