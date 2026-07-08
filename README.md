Running the Project
Clone the repository or download the Agentic_Ai_CapstoneProject.ipynb notebook.

Open the notebook in Google Colab or your local Jupyter environment.

Execute the cells sequentially. The initial cells will download and load the 4-bit quantized Phi-3 model into GPU memory.

The final cell launches a Gradio web interface. A public or local URL will be generated (e.g., http://127.0.0.1:7860).

💻 How to Use
Upload Material: Use the left panel to upload your PDF lecture notes or reading material. Click "Process Document". The Supervisor will extract and store the text in its working memory.

Choose an Agent: Navigate through the tabs on the right panel to interact with different agents:

Click Generate Revision Notes in the Summary Tab.

Click Generate Practice Quiz to test your knowledge.

Click Generate Key Term Flashcards for vocabulary and core concepts.

Click Generate Study Schedule for a structured revision plan.

Type a question and click Ask Agent in the Doubt Solver tab to get text-grounded answers.

⚠️ Notes on Hardware limitations
The PDF Reader agent currently caps context extraction to 12,000 characters to prevent out-of-memory (OOM) errors and stay within the context window limits of the LLM.

Due to 4-bit quantization, the model fits comfortably on consumer hardware (like the free tier Colab T4 GPU).

📄 License
This project is for educational purposes as a Capstone Project demonstrating Agentic AI workflows.
"""

with open("README.md", "w", encoding="utf-8") as f:
f.write(markdown_content)

print("README.md generated successfully.")
