# PCC
This is the official code repository for the paper "PCC: Paraphrasing with Bottom-k Sampling and Cyclic Learning for Curriculum Data Augmentation" accepted to EACL 2023 (main).

This is a code repo and tips to reproduce our paper at EACL 2023.

# Code
We build our code for text classification on Wei et al., 2021 for few shot text classification which we used as a baseline in our paper: https://github.com/jasonwei20/triplet-loss
 
In our repository, you can find python files that is a modified version in their code repository. Replace the augmentation.py under utils/ and create an example like amzn json config under config/, then changing the augmentation file name to corresponding txt file can reproduce the results in the paper.

# Data
The augmentation file for few-shot text classification is under /data repository as txt files.

We also also provide .pkl file that contains paraphrases to reproduce our results for dialog generation, which contains a dictionary with the original traits as key and the paraphrase as values. We refer to using ParlAI to reproduce the results: https://parl.ai. 

To generate your own paraphrases, please refer to https://github.com/Advancing-Machine-Human-Reasoning-Lab/apt, which is the off-the-shelf paraphrase generation model we use.

Note that if you would like to use bottom-k sampling, remember to put constraints on the steps to apply bottom-k sampling. You might find it easy to give some simple modification to the top-k sampling function.

# Citation 
Please cite our paper if you find the resource is useful:

Hongyuan Lu and Wai Lam. 2023. PCC: Paraphrasing with Bottom-k Sampling and Cyclic Learning for Curriculum Data Augmentation. In Proceedings of the 17th Conference of the European Chapter of the Association for Computational Linguistics, pages 68–82, Dubrovnik, Croatia. Association for Computational Linguistics.

```
@inproceedings{lu-lam-2023-pcc,
    title = "{PCC}: Paraphrasing with Bottom-k Sampling and Cyclic Learning for Curriculum Data Augmentation",
    author = "Lu, Hongyuan  and
      Lam, Wai",
    booktitle = "Proceedings of the 17th Conference of the European Chapter of the Association for Computational Linguistics",
    month = may,
    year = "2023",
    address = "Dubrovnik, Croatia",
    publisher = "Association for Computational Linguistics",
    url = "https://aclanthology.org/2023.eacl-main.5",
    pages = "68--82",
    abstract = "Curriculum Data Augmentation (CDA) improves neural models by presenting synthetic data with increasing difficulties from easy to hard. However, traditional CDA simply treats the ratio of word perturbation as the difficulty measure and goes through the curriculums only once. This paper presents \textbf{PCC}: \textbf{P}araphrasing with Bottom-k Sampling and \textbf{C}yclic Learning for \textbf{C}urriculum Data Augmentation, a novel CDA framework via paraphrasing, which exploits the textual paraphrase similarity as the curriculum difficulty measure. We propose a curriculum-aware paraphrase generation module composed of three units: a paraphrase candidate generator with bottom-k sampling, a filtering mechanism and a difficulty measure. We also propose a cyclic learning strategy that passes through the curriculums multiple times. The bottom-k sampling is proposed to generate super-hard instances for the later curriculums. Experimental results on few-shot text classification as well as dialogue generation indicate that PCC surpasses competitive baselines. Human evaluation and extensive case studies indicate that bottom-k sampling effectively generates super-hard instances, and PCC significantly improves the baseline dialogue agent.",
}
```
