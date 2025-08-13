
 # Cache Eviction Strategies

    When we save data in to cache after certain period of time it should be deleted as well. so the process to delete from
    cache is called cache eviction.

    why to delete because we will have a limited size so need to remove unnecessary datas or suppose you have some configurations
    suppose for a netflix having 4 plans and you have mentioned deletion after 10 years but suppose you have added one more plans
    so now total 5 plans so in caching since only 4 plans so only it will view 4 plans not 5 plans it will not auto deleted so manually
    we have to delete.

    generally we keep ttl(time to live) for caching 4 hours on an average. so automatically from cache it will get deleted after
    4 hours. when first call will come for listing which mean plan listing then he won't found data in cache so he will find data
    from database. now once he get the data from db then we will set data into cache. so once response will come from db and going 
    to client back then we will set that in cache. cache miss means data not found in cache.

    
 # Cache Eviction: How to delete caching

    1. LRU - Least Recently Used

        this strategy will delete that data from caching which will not be in use for a very long time.
            so here which caching not be used which we are tracking here like this caching not been use since 10 days,
            or since 1 year for this we need additional memory. 

    2. MRU - Most Recently Used
    
        If you have a business logic like to delete most recently used data then we should go for a
        MRU.

    3. LFU - Least Frequently Used

        which means how many times being used suppose some caching data is getting used 1000 times and some caching
        data only being used 1 times. so 1 time caching data we can delete because there is no use to keep that.
        suppose we have netflix in that you have many genres like bollywood, NMA, Hollywood...etc. because no one is watching
        bollywood so that caching data no use to keep it. so you have see the count if less then deleted to save memory.

    4. FIFO

        first in first out, which come first will get deleted. we have one caching in that caching we can save only 4 data. 
        when 5th data came so there is no space so we can delete first data. 
    
    5. LIFO

        last in first out, evicts the last added data which is happening in stack.

    6. RR - Random Replacement

        Randomly we evicts caching so there will be no high and low priority of caching data.

