# PCC
This is the official code repository for the paper "PCC: Paraphrasing with Bottom-k Sampling and Cyclic Learning for Curriculum Data Augmentation" accepted to EACL 2023 (main).

This is an early version that contains useful code and tips to reproduce our paper at EACL 2023.

# Code
We build our code for text classification on Wei et al., 2021 for few shot text classification which we used as a baseline in our paper: https://github.com/jasonwei20/triplet-loss
 
In our repository, you can find python files that is a modified version in their code repository. Replace the augmentation.py under utils/ and create an example like amzn json config under config/, then changing the augmentation file name to corresponding txt file can reproduce the results in the paper.

# Data
The augmentation file for few-shot text classification is under /data repository as txt files.

We also also provide .pkl file that contains paraphrases to reproduce our results for dialog generation, which contains a dictionary with the original traits as key and the paraphrase as values. We refer to using ParlAI to reproduce the results: https://parl.ai. 

To generate your own paraphrases, please refer to https://github.com/Advancing-Machine-Human-Reasoning-Lab/apt, which is the off-the-shelf paraphrase generation model we use.

Note that if you would like to use bottom-k sampling, remember to put constraints on the steps to apply bottom-k sampling. We plan to update the code shortly, but there should be just several lines, and you might find it easy to give some simple modification to the top-k sampling function.

# Citation 
Please cite our paper if you find the resource is useful:
```
@ARTICLE{2022arXiv220808110L,
       author = {{Lu}, Hongyuan and {Lam}, Wai},
        title = "{PCC: Paraphrasing with Bottom-k Sampling and Cyclic Learning for Curriculum Data Augmentation}",
      journal = {arXiv e-prints},
     keywords = {Computer Science - Computation and Language},
         year = 2022,
        month = aug,
          eid = {arXiv:2208.08110},
        pages = {arXiv:2208.08110},
          doi = {10.48550/arXiv.2208.08110},
archivePrefix = {arXiv},
       eprint = {2208.08110},
 primaryClass = {cs.CL},
       adsurl = {https://ui.adsabs.harvard.edu/abs/2022arXiv220808110L},
      adsnote = {Provided by the SAO/NASA Astrophysics Data System}
}
```
