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
