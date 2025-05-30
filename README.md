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

| Prompt Strategy | Accuracy | F1 Score | Precision | Recall |
|----------------|----------|----------|-----------|--------|
| zero shot      | 0.27     | 0.20     | 0.34      | 0.20   |
| few shot (3)   | 0.54     | 0.49     | 0.49      | 0.55   |
| few shot (5)   | 0.59     | 0.53     | 0.53      | 0.60   |

### gemma

| Prompt Strategy | Accuracy | F1 Score | Precision | Recall |
|----------------|----------|----------|-----------|--------|
| zero shot      | 0.18     | 0.06     | 0.06      | 0.39   |
| few shot (3)   | 0.26     | 0.19     | 0.26      | 0.17   |
| few shot (5)   | 0.34     | 0.30     | 0.34      | 0.26   |

### deepseek

| Prompt Strategy | Accuracy | F1 Score | Precision | Recall |
|----------------|----------|----------|-----------|--------|
| zero shot      | 0.00     | 0.00     | 0.00      | 0.11   |
| few shot (3)   | 0.00     | 0.00     | 0.00      | 0.02   |
| few shot (5)   | 0.00     | 0.00     | 0.00      | 0.00   |

## Question 3 : Fine Tuning LLM for health applications.

| Model Name |Epochs| Accuracy | F1 Score | Precision | Recall |
|------------|------|----------|----------|-----------|--------|
| gemma      | 5    | 0.50     | 0.39     | 0.48      | 0.41   |
| llama      | 5    | 0.70     | 0.52     | 0.57      | 0.52   |
| deepseek   | 6    | 0.35     | 0.22     | 0.25      | 0.23   |


## Comparing the Models for few shot, zero shot and fine tuning

### llamma

| Model Name | Prompt Strategy | Accuracy | F1 Score | Precision | Recall |
|------------|----------------|----------|----------|-----------|--------|
| llama      | zero shot      | 0.27     | 0.20     | 0.34      | 0.20   |
| llama      | few shot (3)   | 0.54     | 0.49     | 0.49      | 0.55   |
| llama      | few shot (5)   | 0.59     | 0.53     | 0.53      | 0.60   |
| llama      | fine tuning    | 0.70     | 0.52     | 0.57      | 0.52   |

### gemma

|Model Name | Prompt Strategy | Accuracy | F1 Score | Precision | Recall |
|------------|----------------|----------|----------|-----------|--------|
| gemma      | zero shot      | 0.18     | 0.06     | 0.06      | 0.39   |
| gemma      | few shot (3)   | 0.26     | 0.19     | 0.26      | 0.17   |
| gemma      | few shot (5)   | 0.34     | 0.30     | 0.34      | 0.26   |
| gemma      | fine tuning    | 0.50     | 0.39     | 0.48      | 0.41   |

### deepseek

|Model Name | Prompt Strategy | Accuracy | F1 Score | Precision | Recall |
|-----------|----------------|----------|----------|-----------|--------|
| deepseek  | zero shot      | 0.00     | 0.00     | 0.00      | 0.11   |
| deepseek  | few shot (3)   | 0.00     | 0.00     | 0.00      | 0.02   |
| deepseek  | few shot (5)   | 0.       | 0.00     | 0.00      | 0.00   |
| deepseek  | fine tuning    | 0.35     | 0.22     | 0.25      | 0.23   |


### Note:
Even after multiple examples deepseek did not perform well for us. Even during Fine tuning it was not able to generalize well. After fine tuning for 6 epochs the accuracy was just 35% which is lower than few shot prompting of other models.