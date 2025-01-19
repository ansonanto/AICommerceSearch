# AICommerceSearch

# Multi-Modal Search and Conversational System

## Overview
This project aims to develop a **multi-modal search and conversational system** that enhances website interactivity. The system leverages advanced AI models to process various types of inputs (images, text, audio) and provides intelligent responses, including product recommendations and detailed information retrieval. The solution is scalable and can be integrated into any website to offer chatbot-like functionality.

---

## Features
- **Multi-Modal Input Support**:
  - Accepts **images**, **text descriptions**, and **audio queries**.
  - Converts inputs into vector embeddings using state-of-the-art models like **CLIP**, **BLIP**, and **BLIP2**.
- **Product Search**:
  - Performs similarity searches on a vector database to find relevant items.
  - Retrieves information such as price, availability, and detailed descriptions.
- **Conversational Capabilities**:
  - Integrates **Retrieval-Augmented Generation (RAG)** for intelligent and context-aware conversations.
  - Provides chatbot functionality for seamless user interaction.
- **Model Comparison**:
  - Evaluates and compares performance across embedding models (CLIP, BLIP, BLIP2) during inference.
  - Selects the best-performing model for optimal results.
- **Scalability**:
  - Designed to be integrated into any website, enabling customized AI-driven search and interaction.

---

## Use Cases
1. **E-Commerce**:
   - Users upload a product image or provide a description.
   - The system retrieves similar products and provides relevant details.
2. **Accessibility**:
   - Supports audio queries for users who prefer voice interactions.
   - Enhances user experience by accommodating diverse input formats.
3. **Custom AI Chatbots**:
   - Generalizes the solution to make any website interactive with a ready-to-use chatbot.

---

## System Architecture
### Components:
1. **Input Processing**:
   - Image Embedding: Utilizes **CLIP**, **BLIP**, or **BLIP2**.
   - Text Embedding: Converts textual descriptions into vector representations.
   - Audio Embedding: Converts audio input into text and then processes it as a vector.
2. **Vector Database**:
   - Stores embeddings of the product catalog.
   - Enables efficient similarity searches using libraries like **FAISS** or tools like **Pinecone**.
3. **Retrieval-Augmented Generation (RAG)**:
   - Combines embedding-based retrieval with a language model for conversational AI.
   - Models like GPT, LLaMA, or Claude handle the conversational output.
4. **Web Interface**:
   - Provides an interface for users to upload inputs and receive results.
   - Displays product matches with detailed descriptions.

---

## Installation
### Prerequisites
- Python 3.9+
- A virtual environment tool (e.g., `venv`, `conda`)
- GPU-enabled system for inference (optional but recommended)

### Setup
1. Clone the repository:
   ```bash
   git clone https://github.com/your-repo/multimodal-search.git
   cd multimodal-search
   ```
2. Create and activate a virtual environment:
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```
3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
4. Set up the vector database:
   - Install **FAISS** or configure **Pinecone** for remote indexing.
   - Populate the database with product embeddings.
5. Configure the environment:
   - Add API keys for models (if using hosted solutions like OpenAI or HuggingFace).
   - Update the `config.yaml` file with database and model settings.

---

## Usage
1. **Run the server**:
   ```bash
   python app.py
   ```
2. **Access the web interface**:
   - Navigate to `http://localhost:5000` in your browser.
3. **Interact with the system**:
   - Upload an image, input a text description, or provide an audio query.
   - View retrieved results, including product details and conversational responses.

---

## Future Work
- Implement advanced indexing techniques for faster similarity search.
- Enhance multi-modal capabilities by supporting additional input types (e.g., video).
- Improve scalability for handling large datasets.
- Experiment with additional models to further optimize performance.
  

## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

