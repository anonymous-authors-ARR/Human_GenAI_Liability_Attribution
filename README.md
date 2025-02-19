# Human_GenAI_Liability_Attribution
Anonymized Supplementary Materials for the ARR submission: "Towards Law-informed Attribution of Human - Generative AI Liability"

Our "Code" folder includes 5 Jupyter Notebooks, which we originally run on Google Colab. You can re-run those notebooks in the following order: <br /> 
1/ ACL25__EDA_and_Preprocess_OpenAssistant__anonymized.ipynb <br /> 
-> to perform Exploratory Data Analysis (EDA) on the OpenAssistant dataset, and preprocess it to prepare fine-tuning (training) data. <br /> 
2/ ACL25__GPT2__Finetune__Compute_Perplexity__anonymized.ipynb OR ACL25__Zephyr__Finetune__Compute_Perplexity__anonymized.ipynb <br /> 
-> to finetune a base model (GPT-2, 1.5 billion parameters OR Zephyr, 7-billion parameters, alpha) on preprocessed OpenAssistant data, and then compute perplexity ratios between the fine-tuned vs. base model on FairPrism data. We default the number of fine-tuning epochs in this notebook to be 32 epochs, which you can change (e.g., to 4, 8, or 16 epochs). <br /> 
3/ ACL25__Plot_perplexity_ratios__GPT2_and_Zephyr__anonymized.ipynb <br /> 
-> to plot the perplexity ratios from the previous step on two histograms (one for harmful subset, the other for harmless subset of FairPrism). <br /> 
4/ ACL25__Compute_Wasserstein_distances__GPT2_and_Zephyr__anonymized.ipynb <br /> 
-> compute a direction-aware, scaled Wasserstein distance between two (harmful and harmless) distributions of perplexity ratios. <br /> 

Our "Processed_Data" folder includes saved perplexity ratios for the harmful and harmless subsets of FairPrism, evaluated by both fine-tuned models, GPT-2/Zephyr models.  <br /> 

Our figures folder includes the distributions of harmful and harmless perplexity ratios (plotted side by side), as well as the Wasserstein distance between those two distributions. We also plot for both fine-tuned models, GPT-2/Zephyr models. 


