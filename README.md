# AISG_Assignment-2

This repo contains the below files:
* gemma.ipynb : This file contains the code for finetuning gemma model. 
* llama.ipynb : This file contains the code for finetuning Llama model.
* deepseek.ipyn : This file contains the code for fine tuning deepseek model.
* ZeroShot-FewShot_llama.ipynb : This files contains the zero shot and few shot comparision of llama model
* ZeroShot-FewShot_gemma.ipynb : This files contains the zero shot and few shot comparision of gemma model
* ZeroShot-FewShot_deepseek.ipynb : This files contains the zero shot and few shot comparision of deepseek model

This repo contains the below folders:
* modelname-lora-medical : The model-name could be gemma, llama, deepseek. These folders contain the model checkpoints.
* medical-cases-train/test/validation : Contains the dataset stored in folders
* unsloth_compiled_cache : cache folder that is used by unsloth for finetuning purposes.


## Question 1 and 2: Zero Shot and Few Shot Prompting.


### llama

| Promt Strategy | Accuracy | F1 Score | Precision | Recall |
|----------------|----------|----------|-----------|--------|
| zero shot      | 0.27     | 0.20     | 0.34      | 0.20   |
| few shot (3)   | 0.     | 0.     | 0.      | 0.   |
| few shot (5)   | 0.59     | 0.53     | 0.53      | 0.60   |

### gemma

| Promt Strategy | Accuracy | F1 Score | Precision | Recall |
|----------------|----------|----------|-----------|--------|
| zero shot      | 0.       | 0.     | 0.      | 0.   |
| few shot (3)   | 0.       | 0.     | 0.      | 0.   |
| few shot (5)   | 0.       | 0.     | 0.      | 0.   |

### deepseek

| Promt Strategy | Accuracy | F1 Score | Precision | Recall |
|----------------|----------|----------|-----------|--------|
| zero shot      | 0.       | 0.     | 0.      | 0.   |
| few shot (3)   | 0.       | 0.     | 0.      | 0.   |
| few shot (5)   | 0.       | 0.     | 0.      | 0.   |

## Question 3 : Fine Tuning LLM for health applications.

| Model Name | Accuracy | F1 Score | Precision | Recall |
|------------|----------|----------|-----------|--------|
| gemma      | 0.50     | 0.39     | 0.48      | 0.41   |
| llama      | 0.70     | 0.52     | 0.57      | 0.52   |
| deepseek   | 0.0     | 0.     | 0.      | 0.   |