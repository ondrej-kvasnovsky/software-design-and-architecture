# Storage and Retrieval

## Hash indexes

In databases, we are appending new records into a file. First we calculate hash from the record we are inserting and we use it as a key. The value behind the key is a reference offset of new record in the file. The hash indexes need to be kept in memory \(becuase creating hash tables on disk is tricky and accessing values using random access is slow\).

## SSTables

Sorted String tables does not have to be kept in memory. The point is to keep table sorted by keys. Then we can have in memory index that is skipping some records, becuase we know that if, for example, we are looking for b it will be somewhere between a and c keys. That means, we can store batch of values behind a key \(and it can be also compressed\). 

SSTable can be easily created from LSM-tree \(Log-Structured Merge Tree\) - which is a sorted balanced tree. LSM trees are typically faster for writes. Reads are slow becuase LSM keeps data in blocks of variable size. 

## B-Tree

B-Trees keep key-value pairs sorted by key, like SSTables. Unlike SSTables, B-Trees keep data in fixed size blocks. 

B-Trees are typically faster for reads. 





