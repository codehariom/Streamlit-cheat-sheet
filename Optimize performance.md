
## Cache data objects***

 **Define a cached function:**

    @st.cache_data
decorator marks the function `foo()` for caching.

    Inside `foo()
perform some expensive computation and return data.

 **Execute the cached function:**

    d1 = foo(ref1)
executes `foo()` with the argument `ref1` and caches the result in `d1`.

    d2 = foo(ref1)
retrieves the cached result for the same argument, so `foo()` is not executed again, and `d1 == d2`.

    d3 = foo(ref2) 
calls `foo()` with a different argument `ref2`, so the function executes again and caches the result in `d3`.

 **Clearing cache entries:**

    foo.clear()
clears all cached entries for the function `foo()`.

    st.cache_data.clear()
clears values from all cached functions, either in-memory or on-disk.

These snippets demonstrate how Streamlit allows you to cache expensive computations or data retrievals to improve performance.

## Cache global resources

E.g. TensorFlow session, database connection, etc.

    @st.cache_resource
    def foo(bar):
Create and return a non-data object
     return session
#Executes foo

    s1 = foo(ref1)
#Does not execute foo
#Returns cached item by reference, s1 == s2

     s2 = foo(ref1)
#Different arg, so function foo executes

    s3 = foo(ref2)
#Clear all cached entries for this function

    foo.clear()
#Clear all global resources from cache

    st.cache_resource.clear()

 ## Deprecated caching

 These Streamlit snippets showcase caching with the `@st.cache` decorator:

**Define a cached function:**

    `@st.cache
decorator marks the function `foo()` for caching.

     Inside `foo()
perform some expensive computation and return data.

 **Execute the cached function:**

    `d1 = foo(ref1)` executes `foo()` with the argument `ref1` and caches the result in `d1`.

    `d2 = foo(ref1)` retrieves the cached result for the same argument, so `foo()` is not executed again, and `d1 == d2`.

    `d3 = foo(ref2)` calls `foo()` with a different argument `ref2`, so the function executes again.

These snippets demonstrate how Streamlit allows you to cache function results to avoid redundant computation and improve performance.