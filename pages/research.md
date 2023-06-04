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

### Object-based attention 
---

<img src="https://raw.githubusercontent.com/Hosseinadeli/affinity_attention/main/figures/sample_model_outputs/70158.png" width = 600>


A fundamental problem that our visual system must solve is how to group parts of the visual input together into coherent whole objects. 


[arxiv](https://arxiv.org/abs/2306.00294)/ [pdf](https://arxiv.org/pdf/2306.00294.pdf) / [github](https://github.com/Hosseinadeli/affinity_attention)  


### Sequential glimpse attention for multiobject recognition and visual reasoning
---


<img src="https://raw.githubusercontent.com/Hosseinadeli/hosseinadeli.github.io/main/assets/jov_OCRA.gif" width = 300><img src="https://raw.githubusercontent.com/Hosseinadeli/hosseinadeli.github.io/main/assets/OCRA_pipeline.jpg" width = 300>

The visual system uses sequences of selective glimpses to objects to support goal-directed behavior, but how is this attention control learned? Here we present an encoder–decoder model inspired by the interacting bottom-up and top-down visual pathways making up the recognition-attention system in the brain. At every iteration, a new glimpse is taken from the image and is processed through the “what” encoder, a hierarchy of feedforward, recurrent, and capsule layers, to obtain an object-centric (object-file) representation. This representation feeds to the “where” decoder, where the evolving recurrent representation provides top-down attentional modulation to plan subsequent glimpses and impact routing in the encoder. We demonstrate how the attention mechanism significantly improves the accuracy of classifying highly overlapping digits. In a visual reasoning task requiring comparison of two objects, our model achieves near-perfect accuracy and significantly outperforms larger models in generalizing to unseen stimuli. Our work demonstrates the benefits of object-based attention mechanisms taking sequential glimpses of objects.

* Adeli, H., Ahn, S., & Zelinsky, G. J. (2023). A brain-inspired object-based attention network for multiobject recognition and visual reasoning. Journal of Vision, 23(5), 16-16. [link](https://jov.arvojournals.org/article.aspx?articleid=2785636)/ [github](https://github.com/Hosseinadeli/OCRA)  
