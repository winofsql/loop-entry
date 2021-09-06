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
## 
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
