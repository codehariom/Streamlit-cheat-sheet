
***Cache data objects***

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