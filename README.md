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
