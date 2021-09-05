## Map : 環境変数 : ソート : for
```java
Map<String, String> env = System.getenv();

// ****************************************
// 配列とSet
// ****************************************
String[] keys;
Set<String> set;

set = env.keySet();
keys = set.toArray(new String[0]);

// ****************************************
// ソート
// ****************************************
Arrays.sort(keys);

// ****************************************
// for
// ****************************************
for( int i = 0; i < keys.length; i++ ) {
    System.out.println( String.format( "%s => %s", keys[i], env.get( keys[i] ) ) );
}
```
