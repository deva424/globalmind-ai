# Advanced-Multilingual-Assistant
Elevanceskills internship project
# 🌐 GlobalMind AI: Advanced Multilingual Assistant

##  Problem Statement
The goal of this project is to extend an existing chatbot to support at least three additional languages beyond its original base. The system is engineered to solve the following challenges:
*   **Automated Linguistic Intelligence**: Automatically detecting user language without manual toggles.
*   **Seamless Fluidity**: Switching between supported languages mid-session without losing context.
*   **Cultural Contextualization**: Delivering responses that adhere to regional social norms and etiquette.
*   **Enhanced NLP**: Leveraging Large Language Model (LLM) architectures to improve cross-lingual understanding and generation quality.

---

##  Requirements

### **Technical Dependencies**
*   **Python 3.9+**: Core programming language.
*   **Streamlit**: Framework for the interactive chat interface.
*   **LangChain**: Framework for LLM orchestration and memory management.
*   **Google Gemini 1.5 Flash**: The generative engine (via `langchain-google-genai`).
*   **Langdetect**: For real-time language identification.
*   **Python-Dotenv**: For secure API key management.

### **API Prerequisites**
*   **Google AI Studio Key**: A valid API key is required to access the Gemini models.

---

##  Methodology

The chatbot utilizes a **Modular Multilingual Pipeline** to ensure accuracy and cultural relevance:

1.  **Input Detection**: Every user message is analyzed by `langdetect` to identify the ISO language code (e.g., 'es' for Spanish, 'hi' for Hindi).
2.  **Etiquette Injection**: Based on the detected code, a custom logic engine selects a "Cultural Etiquette" profile. This defines the tone, such as formal German ("Sie") or respectful Hindi ("Ji").
3.  **Context Management**: The system maintains a sliding window of the last 6 messages to preserve conversation history.
4.  **Prompt Orchestration**: A dynamic `SystemMessage` is generated, combining the detected language rules with the user’s history.
5.  **Generative Inference**: The context-rich prompt is processed by **Gemini 1.5 Flash**, which generates a response that respects both the linguistic and cultural constraints of the user.

---

##  Deployment

### **1. Local Installation**
1.  **Clone the Repository**:
    ```bash
    git clone [https://github.com/yourusername/globalmind-ai.git](https://github.com/yourusername/globalmind-ai.git)
    cd globalmind-ai
    ```
2.  **Install Requirements**:
   ```bash
    pip install -r requirements.txt
