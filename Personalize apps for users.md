# Show different content based on the user's email address.

    if st.user.email == 'jane@email.com':
        display_jane_content()
     elif st.user.email == 'adam@foocorp.io':
        display_adam_content()
     else:
        st.write("Please contact us to get access!")