# Maevis
![image](https://github.com/user-attachments/assets/a348f97c-cfb3-402c-be3c-5657068dd55d)

**Maevis** is a lightweight, local-first chatbot powered by [Bun](https://bun.sh) and [Ollama](https://ollama.com). It enables fast, private conversations using local LLMs like LLaMA or Qwen, all without the cloud.

---

## 🚀 Features

- ⚡ Ultra-fast Bun runtime
- 🧠 Local LLM inference with Ollama
- 🔐 Private, offline-capable architecture
- 💬 Simple HTTP API for integration
- 🧩 Modular and extensible

---

## 📦 Requirements

- [Bun](https://bun.sh) (v1.0+)
- [Ollama](https://ollama.com) installed and running
- At least 4 GB of free RAM or swap space for larger models

---

## 🛠️ Setup

1. **Install dependencies**  
   ```bash
   bun install
   ```

2. **Ensure Ollama is running**  
   Install [Ollama](https://ollama.com) if you haven’t already, and run a model:
   ```bash
   ollama run qwen2:1.5b
   ```
   > 💡 Tip: Start with `qwen2:1.5b` — it's lightweight and fast for local testing.

3. **Configure the model (optional)**  
   Edit the model name inside `index.ts` if you'd like to use another model:
   ```ts
   const model = 'qwen2:1.5b'; // Or 'llama3:latest', etc.
   ```

4. **Run the Maevis server**  
   ```bash
   bun run index.ts
   ```
   Maevis will now be available at `http://localhost:3000`.

5. **Test the chatbot**  
   Use `curl`, Postman, or any HTTP client to test the API:
   ```bash
   curl -X POST http://localhost:3000/chat \
     -H "Content-Type: application/json" \
     -d '{"prompt": "Hello, Maevis!"}'
   ```
   Example response:
   ```json
   {
     "response": "Hello! How can I assist you today?"
   }
   ```




