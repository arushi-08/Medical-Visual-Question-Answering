# Transfer learning for Medical Visual Question Answering

## Experimental Setup
Install [Miniforge](https://github.com/conda-forge/miniforge?tab=readme-ov-file#install) ([Mamba](https://mamba.readthedocs.io/en/latest/installation/mamba-installation.html)).

Create conda environment:

    conda env create -f environment.yml
    conda activate med_vqa


## Models

Image Encoders
CLIP: Utilized pretrained CLIP models with Vision Transformer (ViT) architecture, specifically ViT-L-14.
PMC-CLIP: Built from pretraining CLIP ViT image encoder on 1.6M medical image-caption pairs in the PMC-OA dataset【lin2023pmcclip】.
Text Encoders and Decoders
LLaMA-2
PMC-LLaMA: Developed from fine-tuning the LLaMA 13B model on 4.8M biomedical academic papers and 30K medical textbooks【wu2024pmc】.
Combinations Explored
1. CLIP + LLaMA-2
2. CLIP + PMC-LLaMA
3. PMC-CLIP + LLaMA-2
4. PMC-CLIP + PMC-LLaMA
