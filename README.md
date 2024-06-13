# SIUO

[**🌐 Homepage**](https://sinwang20.github.io/SIUO/) | [**🤗 Dataset**](https://huggingface.co/datasets/MMMU/MMMU/) | [**🤗 Paper**](https://huggingface.co/papers/2311.16502) | [**📖 arXiv**](https://arxiv.org/pdf/2311.16502.pdf) | [**GitHub**](https://github.com/sinwang20/SIUO)


This repo contains the evaluation code for the paper "[Cross-Modality Safety Alignment](https://arxiv.org/pdf/2311.16502.pdf)"


## 🔔News

- **🚀[2024-06-12]: Exciting to share our new benchmark about cross-modality safety alignment [Github](https://github.com/sinwang20/SIUO)!🌟**


## Introduction
As Artificial General Intelligence (AGI) becomes increasingly integrated into various facets of human life, ensuring the safety and ethical alignment of such systems is paramount. Previous studies primarily focus on single-modality threats, which may not suffice given the integrated and complex nature of cross-modality interactions. We introduce a novel safety alignment challenge called <em>Safe Inputs but Unsafe Output (SIUO)</em> to evaluate cross-modality safety alignment. Specifically, it considers cases where single modalities are safe independently but could potentially lead to unsafe or unethical outputs when combined. To empirically investigate this problem, we developed the SIUO, a cross-modality benchmark encompassing 9 critical safety domains, such as self-harm, illegal activities, and privacy violations. Our findings reveal substantial safety vulnerabilities in both closed- and open-source LVLMs, such as GPT-4V and LLaVA, underscoring the inadequacy of current models to reliably interpret and respond to complex, real-world scenarios.

![Alt text](static/images/intro6.jpg)


## Dataset Creation

SIUO was created to challenge LVLMs with tasks that demand college-level subject knowledge and deliberate reasoning, pushing the boundaries of what these models can achieve in terms of expert-level perception and reasoning. Please refer to our huggingface [**🤗 Dataset**](https://huggingface.co/datasets/MMMU/MMMU/) for more details.


## Evaluation
Please refer to our [eval](eval)
 folder for more details.


## Contact
- Siyin Wang: siyinwang20@fudan.edu.cn
- Xipeng Qiu: xpqiu@fudan.edu.cn


## Papers citing(utilizing) SIUO

TBD

## Citation

**BibTeX:**
```bibtex
@inproceedings{yue2023mmmu,
  title={MMMU: A Massive Multi-discipline Multimodal Understanding and Reasoning Benchmark for Expert AGI},
  author={Xiang Yue and Yuansheng Ni and Kai Zhang and Tianyu Zheng and Ruoqi Liu and Ge Zhang and Samuel Stevens and Dongfu Jiang and Weiming Ren and Yuxuan Sun and Cong Wei and Botao Yu and Ruibin Yuan and Renliang Sun and Ming Yin and Boyuan Zheng and Zhenzhu Yang and Yibo Liu and Wenhao Huang and Huan Sun and Yu Su and Wenhu Chen},
  booktitle={Proceedings of CVPR},
  year={2024},
}
```

<!-- # Website License
<a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-sa/4.0/88x31.png" /></a><br />This work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/">Creative Commons Attribution-ShareAlike 4.0 International License</a>. -->
