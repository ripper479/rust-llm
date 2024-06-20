# Fine-tuning CodeLlama-7b-Instruct for Rust Code Generation using PEFT 

This project aims at improving the performance of language-specific code generation by building a lightweight LLM for Rust language. The baseline model, i.e., CodeLlama-7b-Instruct, is instruct finetuned on the Rust dataset to improve the performance, as mainly CodeLlama models were trained on to learn programming languages like Python and C++. The limited availability of code corpora poses unique challenges in learning language-specific libraries and syntax.<p>
The fine-tuned Rust LLM is evaluated on Leetcode Top 150 problems and compared to the baseline CodeLlama-7B model. From the results, the fine-tuned Rust LLM was able to improve the acceptance and compilation of many leetcode problems that the baseline model suffered from.

# Project Structure
```
├── .github/workflows                           # config file for github workflows
│      
├── evaluation
│   ├── data
│   │   │   ├── baseline_code.json              # baseline model generate code
│   │   │   ├── baseline_eval.json              # baseline model evalation details
│   │   │   ├── finetuned_code.json             # finetuned model generate code
│   │   │   ├── finetuned_eval.json             # finetuned model evalation details
│   │   │   └── leetcode_problems.json          # leetcode problems details
│   │   │
│   ├── templates                               # template for generating site
│   ├── generate_static_site.py                 # generate static site using Flask Freeze 
│   ├── requirements.txt                        # Required libraries
│   └── server.py                               # Main Flask app
└── README.md                                   # Readme File
└── Rust_LLM.ipynb                              # Notebook for Finetuning LLM

```
# Dataset and Finetuned Model Link
[Dataset](https://huggingface.co/datasets/Neloy262/rust_instruction_dataset) &emsp;
[Rust LLM](https://huggingface.co/ripper479/rust_llm)
# Results
The results can be seen on the [Link](https://ripper479.github.io/rust-llm/).