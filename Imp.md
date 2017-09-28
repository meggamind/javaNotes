

- ***Declaring a map***
```java
Map<Character, Integer> map = new HashMap<>();
```

-  ***Iterating through Map***
```java
public static void printMap(Map mp) {
    Iterator it = mp.entrySet().iterator();
    while (it.hasNext()) {
        Map.Entry pair = (Map.Entry)it.next();
        System.out.println(pair.getKey() + " = " + pair.getValue());
        it.remove(); // avoids a ConcurrentModificationException
    }
}
```

- ***Declaring a PriorityQueue***
```java
PriorityQueue<String> pQueue = new PriorityQueue<String>();
```
- ***Custom Comparator***
```java
class Checker implements Comparator<String>{
    public int compare(String str1, String str2){
        return str1.length() < str2.length() ? -1: 1;
    }
}

PriorityQueue<String> queue = new PriorityQueue<String>(5, new Checker());
```
- 
```java
int compareTo(Object 0)
int compareToIgnoreCase()
```
- ***[.equals() vs .compareTo() vs .compare()](https://www.leepoint.net/data/expressions/22compareobjects.html)***
```java
Comparator defined in java.util pacakge -> public int compare(Object1, Object2)
Comparable defined in java.lang package -> public int comapreTo(Object o)
```
- ***[.compareTo() vs .compare()](http://javarevisited.blogspot.com/2011/06/comparator-and-comparable-in-java.html)***
- ***[How to override compareTo method in Java](http://javarevisited.blogspot.sg/2011/11/how-to-override-compareto-method-in.html)***
- ***Sort ArrayList of custom Objects by property***
```java
public class CustomComparator implements Comparator<MyObject>{
    @Override
    public int compare(MyObject o1, Myobject o2){
        return 01.getStartDate().compareTo(o2.getStartDate());
    }
}
Collections.sort(Database.arrayList, new CustomComparator());

// As an inline Anonymous class:
Collections.sort(Database.entryList, new Comparator<MyObject>{
    @Override
    public int compare(MyObject o1, MyObject o2){
        return 01.getStartDate().compareTo(o2.getStartDate());
    }
});
```
