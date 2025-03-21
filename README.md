# Math Meme Repair

## Project Overview

The **Math Meme Repair** project focuses on fine-tuning an AI model to correct viral math memes with errors. The goal is to fix memes like “8 ÷ 2(2+2) = 1?” and provide the correct answer with explanations. For example, correcting this to the accurate result of **16**.

The model used for this project is **unsloth/DeepSeek-R1-Distill-Llama-8B**, fine-tuned on a custom dataset of 20 incorrect math memes. We also leveraged **Hugging Face** for model deployment and **Wandb** for tracking experiments and visualizing training progress.

## Goal

- **Fine-tune a model** to **correct math memes** by generating clear explanations and accurate answers.
- Provide **before-and-after examples** of meme corrections.
- Generate an **“error rating”** for the model’s personality when fixing the memes (e.g., "90% sass, 10% patience").

## Files in the Repository

- **fine-tuned-OA-deepseek-lama-8B**: Folder containing the fine-tuned model for meme correction.
- **outputs/**: Folder containing the output files, including corrected memes and explanations.
- **LICENSE**: License file for the project.
- **Q2.ipynb**: Jupyter notebook for the fine-tuning process and testing.
- **README.md**: Documentation for the Math Meme Repair project.
- **app.py**: Python file for the Streamlit-based web interface to interact with the model.
- **math_memes.jsonl**: Dataset file containing the list of incorrect math memes and their corrections.
- **requirements.txt**: List of Python dependencies required to run the project.

## Steps

### 1. Dataset Creation
- Collected **20 incorrect math memes** and social media posts containing **wrong PEMDAS**, **incorrect fractions**, and other common math errors.
- Each meme was paired with a **corrected explanation** to train the model.

### 2. Fine-Tuning
- Used the **unsloth/DeepSeek-R1-Distill-Llama-8B** model and fine-tuned it on the meme dataset for **2-3 epochs**.
- Fine-tuning was carried out using **Wandb** for experiment tracking and visualization, and **Hugging Face** for model integration and training.

### 3. Testing
- Provided **3 new incorrect math memes** to the fine-tuned model.
- Evaluated if the model correctly explained the mistakes and provided the corrected solution.
- Generated a fun **“error rating”** to reflect the model’s tone and attitude in its corrections.

## Deliverables

- A **before/after meme example**, showing the incorrect meme and the corrected explanation.
- A **funny "error rating"** for the model’s humor in dealing with meme mistakes.

### Example:

- **Incorrect Meme**: "8 ÷ 2(2+2) = 1?"
  - **Correct Answer**: 16

- **Error Rating**: "90% sass, 10% patience"

## Technologies Used

- **Model**: [unsloth/DeepSeek-R1-Distill-Llama-8B](https://huggingface.co/unsloth/DeepSeek-R1-Distill-Llama-8B)  
- **Fine-Tuning Framework**: **LoRA**, **Unsloth**
- **Libraries**: **Hugging Face Transformers**, **PyTorch**, **Wandb**

## How to Run

1. Clone the repository:  
   `git clone https://github.com/shaiiikh/Math-Meme-Repair.git`

2. Install dependencies:  
   `pip install -r requirements.txt`

3. Fine-tune the model:  
   run the cells in the **Q2.ipynb** file

4. Generate meme corrections:  
   run the inference cell in the **Q2.ipynb** file

5. Run Streamlit app:  
   `streamlit run app.py`

## Conclusion

The **Math Meme Repair** project demonstrates the ability of **Generative AI** to fix viral math memes, offering both a corrected answer and a clear explanation of the mistake. By using the **unsloth/DeepSeek-R1-Distill-Llama-8B** model, **LoRA** for memory optimization, and **Wandb** for experiment tracking, we were able to efficiently train the model and generate both correct answers and hum
