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
