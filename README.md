# 📚 AI-Powered Multi-Agent Study Assistant

An intelligent **multi-agent AI study assistant** that transforms any PDF into a personalized learning experience. Built using **Microsoft Phi-3 Mini**, **Transformers**, **Gradio**, and **pdfplumber**, the system automatically extracts content, summarizes notes, generates quizzes, creates flashcards, answers doubts, and prepares personalized study plans through a supervisor-based multi-agent architecture.

---

## 🚀 Features

✅ Upload any educational PDF

✅ Automatically extract text from the document

✅ Generate concise revision notes

✅ Create multiple-choice quizzes

✅ Generate flashcards for active recall

✅ Ask questions about the uploaded document

✅ Receive personalized study schedules

✅ Interactive Gradio web interface

---

# 🏗️ Project Architecture

```
                    PDF Upload
                         │
                         ▼
                 PDF Reader Agent
                         │
         Extracted Document Context
                         │
                         ▼
                Supervisor Agent
        (Stores Shared Document Memory)
     ┌──────────┬──────────┬──────────┬──────────┬──────────┐
     ▼          ▼          ▼          ▼          ▼
 Summary     Quiz      Flashcards  Doubt Solver Study Planner
  Agent      Agent        Agent        Agent        Agent
     │          │            │            │            │
     └──────────┴────────────┴────────────┴────────────┘
                         │
                         ▼
                 Gradio User Interface
```

---

# 🤖 Multi-Agent Workflow

## 1. PDF Reader Agent

Responsible for:

- Reading uploaded PDF files
- Extracting clean text
- Removing unnecessary formatting
- Providing document context to all downstream agents

**Library Used**

- pdfplumber

---

## 2. Summary Agent

Uses the Phi-3 language model to generate:

- Revision notes
- Bullet-point summaries
- Key concepts
- Important takeaways

---

## 3. Quiz Generator Agent

Automatically generates:

- Multiple Choice Questions
- Four options
- Correct answer
- Concept-based assessment

Useful for self-testing after studying.

---

## 4. Flashcard Generator Agent

Creates active recall flashcards in the format:

```
Question
↓

Answer
```

Ideal for revision and spaced repetition learning.

---

## 5. Doubt Solver Agent

Allows users to ask natural language questions regarding the uploaded document.

Example:

> "Explain Newton's Second Law."

The agent answers using only the uploaded document as context.

---

## 6. Study Planner Agent

Analyzes the document and prepares a structured revision schedule including:

- Daily study goals
- Revision timeline
- Important chapters
- Time allocation

---

## 7. Supervisor Agent

The Supervisor orchestrates the complete system.

Responsibilities include:

- Loading PDFs
- Managing shared document memory
- Coordinating all agents
- Preventing repeated document processing
- Providing a single interface for the UI

This design follows a **Supervisor-based Multi-Agent Architecture**, where all specialized agents communicate through a centralized controller.

---

# 🧠 AI Model

The project uses:

**Microsoft Phi-3 Mini 4K Instruct**

Features:

- 3.8 Billion parameters
- Instruction tuned
- Optimized for reasoning
- Lightweight enough for Google Colab
- Loaded using 4-bit quantization

---

# ⚙️ Technologies Used

| Category | Technology |
|----------|------------|
| Programming | Python |
| LLM | Microsoft Phi-3 Mini 4K Instruct |
| Framework | Hugging Face Transformers |
| Quantization | BitsAndBytes |
| Acceleration | Accelerate |
| PDF Processing | pdfplumber |
| UI | Gradio |
| Deep Learning | PyTorch |

---

# 📦 Installation

Clone the repository

```bash
git clone https://github.com/yourusername/AI-Multi-Agent-Study-Assistant.git

cd AI-Multi-Agent-Study-Assistant
```

Install dependencies

```bash
pip install -q transformers accelerate bitsandbytes pdfplumber gradio
```

Upgrade Pillow

```bash
pip install --upgrade Pillow
```

---

# ▶️ Running the Project

Run the notebook

```
Agentic_Ai_CapstoneProject.ipynb
```

or launch the Gradio application

```python
demo.launch()
```

A local web interface will open where users can upload PDFs and interact with all study agents.

---

# 📂 Project Structure

```
.
├── Agentic_Ai_CapstoneProject.ipynb
├── README.md
├── requirements.txt
└── sample_pdfs/
```

---

# 💻 User Workflow

1. Upload an educational PDF.
2. PDF Reader extracts the content.
3. Supervisor stores the extracted document.
4. Choose one of the available study tools:
   - Generate Summary
   - Generate Quiz
   - Generate Flashcards
   - Ask Questions
   - Generate Study Plan
5. Receive AI-generated learning materials instantly.

---

# 🌟 Example Use Cases

- 📖 College lecture notes
- 📚 Research papers
- 📝 Competitive exam preparation
- 📑 Textbook chapters
- 📄 Class handouts
- 🎓 Revision before exams

---

# 📈 Advantages

- Saves hours of manual note-making
- Improves revision efficiency
- Encourages active recall
- Personalized learning experience
- Interactive AI tutor
- Modular multi-agent design
- Easily extensible with new agents

---

# 🔮 Future Improvements

- Retrieval-Augmented Generation (RAG) using vector databases
- Multi-document support
- Voice interaction
- Image and diagram understanding
- Citation-aware responses
- Progress tracking dashboard
- Learning analytics
- Cloud deployment
- User authentication
- Export notes to PDF

---

# 📸 Screenshots

Add screenshots of:

- Home Interface
- PDF Upload
- Summary Generation
- Quiz Generation
- Flashcards
- Doubt Solver
- Study Planner

---

# 🤝 Contributing

Contributions are welcome!

1. Fork the repository
2. Create a feature branch

```bash
git checkout -b feature-name
```

3. Commit your changes

```bash
git commit -m "Added new feature"
```

4. Push to GitHub

```bash
git push origin feature-name
```

5. Open a Pull Request

---

# 📜 License

This project is licensed under the MIT License.

---

# 👨‍💻 Author

**Chirag Khandelwal**

- IIT Bombay
- Civil Engineering
- AI • Machine Learning • Multi-Agent Systems

---

## ⭐ If you found this project helpful, consider giving the repository a star!
