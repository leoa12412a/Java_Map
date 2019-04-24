# Java_Map
java.util中的集合類包含Java中某些最常用的類。最常用的集合類是List和Map。
Map提供了一個更通用的元素存儲方法.Map集合類用於存儲元素對（稱作"鍵(Key)"和"值(Value)"），其中每個鍵映射到一個值。
本文主要介紹java map的初始化，用法，map的四種常用的遍歷方式，map的排序以及常用api。

常見的Map的實現大概有以下四種:
* HashMap
* LinkedHashMap
* TreeMap
* Hashtable

## HashMap

HashMap最常用的Map，它根據鍵的HashCode值存儲數據，根據鍵可以直接獲取它的值，具有很快的訪問速度。
HashMap最多只允許一條記錄的鍵為Null（多條會覆蓋）;允許多條記錄的值為Null。非同步的。

```
package Map;

import java.util.HashMap;
import java.util.LinkedHashMap;
import java.util.Map;


public class example {
    public static void main(String[] args) {
        Hashmap();
    }

    public static void Hashmap() {
    
        Map map = new HashMap();    //new一個名為map的HashMap
        
        map.put("key9","value1");   //插入元素插入鍵(Key)和值(Value)
        map.put("key1","value1");  
        map.put("key3","value1");
        map.put("key5","value1");
        map.put("key4","value1");
        map.put("key6","value1");
        map.put("key7","value1");
        map.put("key2","value1");
        map.put("key8","value1");
        
        System.out.println(map);  // 輸出整個HashMap
        
        map.remove("key7");   // 移除key=key7的key&value
        
        map.forEach((k, v) -> System.out.println("key = " + k + ", value = " + v));  // 輸出Key內所有key和value
        
        map.clear();  // 清除
        
        System.out.println(map);
    }

}
```
產生結果

```
{key1=value1, null=null, key2=value1, key5=value1, key6=value1, key3=value1, key4=value1, key9=value1, key7=value1, key8=value1}
key = key1, value = value1
key = null, value = null
key = key2, value = value1
key = key5, value = value1
key = key6, value = value1
key = key3, value = value1
key = key4, value = value1
key = key9, value = value1
key = key8, value = value1
{}
```

## LinkedHashMap
## TreeMap
## Hashtable
HashTable已經被淘汰了，所暫不討論

以下是根據HashTable類的說明
```
If a thread-safe implementation is not needed, it is recommended to use HashMap in place of Hashtable.
If a thread-safe highly-concurrent implementation is desired, then it is recommended to use 
java.util.concurrent.ConcurrentHashMapin place of Hashtable.
```
```
如果不需要線程安全實現，建議使用HashMap代替Hashtable。如果需要線程安全的高度並發實現，
則建議使用java.util.concurrent.ConcurrentHashMap代替Hashtable。
```
