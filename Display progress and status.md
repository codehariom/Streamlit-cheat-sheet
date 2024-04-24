These Streamlit snippets demonstrate various visual elements and notifications:

1. **Show a spinner during a process:**
   - `with st.spinner(text='In progress'):` displays a spinner with the text "In progress".
   - Inside the context manager, a process (here, `time.sleep(3)`) is simulated.
   - After the process, `st.success('Done')` displays a success message.

2. **Show and update progress bar:**
   - `bar = st.progress(50)` creates a progress bar initialized to 50%.
   - After a delay (`time.sleep(3)`), `bar.progress(100)` updates the progress bar to 100%.

3. **Other visual elements and notifications:**
   - `st.balloons()`: Displays flying balloons animation.
   - `st.snow()`: Displays falling snow animation.
   - `st.toast('Mr Stay-Puft')`: Shows a toast notification with the message "Mr Stay-Puft".
   - `st.error('Error message')`, `st.warning('Warning message')`, `st.info('Info message')`, `st.success('Success message')`: Displays different types of messages.
   - `st.exception(e)`: Displays an exception message `e` with a traceback.

These snippets showcase Streamlit's ability to provide visual feedback, notifications, and animations to enhance user experience.