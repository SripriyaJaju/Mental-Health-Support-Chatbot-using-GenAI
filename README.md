# Mental-Health-Support-Chatbot-using-GenAI
This project fine-tunes the Gemma 3 4B language model using the Unsloth framework on the CACTUS Mental Health dataset. It creates a Conversational AI system capable of offering compassionate and personalized support based on Cognitive Behavioral Therapy (CBT) principles.

🔍 Project Overview

Model: Gemma 3 4B (fine-tuned using LoRA via Unsloth)

Dataset: CACTUS Mental Health Dataset (multi-turn client-counselor dialogues)

Domain: Mental Health Support using CBT techniques

Objective: Provide empathetic, secure, and personalized AI-driven mental health guidance

📁 Dataset

Name: CACTUS Mental Health Dataset

Type: Open-domain therapeutic conversations

Features: Client statements, counselor responses, CBT plan, and techniques

Source: https://arxiv.org/abs/2407.03103

⚙️ Technologies Used

Python 3.10+

PyTorch

Transformers (Hugging Face)

Unsloth (LoRA-based fine-tuning)

WandB (experiment tracking)

Kaggle (for execution environment)

📌 Methodology

Data Preprocessing:

Dialogue parsing into (Client, Counselor) pairs

Conditional addition of CBT context

Standardization and tokenization using Unsloth’s get_chat_template

Model Fine-Tuning:

Loaded "unsloth/gemma-3-4b-it" in 4-bit mode

Applied LoRA using FastModel.get_peft_model

Training via SFTTrainer with ~1,000 examples and SFTConfig settings

Evaluation:

Metrics: BLEU Score, ROUGE-L Score, and Perplexity

Results:

BLEU Score: 0.35

ROUGE-L: 0.52

Perplexity: ~4.2

📈 Results

The chatbot demonstrates the ability to generate contextually accurate, empathetic, and CBT-aligned responses.

Metric performance supports the effectiveness of domain-specific fine-tuning.

📦 Setup & Usage

Clone this repository:
git clone https://github.com/Sripriyajaju/Mental-Health-Support-Chatbot-using-GenAI.git

Install dependencies:
pip install -r requirements.txt

Run the notebook:
Execute on Kaggle or local GPU environment supporting bfloat16 or 4-bit inference.

Configure:

Add your Hugging Face and WandB tokens in the notebook

Dataset auto-loads from HF hub: saarib2405/Cactus-Mental-Health-dataset
