<!-- ---
layout: page
--- -->


<!-- [click here for the most recent version of the paper]({{ BASE_PATH}}/pages/working_papers/sample-working-paper.pdf) -->


<!-- Note: this is how to write a comment in HTML. Everything in here won't show up on your webpage.-->

<!--
To increase the size of the title, use fewer # in front of the paper title.
To decrease the size of the title, use more #. 
To remove the italics, remove the * before and after the description
To remove the underline from the title, remove the <u> tags (<u> and </u>)
-->

### Introduction to Cognitive Neuroscience
---

<img src="https://raw.githubusercontent.com/Hosseinadeli/algonauts2023_transformers/main/figures/model_architecture.jpg" width = 400><img src="https://raw.githubusercontent.com/Hosseinadeli/algonauts2023_transformers/main/figures/02_hosseinadeli.png" width = 300>


A major goal of computational neuroscience is to model how different brain regions respond to visual input. Our approach here leverages transformer neural networks for both the visual features and the mapping from features to brain responses. The image features are extracted from a powerful transformer model trained with self-supervision (DINOv2; Oquab et al. 2023) that can capture object-centric representations without labels (Adeli et al. 2023). The decoder uses queries corresponding to different brain regions of interests (ROI) in different hemispheres to gather relevant information from the encoder output for predicting neural activity in each ROI. The output tokens from the decoder are then linearly mapped to the fMRI activity. We trained different versions of our model with inputs to the decoder coming from different layers of the encoder and combined the responses for our final prediction. Our model was tested on a held-out set of the NSD dataset (as part of the Algonauts2023 challenge; Gifford et al. 2023) and achieved a score of 63.5 on the challenge ROIs.

[Talk](https://www.youtube.com/live/9Xh55mcWJeE?si=K_Nqme9OYwBHj8eh&t=2302)

[biorxiv](https://www.biorxiv.org/content/10.1101/2023.08.02.551743v1.abstract)/ [pdf](https://www.biorxiv.org/content/10.1101/2023.08.02.551743v1.full.pdf) / [github](https://github.com/Hosseinadeli/algonauts2023_transformers)  

### Grouping and Object-based attention 
