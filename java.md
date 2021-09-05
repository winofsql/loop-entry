## Map( 環境変数 ) : 配列 : ソート : for
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

## Map( 環境変数 ) : ソート : iterator : while
```java
Map<String, String> env = System.getenv();

// ****************************************
// ソート
// ****************************************
TreeMap<String, String> tm = new TreeMap<String, String>( env );

Iterator<String> iterator = tm.keySet().iterator();

// ****************************************
// while
// ****************************************
String key;
while ( iterator.hasNext() ) {
    key = iterator.next();
    System.out.println( String.format( "%s => %s", key, env.get( key ) ) );
}        
```
