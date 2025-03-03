# Fine Tuning DeepSeek with Terraform Code
This project demonstrates how to fine-tune the innovative LLM model **DeepSeek** with open-sourced **terraform** codes and documentation so that it can effectively generate terraform codes. <br />
<img width="800" alt="image" src="https://github.com/user-attachments/assets/d991ebe5-21b9-4866-b3c4-ff1ca247a4b2" /> 

## 1. Collect & Prepare Terraform Data for Fine Tuning
Running [this notebook](https://github.com/Hiroaki0422/deepseek_terraform_finetune/blob/main/notebooks/terraform-data-collections.ipynb) will retrieve terraform code data from official documentation and prepare data for fine tuning 

## 2. Fine-tuning 
Training (fine tune) the base model `deepseek-coder-base-1.3B` and make it learn terraform codes from the output of the earlier. [this notebook](https://github.com/Hiroaki0422/deepseek_terraform_finetune/blob/main/notebooks/deepseek-terraform-fine-tune.ipynb) shows how to create a training pipeline.

## 3. Result
### Before Fine Tuning ###:
Prompt: Create a Terraform template with AWS Lambda function which reads S3\
Base model output: \
<img width="912" alt="image" src="https://github.com/user-attachments/assets/cd5e3ea6-91ae-4b94-9c62-ffbaad3ff1ec" /> \
Note: 
- the base DeepSeek model does not generate actual terraform codes.
- The solution does not provide IaC(Infrastructure-as-code) aspect of terraform \\

### After Fine Tuning ###:
Prompt: Create a Terraform template with AWS Lambda function which reads S3\
Base model output: \
<img width="797" alt="image" src="https://github.com/user-attachments/assets/047f49df-6d2e-4a98-81d3-cf429ab0ecfb" /> \
<img width="883" alt="image" src="https://github.com/user-attachments/assets/c3224e72-1279-4d69-8897-0e2ce467c571" /> \
<br />
Observe:
- The DeepSeek model can now effectively generate terraform data
- it is also able to generate parameters it has learned from terraform documentation

