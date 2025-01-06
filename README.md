# PEFT TRAINING

This repository contains the implementation and analysis of two adapters—QLORA and IA3—integrated into the base model senseable/WestLake-7B-v2 for a medical chatbot application. The study evaluates the performance of these adapters, highlighting their strengths and weaknesses in handling medical queries.
## Objective
The primary goal of this project is to:
- Compare the performance of QLORA and IA3 adapters in a medical chatbot context.
- Analyze metrics like loss reduction, stability, and output quality.
- Deploy the models via Gradio for interactive testing.

## Features
- Base Model: senseable/WestLake-7B-v2
- Adapters: QLORA and IA3 for task-specific fine-tuning.
- Deployment: Gradio interface for interactive model testing.

## Installation
Run the following command to install the required libraries:\
pip install gradio python-dotenv transformers torch==2.0.1 transformers==4.38.2 datasets==2.18.0 peft==0.10.0 groq accelerate==0.28.0 trl==0.8.1 bitsandbytes==0.43.0 optimum==1.18.0 auto-gptq==0.7.1

## Clone the Repository
git clone https://github.com/jamalnasir551/PEFT-Training-FYP.git
cd PEFT-Training-FYP

## Sample Conversations
### QLORA
QLORA: Hello there!\
Patient: I'm feeling sick.\
QLORA: Just take some aspirin.\
Patient: First ask me symptoms, then suggest any medicine.\
QLORA: What's your cough like?

### IA3
IA3: Hello! How can I help you today?\
Patient: I'm feeling sick.\
IA3: Sorry to hear that. Can you please tell me more about what's going on? What symptoms are you experiencing?\
Patient: I've had a fever and cold cough since yesterday.\
IA3: It sounds like you might have a viral infection. I'd recommend acetaminophen and rest. If symptoms worsen, seek medical attention.

## Results
The performance comparison between QLORA and IA3 highlights significant differences in their suitability for the medical chatbot task. QLORA exhibited fluctuating and unstable loss during training, which prevented it from converging effectively. Its output quality was inconsistent, often producing hallucinations and irrelevant responses, making it less suitable for the task. In contrast, IA3 demonstrated consistently superior performance. Its training loss steadily approached near-zero values, indicating effective adaptation to the task. Additionally, IA3 produced reliable and contextually accurate responses, making it highly suitable for the medical chatbot application.

<img width="488" alt="Sample Converation" src="https://github.com/user-attachments/assets/d72c6cd3-58ba-4215-9774-7123e5d9c489" />
