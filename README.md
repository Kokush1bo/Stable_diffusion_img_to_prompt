# Stable_diffusion_img_to_prompt
This repository contains resources for generating prompts from stable diffusion images. 

Approach:
The idea was to have a CNN Encoder, for which i chose InceptionV3, pretrained model. Transformer based architecture is used to get best possible results. A RNN or LSTM
based model can also be chosen but Transformers are just great with NLP.So, an ecoder and decoder transformer was added. This gave us the predicted prompts. To convert
the prompts into embeddings, a sentence transformer can be used. I used MiniLM-L6-v2 which was recommended on Kaggle for converting prompts into embeddings vector of 384
size.

Data Acquisition:
Firstly i went with Diffusiondb dataset -> https://huggingface.co/datasets/poloclub/diffusiondb/tree/main
This was available on huggingface, it was great for this project but i had some trouble organising the data and had to leave the idea of using this dataset.
I tried many more datasets available and also tried to a=make my own dataset but time and limited computing resources did'nt permit to do so.
At the end i settled for COCO-2017 dataset which was also easily available on Kaggle.

I tried a lot of things for all the aspects of the project and finally settled with the current configuration and method.
