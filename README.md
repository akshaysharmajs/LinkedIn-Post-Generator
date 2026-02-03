# ✍️ LinkedIn Influencer Post Generator

A specialized GenAI tool that allows influencers to clone their unique writing style and automate content creation. By analyzing historical post data, this tool uses **few-shot learning** to generate new content that maintains the user's authentic voice.

## 🎯 Project Overview
Designed for creators like Mohan, this tool bridges the gap between raw ideas and finished posts. Users feed their past LinkedIn content into the system, which then extracts key topics and linguistic patterns. When generating new posts, the tool references those specific examples to ensure the output matches the influencer's established brand.

## ⚙️ Technical Architecture

### **Stage 1: Content Intelligence**
* **Ingestion:** Processes historical LinkedIn posts.
* **Extraction:** Uses **gpt-oss-120b** to analyze and categorize posts by **Topic**, **Language**, and **Length**.
* **Style Mapping:** Identifies the unique "voice" and structural patterns used in previous successful content.

### **Stage 2: Contextual Generation**
* **Few-Shot Learning:** Injects relevant past posts into the LLM prompt as style guides.
* **Inference:** Powered by **Groq Cloud** and **Llama 3.2** for ultra-low latency generation.
* **Customization:** Users can toggle topics, languages, and lengths to produce tailor-made drafts.

## 🛠️ Tech Stack
* **LLM:** `openai/gpt-oss-120b` & `Llama 3.2`
* **Inference:** Groq Cloud (LPU™ Acceleration)
* **Orchestration:** LangChain
* **UI:** Streamlit

## 🚀 Set-up

1. To get started we first need to get an API_KEY from here: https://console.groq.com/keys. Inside `.env` update the value of `GROQ_API_KEY` with the API_KEY you created. 
2. To get started, first install the dependencies using:
    ```commandline
     pip install -r requirements.txt
    ```
3. Run the streamlit app:
   ```commandline
   streamlit run main.py
   ```