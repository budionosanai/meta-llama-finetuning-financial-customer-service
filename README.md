## 📘 Overview

This repository explains end-to-end fine-tuning Llama 3.2-1B-Instruct model for financial customer service use case that can handle financial customer service requests with accurate and helpful responses.

## 📁 Repository Structure

| File / Notebook | Description |
| :--- | :--- |
| `LlamaBeforeFineTuning.ipynb` | Notebook of deploy Llama 3.2-1B-Instruct model and test asking several prompts/questions about financial customer service to Llama model before fine-tuning. |
| `LlamaFineTuning.ipynb` | Notebook of fine-tuning Llama 3.2-1B-Instruct model using PEFT (Parameter-Efficient Fine-Tuning) technique, LoRA (Low-Rank Adaptation) technique and SFT (Supervised Fine-Tuning) technique then export result of this fine-tuning model to HuggingFace model repository. |
| `LlamaAfterFineTuning.ipynb` | Notebook of deploy fine-tuning model and test asking same prompts/questions in `LlamaBeforeFineTuning.ipynb` to fine-tuning model and see difference responses from several prompts/questions related to financial customer service before and after fine-tuning. |
| `fcsdataset.jsonl` | Financial customer service dataset used in the `LlamaFineTuning.ipynb`. |

## ✅ Prerequisites

1. **Google Colab**: Access to **Google Colab** for fine-tuning and inference using T4 GPU, you can open [here.](https://colab.research.google.com)

2. **Hugging Face**: Access to create access token and Llama model, you can sign up/sign in [here.](https://huggingface.co)

## 🚀 Getting Started

1. Clone this repository
```bash
git clone https://github.com/budionosanai/meta-llama-finetuning-financial-customer-service.git
cd meta-llama-finetuning-financial-customer-service
```

2. Request access to [Llama 3.2 1B Instruct](https://huggingface.co/meta-llama/Llama-3.2-1B-Instruct) model and wait approval from Meta.

3. Open, run and following this notebooks :

| Notebook | Using |
| :--- | :--- |
| 1 - **[Llama before fine-tuning](./LlamaBeforeFineTuning.ipynb)** | **Google Colab** and [Llama 3.2 1B Instruct](https://huggingface.co/meta-llama/Llama-3.2-1B-Instruct) |
| 2 - **[Llama fine-tuning process](./LlamaFineTuning.ipynb)** | **Google Colab** and [Llama 3.2 1B Instruct](https://huggingface.co/meta-llama/Llama-3.2-1B-Instruct) |
| 3 - **[Llama after fine-tuning](./LlamaAfterFineTuning.ipynb)** | **Google Colab** and [Llama fine tuning model](https://huggingface.co/budionosan/llama-finetuning-financial-customer-service) |

4. Create Python environment variable using python-dotenv, you can see this [link.](https://pypi.org/project/python-dotenv/) then write Hugging Face token (e.g.  `HUGGINGFACE_TOKEN=your_token_here`) in a Notepad file, then save the file with the name `....txt` (e.g. `env.txt`). You can see this [link.](https://huggingface.co/docs/hub/en/security-tokens) to create HuggingFace token.

## ⚠️ Warning

**Ensure securely API keys such as Hugging Face token — DO NOT HARDCORE them in notebooks.**

## 📚 Resources

* [PEFT documentation](https://huggingface.co/docs/peft/en/index)
* [LoRA documentation](https://huggingface.co/docs/peft/main/en/conceptual_guides/lora/)
* [SFT documentation](https://huggingface.co/docs/trl/en/sft_trainer/)

## 🙏 Acknowledgments

**Hugging Face, Meta Llama and Google Colab**