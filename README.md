In this project, we attempt to fine-tune tge open source Llama-2 model (available on Vertex AI platform) using reinforcement learning with human feedback (RLHF) with the help of the RLHF pipeline also available on vertex AI and using a dataset of reddit posts.

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
