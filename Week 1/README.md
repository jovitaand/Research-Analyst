# Exploring Python Development Environments for Streamlit

## 1. Option 1: GitHub Codespaces
GitHub Codespaces provides a cloud-based development environment where you can run Python and Streamlit without needing to install anything on your local machine.

### Step 1: Create a GitHub Account
If you don’t already have one, sign up for GitHub at [github.com](https://github.com/).

### Step 2: Create a New Repository
1. Go to [GitHub](https://github.com/).
2. Click on **"New"** to create a repository.
3. Name it something like `streamlit-demo`.
4. Initialize the repository with a **README** file.
5. Click **"Create repository"**.

### Step 3: Open in Codespaces
1. In your newly created repository, click the **"Code"** button.
2. Select **"Codespaces"** and click **"Create codespace on main"**.
3. Wait for it to set up (a few minutes).

### Step 4: Install Python & Streamlit
Once the Codespace is ready, open the terminal and run:

```bash
pip install streamlit
```
Verify installation:
 ```bash
streamlit --version
```

### Step 5: Create a "Hello World" Streamlit App
1. In Codespaces, open the terminal
2. Create a new file:
``` bash
touch app.py
```
3. Open app.py and add the following code:
``` bash
import streamlit as st
st.title("Hello, Streamlit")
st.write("This is a basic streamlit app running in GitHub Codespaces. ")
```

### Step 6: Run the Streamlit App
In the terminal, run:
``` bash
streamlit run app.py
```
GitHub Codespaces will generate a public URL where you can view your running Streamlit app.

## Option 2: VS Code (Local Installation)
This setup requires installing Python, VS Code, and Streamlit on your local machine.

### Step 1: Install Python
1. Download and install Python: https://www.python.org/downloads/
2. Verify installation:
``` bash
python --version
```

### Step 2: Install VS code
1. Download and install Visual Studio Code (VS Code) from https://code.visualstudio.com/
2. Open VS Code and install the Python Extension:
   - Click on Extensions (Ctrl + Shift + X)
   - Search for Python
   - Click Install

### Step 3: Create a Virtual Environment (Recommended)
1. Open VS Code and open a new terminal.
2. Navigate to your project folder or create one:
``` bash
mkdir streamlit-project && cd streamlit-project
```
3. Create a virtual environment
``` bash
python -m venv venv
```
4. Activate the virtual environment:
   - Windows:
   ``` bash
   venv\Scripts\activate
   ```
   - Mac/Linux:
   ``` bash
   source venv/bin/activate 
   ```
5. Install Streamlit:
  ``` bash
  pip install streamlit
  ```
### Step 4: Create a Simple Streamlit App
1. Open VS Code and create a new file named `app.py`.
2. Add the following code:
``` bash
import streamlit as st

st.title("Hello, Streamlit!")
st.write("This is a basic Streamlit app running in VS Code.")
```
### Step 5: Run the Streamlit App
In the terminal, run:
``` bash
streamlit run app.py
```
A local web browser will open, displaying your Streamlit app.

---------------------------------------------------------------------------------------------------------------------------

## Comparison Table: Codespaces vs. VS Code

| Feature                 | GitHub Codespaces (Web) | VS Code (Local) |
|-------------------------|------------------------|-----------------|
| Installation Required?  | No                     | Yes             |
| Works in the Browser?   | Yes                    | No              |
| Internet Required?      | Yes                    | No (once set up) |
| Performance            | Limited by cloud resources | Uses local machine power |
| Best for...            | Quick development & collaboration | Full control over the environment |

