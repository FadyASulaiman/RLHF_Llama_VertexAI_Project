## Project Introduction

In this project, we attempt to fine-tune the open source Llama-2 model (available on Vertex AI platform) on text-summarization tasks using reinforcement learning with human feedback (RLHF) with the help of the RLHF pipeline also available on vertex AI and using a dataset of reddit posts.

---

## Technical Concepts:

### RLHF:
**RLHF** is a training approach that optimizes language models to align with human preferences. It involves three key components: a pretrained language model, a reward model trained on human preference data, and a policy optimization step (typically using PPO) that fine-tunes the original model to maximize the reward model's scores. 

The process essentially creates a feedback loop where the model learns to generate outputs that humans would rate highly, making it particularly effective for improving model safety, reducing harmful outputs, and enhancing the quality of responses.

### PPO:
**PPO (Proximal Policy Optimization)** is a reinforcement learning algorithm that optimizes a policy (in this case, the language model's behavior) while preventing too large policy updates. It works by:
- Setting a ratio between new and old policies
- Clipping this ratio to stay within a small interval (typically 0.8 to 1.2)
- Taking the minimum of the clipped and unclipped objective

This conservative update approach helps prevent the model from taking destructive large steps that could collapse its performance.

---

## Project Structure

The project is structured on three main notebooks, numbered 1-3, where in the first we explore the dataset, in the second we tune the model and in the third we evaluate the tuned model.

---

## Dataset

The dataset used to tune the model can be found here: [Reddit posts](https://github.com/openai/summarize-from-feedback)

---

### Dependencies:

This project relies on GCP's vertex AI tools and pipelines.

To Install the dependencies ffor the 'tuning_llama' notebook run:
```
!pip3 install google-cloud-pipeline-components
!pip3 install kfp
!pip3 install google-cloud-aiplatform
```

To Install the dependencies for the 'evaluating_tuned_llama' notebook run:

```
pip install tensorboard
```
