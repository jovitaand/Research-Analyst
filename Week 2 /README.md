Week 2 Guide: Developing and Deploying a Simple Chatbot

Introduction

This guide provides step-by-step instructions for building and deploying a simple chatbot using Streamlit. The chatbot captures user input and responds with a message while displaying the chat history. Additionally, we will cover best practices, challenges, and deployment options.

1. Setting Up the Development Environment

Step 1: Install Dependencies

Ensure you have Streamlit installed. If not, install it using:

```bash
pip install streamlit
```

Step 2: Create the Chatbot File

1. Create a new file named `chatbot.py`.
2. Copy and paste the following chatbot code:
```bash
import streamlit as st

if "messages" not in st.session_state:
    st.session_state["messages"] = []

st.title("Simple Chatbot")

for message in st.session_state["messages"]:
    with st.chat_message(message["role"]):
        st.write(message["content"])

user_input = st.chat_input("Say something...")
if user_input:
    st.session_state["messages"].append({"role": "user", "content": user_input})
    bot_response = f"Thank you for telling me: {user_input}"
    st.session_state["messages"].append({"role": "assistant", "content": bot_response})

    with st.chat_message("user"):
        st.write(user_input)
    with st.chat_message("assistant"):
        st.write(bot_response)
```

2. Running the Chatbot Locally

Step 1: Navigate to the Project Directory

Open a terminal and go to the directory where `chatbot.py` is saved.

Step 2: Run the Streamlit Application

Execute the following command:

```bash
streamlit run chatbot.py
```

Step 3: Open in Browser

- The terminal will display a **local URL** (e.g., `http://localhost:8501`).
- Open this link in a **web browser** to interact with the chatbot.

Step 4: Stop the Chatbot

To **stop** the chatbot, press:

```bash
Ctrl + C
```

3. Deploying the Chatbot

Option 1: Deploy on Streamlit Cloud

1. Push the chatbot code to **GitHub**.
2. Go to [Streamlit Cloud](https://share.streamlit.io/).
3. Click **"Deploy an App"**.
4. Select the GitHub repository.
5. Deploy and get a **public URL** for your chatbot.

Option 2: Deploy on Heroku (Optional)

1. Create a `requirements.txt` file:

```bash
pip freeze > requirements.txt
```

2. Follow the **Heroku CLI deployment steps**.

4. Best Practices & Challenges

Best Practices:

- Use **`st.session_state`** to maintain chat history across user interactions.
- Ensure **user input is properly handled** to prevent errors.
- Keep responses **simple and interactive**.

Challenges & Solutions:

Challenge

Solution

Losing chat history

Used `st.session_state` to retain previous messages.

API response delays

Consider adding a loading indicator (`st.spinner`).

Deployment errors

Verified dependencies and environment variables before deploying.

5. Summary and Next Steps

Summary:

- Built a simple chatbot using **Streamlit**.
- Implemented **chat history retention** using `st.session_state`.
- Explored **deployment options** using Streamlit Cloud and Heroku.

Next Steps:

- Improve the chatbot by integrating **AI-based responses**.
- Add **custom styling and UI enhancements**.
- Deploy on **AWS Lambda** for scalability.


**End of Week 2 Guide 🚀**
