# 📘 Project Description

This repository contains a practical implementation of the experiments presented in the TCC:

> **"AVALIAÇÃO COMPARATIVA DE MODELOS DE IA ESPECIALIZADOS NA GERAÇÃO DE CÓDIGO: UM ESTUDO COM LLMS POPULARES DA HUGGING FACE"**

---

## 📂 About

This project consists of a Jupyter Notebook implementation designed to **test and evaluate code-generating LLMs** using models available on Hugging Face.

It leverages the [`lm-eval`](https://github.com/EleutherAI/lm-evaluation-harness) library for model evaluation.

---

## 🚀 How to Use

1. **Choose a model** from Hugging Face.
   The evaluation is done using the `hf-auto` loader from `lm_eval`, which automatically downloads and loads the model directly from Hugging Face (no manual download needed).

   ### ✅ Example:

   ```python
   model = "Qwen/Qwen2.5-Coder-0.5B-Instruct"
   ```

2. **Customize the evaluation tasks (optional):**
   You can modify the list of evaluation tasks by editing the `tasks` array in the notebook.

   To see the full list of available tasks, run:

   ```bash
   !python -m lm_eval --tasks list
   ```

   > ⚠️ Make sure `lm_eval` is installed, as shown in the first cell of the notebook.

   ### 🛠 Example task configuration:

   ```python
   tasks = [
       "global_mmlu_full_sv_machine_learning",
       "global_mmlu_full_sv_formal_logic",
       "global_mmlu_full_uk_college_computer_science",
       "global_mmlu_full_uk_computer_security",
       "humaneval_instruct",
       "humaneval_plus",
       "mbpp",
       "jsonschema_bench"
   ]
   ```

3. **Run the notebook** in any Jupyter environment (e.g., Jupyter Lab, VSCode, or [Google Colab](https://colab.google/)).

---

## 📊 Results

* The evaluation metrics will be **printed in the console**.
* Results are also **saved to CSV files** under the directory:

  ```
  ./results/<model_name>/results.csv
  ```

---

## 🔗 Useful Links

* [📘 lm-eval GitHub Repository](https://github.com/EleutherAI/lm-evaluation-harness)
* [🤗 Hugging Face (Models & Datasets)](https://huggingface.co/)
* [💻 Run the Notebook on Google Colab](https://colab.google/)

---

## ✅ Requirements

Make sure the required dependencies are installed, including:

* Python 3.8+
* `lm_eval` (see installation instructions in the notebook)

---