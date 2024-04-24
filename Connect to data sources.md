These Streamlit snippets illustrate how to establish experimental connections and create a custom connection class:

**Establishing connections:**

    st.experimental_connection('pets_db', type='sql')
sets up an experimental connection named 'pets_db' of type SQL.

    conn = st.experimental_connection('sql')
retrieves the experimental SQL connection.

    conn = st.experimental_connection('snowpark')
retrieves the experimental Snowpark connection.

**Creating a custom connection class:**

The code defines a custom connection class `MyConnection` inheriting from `ExperimentalBaseConnection[myconn.MyConnection]`.

    _connect()
method establishes a connection using custom parameters and returns an instance of `MyConnection`.

    query()
method executes a query using the connection instance.

This code demonstrates Streamlit's experimental features for establishing and customizing connections to databases and other data sources.