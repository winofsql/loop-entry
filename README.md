# loop-entry
## Java
```java
String[] a = {"AB-", "CD-", "EF\n"};

for( int i = 0; i < a.length; i++ ) {
    System.out.print(a[i]);
}
for( String value: a ) {
    System.out.print(value);
}
Arrays.asList(a).forEach(
    (value) -> {
            System.out.print(value); 
    }
);                
```
## C#
```cs
string[] a = {"AB-", "CD-", "EF\n"};

for( int i = 0; i < a.Length; i++ ) {
    Console.Write(a[i]);
}
foreach (string value in a) {
    Console.Write($"{value}");
}
```
## PHP
```php
$a = ["AB-", "CD-", "EF\n"];

for( $i = 0; $i < count($a); $i++ ) {
    print "{$a[$i]}";
}
foreach ( $a as $value  ) {
    print "{$value}";
}
```
## JavaScript
```javascript
var a = ["AB", "CD", "EF"];

for( i = 0; i < a.length; i++  ) {
    console.log( a[i] );
}
for( value of a ) {
    console.log( value );
}
for( value in a ) {
    console.log( value );
}
```
![image](https://user-images.githubusercontent.com/1501327/132113676-c3b054be-115f-42ef-af2e-b7d2032a3904.png)
