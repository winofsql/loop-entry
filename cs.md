## IDictionary( 環境変数 ) : 配列 : ソート : for
```cs
IDictionary env = Environment.GetEnvironmentVariables();

// ****************************************
// 配列とICollection
// ****************************************
ICollection col;

col = env.Keys;
string[] keys = new string[col.Count];

col.CopyTo(keys, 0);

// ****************************************
// ソート
// ****************************************
Array.Sort(keys);

// ****************************************
// for
// ****************************************
for( int i = 0; i < keys.Length; i++ ) {
    Console.WriteLine($"{keys[i]} => {env[keys[i]]}");
}        
```
## IDictionary( 環境変数 ) : ソート( SortedDictionary<string, string> ) : foreach
```cs
// ****************************************
// Collections
// ****************************************
IDictionary env = Environment.GetEnvironmentVariables();

// ****************************************
// Collections.Generic
// ****************************************
SortedDictionary<string, string> sd = new SortedDictionary<string, string>();

// ****************************************
// SortedDictionary に追加
// ****************************************
foreach (string key in env.Keys) {
    sd.Add(key, env[key].ToString());
}
// ****************************************
// SortedDictionary から表示
// ****************************************
foreach (string key in sd.Keys) {
    Console.WriteLine($"{key} => {sd[key]}");
}
```

## IDictionary( 環境変数 ) : ループ( IEnumerator ) : while
```cs
IDictionary env = Environment.GetEnvironmentVariables();

IEnumerable iemu = env;
IEnumerator iemu_loop = iemu.GetEnumerator();
DictionaryEntry de;
while( iemu_loop.MoveNext() ) {
    de = (DictionaryEntry)iemu_loop.Current;
    System.Console.WriteLine($"{de.Key} => {de.Value}");
}
```

## Dictionary( クラス ) : ループ( IEnumerator ) : while
```cs
Dictionary<string,string> idic = new Dictionary<string,string>();
idic.Add("A","X");
idic.Add("B","Y");

IEnumerable iemu = idic;
IEnumerator iemu_loop = iemu.GetEnumerator();
KeyValuePair<string,string> kvp;
while( iemu_loop.MoveNext() ) {
    kvp = (KeyValuePair<string,string>)iemu_loop.Current;
    System.Console.WriteLine( iemu_loop.Current );
    System.Console.WriteLine( iemu_loop.Current.GetType() );
    System.Console.WriteLine($"{kvp.Key} => {kvp.Value}");
}
```
```
[A, X]
System.Collections.Generic.KeyValuePair`2[System.String,System.String]
A => X
[B, Y]
System.Collections.Generic.KeyValuePair`2[System.String,System.String]
B => Y
```
