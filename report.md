# VARIOUS CACHING TECHNIQUES

In this modern time of fast-developing technologies, we also need to cope up with the same speed, updating our technologies to make our product fast and robust. 

 In the world of fast and modern database systems, still, they can be slow in real-time data fetching. One of these must-have technological updates is using caching. Caching is the easiest and effective way to make data retrieval fast. Here are some caching techniques which can be implemented on our product. This research includes the pros and cons of using them.

* ### **CACHE-ASIDE**

    Cache-aside is the most commonly used caching techniques. The application first checks the cache for the data. If data is present(cache hit) the data is returned but if data is not present in the cache (cache miss) the app then fetch the data from the database, then returns data to the client and also store in the cache for future use.

    **Pros-**
    - If the cache goes down, the app can fetch data directly from the database.
    - The data model can be different from database which can be useful to store data in the cache as per need.
    
    **Cons-**
    - It uses to write in the database directly. Which can be sometimes inconsistent.

    For more Info [Click here](https://docs.microsoft.com/en-us/azure/architecture/patterns/cache-aside#:~:text=An%20application%20can%20emulate%20the,into%20the%20cache%20on%20demand.&text=When%20the%20item%20is%20next,added%20back%20into%20the%20cache.)


* ### **READ-THROUGH CACHE**

    It is present in between client and database, in case of a cache hit it returns to the client but in case of a cache miss, it directly reads the data from database and populates the cache for future.

    **Pros-**
    - The cache can directly fetch data from the database and populate the cache.
    - Works well in heavy load.
    
    **Cons-**
    - The data model of Cache is the same as the database.

    For more Info [Click here](https://docs.oracle.com/cd/E15357_01/coh.360/e15723/cache_rtwtwbra.htm#COHDG5177)

* ### **WRITE-THROUGH CACHE**

    In this writing strategy, data is first written to the cache and then to the database.
   
    **Pros-**
    - Great when used with Read-through cache.
    - No stale data.
    
    **Cons-**
    - Not Good when used alone.
    - 2 network operations need to write in cache and database.

    For more Info [Click here](https://docs.oracle.com/cd/E15357_01/coh.360/e15723/cache_rtwtwbra.htm#COHDG5177)

* ### **WRITE-BEHIND CACHE**

    In this data is stored asynchronously stored first in the cache and then to the database.
   
    **Pros-**
    - Read and Write both happen on the caching side. This improves performance.
    - Suitable in heavy usage.
    
    **Cons-**
    - Directing access to the database can lead to using stale data.

    For more Info [Click here](https://docs.oracle.com/cd/E15357_01/coh.360/e15723/cache_rtwtwbra.htm#COHDG5177)


### **SOME REAL TIME CACHING SOFTWARE SOLUTIONS**
* Memcached
* Redis
* DynamoDB Accelerator (DAX)
* Aerospike
* Hazelcast
* Couchbase

### **SUMMARY**

 In this Report here is the working, pros and cons of the popular caching techniques. The relevant technique can be chosen as per need.

### **REFERENCES**

* https://medium.com/datadriveninvestor/all-things-caching-use-cases-benefits-strategies-choosing-a-caching-technology-exploring-fa6c1f2e93aa
* https://codeahoy.com/2017/08/11/caching-strategies-and-how-to-choose-the-right-one/
* https://docs.oracle.com/cd/E15357_01/coh.360/e15723/cache_rtwtwbra.htm#COHDG5177
* https://docs.microsoft.com/en-us/azure/architecture/patterns/cache-aside#:~:text=An%20application%20can%20emulate%20the,into%20the%20cache%20on%20demand.&text=When%20the%20item%20is%20next,added%20back%20into%20the%20cache.