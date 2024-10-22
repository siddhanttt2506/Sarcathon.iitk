# FAQ Search System

This repository contains a web-based FAQ search system that allows users to input queries and returns the most relevant FAQs based on cosine similarity using TF-IDF (Term Frequency-Inverse Document Frequency). The system is built using **Streamlit** for the front-end and **Pyngrok** for exposing the local app to the internet.

## Features
- **Search Functionality:** Input a query and get the top 3 most relevant FAQs with relevance scores.
- **TF-IDF and Cosine Similarity:** FAQ data is vectorized using TF-IDF, and cosine similarity is used to match user queries to FAQ questions.
- **Web Interface:** Built with Streamlit, allowing easy interaction.
- **Localhost Exposure:** Pyngrok creates a public URL to expose the Streamlit app.

## Setup Instructions
1. **Install Required Libraries:**
   ```bash
   pip install streamlit
   pip install pyngrok
2. **Ngrok Authentication:**

   - Get an Ngrok account and authentication token from [here](https://dashboard.ngrok.com).
   - Authenticate Ngrok:
     ```bash
     ngrok authtoken <your_ngrok_authtoken>
     ```

3. **Run the App:**

   - Write the code into `app.py` and run the Streamlit app:
     ```bash
     streamlit run app.py
     ```

4. **Create Public URL:**

   - Expose the app via Pyngrok:
     ```python
     public_url = ngrok.connect(8501, "http")
     print(f"Streamlit is live at: {public_url}")
     ```
