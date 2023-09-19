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

### Predicting brain activity using Transformers
---

<img src="https://raw.githubusercontent.com/Hosseinadeli/algonauts2023_transformers/main/figures/model_architecture.jpg" width = 300><img src="https://raw.githubusercontent.com/Hosseinadeli/algonauts2023_transformers/main/figures/02_hosseinadeli.png" width = 300>


A major goal of computational neuroscience is to model how different brain regions respond to visual input. Our approach here leverages transformer neural networks for both the visual features and the mapping from features to brain responses. The image features are extracted from a powerful transformer model trained with self-supervision (DINOv2; Oquab et al. 2023) that can capture object-centric representations without labels (Adeli et al. 2023). The decoder uses queries corresponding to different brain regions of interests (ROI) in different hemispheres to gather relevant information from the encoder output for predicting neural activity in each ROI. The output tokens from the decoder are then linearly mapped to the fMRI activity. We trained different versions of our model with inputs to the decoder coming from different layers of the encoder and combined the responses for our final prediction. Our model was tested on a held-out set of the NSD dataset (as part of the Algonauts2023 challenge; Gifford et al. 2023) and achieved a score of 63.5 on the challenge ROIs.

[Talk](https://www.youtube.com/live/9Xh55mcWJeE?si=K_Nqme9OYwBHj8eh&t=2302)

[biorxiv](https://www.biorxiv.org/content/10.1101/2023.08.02.551743v1.abstract)/ [pdf](https://www.biorxiv.org/content/10.1101/2023.08.02.551743v1.full.pdf) / [github](https://github.com/Hosseinadeli/algonauts2023_transformers)  

### Grouping and Object-based attention 
---

<img src="https://raw.githubusercontent.com/Hosseinadeli/affinity_attention/main/figures/sample_model_outputs/70158.png" width = 600>


A fundamental problem that our visual system must solve is how to group parts of the visual input together into coherent whole objects. 


[arxiv](https://arxiv.org/abs/2306.00294)/ [pdf](https://arxiv.org/pdf/2306.00294.pdf) / [github](https://github.com/Hosseinadeli/affinity_attention)  


### Sequential glimpse attention for multiobject recognition and visual reasoning
---


<img src="https://raw.githubusercontent.com/Hosseinadeli/hosseinadeli.github.io/main/assets/OCRA_pipeline.jpg" width = 300>  &nbsp;   &nbsp;  &nbsp;  &nbsp;  <img src="https://raw.githubusercontent.com/Hosseinadeli/hosseinadeli.github.io/main/assets/jov_OCRA.gif" width = 200>
<br/>
<br/>
<br/>
<img src="https://raw.githubusercontent.com/Hosseinadeli/OCRA_samediff/main/figures/generated_10_time_steps_t3.gif" width = 550>  

The visual system uses sequences of selective glimpses to objects to support goal-directed behavior, but how is this attention control learned? Here we present an encoder–decoder model inspired by the interacting bottom-up and top-down visual pathways making up the recognition-attention system in the brain. At every iteration, a new glimpse is taken from the image and is processed through the “what” encoder, a hierarchy of feedforward, recurrent, and capsule layers, to obtain an object-centric (object-file) representation. This representation feeds to the “where” decoder, where the evolving recurrent representation provides top-down attentional modulation to plan subsequent glimpses and impact routing in the encoder. We demonstrate how the attention mechanism significantly improves the accuracy of classifying highly overlapping digits. In a visual reasoning task requiring comparison of two objects, our model achieves near-perfect accuracy and significantly outperforms larger models in generalizing to unseen stimuli. Our work demonstrates the benefits of object-based attention mechanisms taking sequential glimpses of objects.

* Adeli, H., Ahn, S., & Zelinsky, G. J. (2023). A brain-inspired object-based attention network for multiobject recognition and visual reasoning. Journal of Vision, 23(5), 16-16. [link](https://jov.arvojournals.org/article.aspx?articleid=2785636)/ [github](https://github.com/Hosseinadeli/OCRA)  


### A Computational Model of Attention in the Superior Colliculus 
---

<img src="https://raw.githubusercontent.com/Hosseinadeli/hosseinadeli.github.io/main/assets/MASC_method.png" width = 300><img src="https://raw.githubusercontent.com/Hosseinadeli/hosseinadeli.github.io/main/assets/MASC_free_viewing_scanpath.jpg" width = 300>

Modern image-based models of search prioritize fixation locations using target maps that capture visual evidence for a target goal. But while many such models are biologically plausible, none have looked to the oculomotor system for design inspiration or parameter specification. These models also focus disproportionately on specific target exemplars, ignoring the fact that many important targets are categories (e.g., weapons, tumors).  We introduce MASC, a Model of Attention in the Superior Colliculus (SC). MASC differs from other image-based models in that it is grounded in the neurophysiology of the SC, a mid-brain structure implicated in programming saccades—the behaviors to be predicted. It first creates a target map in one of two ways: by comparing a target image to objects in a search display (exemplar search), or by using a SVM-classifier trained on the target category to estimate the probability of search display objects being target category members (categorical search). 

* Adeli, H., Vitu, F., & Zelinsky, G. J. (2017). A model of the superior colliculus predicts fixation locations during scene viewing and visual search. Journal of Neuroscience, 37(6), 1453-1467.
* Vitu, F., Casteau, S., Adeli, H., Zelinsky, G. J., & Castet, E. (2017). The magnification factor accounts for the greater hypometria and imprecision of larger saccades: Evidence from a parametric human-behavioral study. Journal of Vision, 17(4):2, 1–38. [link][PDF]
