\# UrduGPT: Fine-Tuned and DPO-Aligned Urdu Language Model



UrduGPT is an end-to-end LLM engineering project that demonstrates the complete workflow of adapting a pretrained language model for Urdu using Supervised Fine-Tuning (SFT) and Direct Preference Optimization (DPO).



The project covers dataset preparation, parameter-efficient fine-tuning with LoRA, baseline evaluation, preference dataset generation, DPO alignment, and model publishing on Hugging Face. An LLM-as-Judge evaluation pipeline is included to compare the aligned model against the SFT baseline.



\---



\## Overview



This project implements the following workflow:



\- Supervised Fine-Tuning (SFT)

\- Baseline Response Evaluation

\- Preference Dataset Creation

\- Direct Preference Optimization (DPO)

\- LLM-as-Judge Evaluation \*(In Progress)\*



\---



\## Architecture



<p align="center">

&#x20; <img src="images/architecture.png" alt="Architecture" width="900">

</p>



\---



\## Project Structure



```text

UrduGPT/

│

├── notebooks/

│   ├── 01\_SFT\_Training.ipynb

│   ├── 02\_Baseline\_Evaluation.ipynb

│   ├── 03\_DPO\_Dataset\_Creation.ipynb

│   ├── 04\_DPO\_Training.ipynb

│   └── 05\_LLM\_as\_Judge\_Evaluation.ipynb

│

├── datasets/

│

├── images/

│   ├── architecture.png

│   └── training.png

│

├── requirements.txt

├── LICENSE

└── README.md

```



\---



\## Training Pipeline



The project follows a complete LLM alignment workflow:



1\. Fine-tune the base model using an Urdu instruction dataset.

2\. Generate baseline responses from the fine-tuned model.

3\. Construct a preference dataset containing prompts, chosen responses, and rejected responses.

4\. Align the model using Direct Preference Optimization (DPO).

5\. Compare the SFT and DPO models using an LLM-as-Judge evaluation pipeline.



\---



\## Technical Stack



\### Frameworks



\- PyTorch

\- Hugging Face Transformers

\- TRL

\- PEFT

\- Unsloth



\### Tools



\- Google Colab

\- Hugging Face Hub

\- Groq API



\### Languages



\- Python

\- JSON



\---



\## Models



\### Base Model



\- Llama 3.2 3B Instruct (4-bit, Unsloth)



\### Fine-Tuned Model



\- https://huggingface.co/mfayazkhan/UrduGPT-v2



\### DPO-Aligned Model



\- https://huggingface.co/mfayazkhan/UrduGPT-v2-DPO



\---



\## Installation



Clone the repository.



```bash

git clone https://github.com/mfayazkhan/UrduGPT.git

cd UrduGPT

```



Install the dependencies.



```bash

pip install -r requirements.txt

```



\---



\## Repository Workflow



| Notebook | Description |

|----------|-------------|

| 01\_SFT\_Training.ipynb | Fine-tune the base model using LoRA |

| 02\_Baseline\_Evaluation.ipynb | Generate baseline responses |

| 03\_DPO\_Dataset\_Creation.ipynb | Build the preference dataset |

| 04\_DPO\_Training.ipynb | Train the model using DPO |

| 05\_LLM\_as\_Judge\_Evaluation.ipynb | Evaluate SFT vs DPO models |



\---



\## Results



Completed:



\- Fine-tuned an Urdu language model using LoRA.

\- Built a preference dataset for alignment.

\- Trained a DPO-aligned model using TRL and Unsloth.

\- Published both models on Hugging Face.



Pending:



\- Complete the LLM-as-Judge evaluation.

\- Benchmark against additional open-source models.



\---



\## Future Work



\- Expand the Urdu instruction dataset.

\- Increase the preference dataset size.

\- Perform quantitative benchmarking.

\- Deploy the model using a production inference framework.

\- Build a web-based chat interface.



\---



\## License



This project is released under the MIT License.



\---



\## Author



\*\*Muhammad Fayaz Khan\*\*



\- GitHub: https://github.com/mfayazkhan50-AI

\- Hugging Face: https://huggingface.co/mfayazkhan

\- LinkedIn: https://www.linkedin.com/in/muhammad-fayaz-khan-271487381/

