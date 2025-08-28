Today I learned the difference between using an object, an array, and a simple interface in React state with TypeScript, especially when working with API calls.
1. An **object** is like a dictionary, good for saving data by key (like an ID). This makes it useful for caching, because once some data is saved, it can be used again without calling the API each time. 
2. An **array** is better when the order of items matters, like showing a list, but finding one item is slower because every item has to be checked. 
3. A **simple interface** is only for storing one piece of data at a time, so if new data is needed, another API call has to be made.
##### Key takeaway:
 use objects for caching and quick lookups, arrays for ordered lists, and simple interfaces for single values. Picking the right one helps make apps faster and reduces extra API calls.
