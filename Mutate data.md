These code snippets demonstrate how to add rows to a dataframe or a chart after displaying them using Streamlit:

For a dataframe

    element = st.dataframe(df1)
displays the initial dataframe `df1`.

    element.add_rows(df2)
adds rows from another dataframe `df2` to the displayed dataframe.

For a chart

    element = st.line_chart(df1)
displays the initial line chart using data from `df1`.

    element.add_rows(df2)
adds data from another dataframe `df2` to the displayed chart.

