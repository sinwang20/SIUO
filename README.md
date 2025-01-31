# SIUO

[**🌐 Homepage**](https://sinwang20.github.io/SIUO/) |  [**📖 arXiv**](https://arxiv.org/abs/2406.15279) | [**🤗 Paper**](https://huggingface.co/papers/2406.15279) | [**🤗 Dataset**](https://huggingface.co/datasets/sinwang/SIUO) | [**GitHub**](https://github.com/sinwang20/SIUO)


This repo contains the evaluation code for the paper "[Cross-Modality Safety Alignment](https://arxiv.org/abs/2406.15279)"


## 🔔News
- **🎉[2025-01-24]: Our SIUO is accepted by NAACL 2025!
- **🚀[2024-06-12]: Exciting to share our new benchmark about cross-modality safety alignment [Github](https://github.com/sinwang20/SIUO)!🌟**


## Introduction
As Artificial General Intelligence (AGI) becomes increasingly integrated into various facets of human life, ensuring the safety and ethical alignment of such systems is paramount. Previous studies primarily focus on single-modality threats, which may not suffice given the integrated and complex nature of cross-modality interactions. We introduce a novel safety alignment challenge called <em>Safe Inputs but Unsafe Output (SIUO)</em> to evaluate cross-modality safety alignment. Specifically, it considers cases where single modalities are safe independently but could potentially lead to unsafe or unethical outputs when combined. To empirically investigate this problem, we developed the SIUO, a cross-modality benchmark encompassing 9 critical safety domains, such as self-harm, illegal activities, and privacy violations. Our findings reveal substantial safety vulnerabilities in both closed- and open-source LVLMs, such as GPT-4V and LLaVA, underscoring the inadequacy of current models to reliably interpret and respond to complex, real-world scenarios.

![Alt text](static/images/intro6.jpg)


## 🧩 Dataset Creation

SIUO was created to challenge LVLMs with tasks that demand college-level subject knowledge and deliberate reasoning, pushing the boundaries of what these models can achieve in terms of expert-level perception and reasoning. 


### ✨ Dataset Examples

<img src="static/images/example2.jpg" class="floatpic">


### 🪜 Download
You can find the generation task questions in `data/siuo_gen.json` and the multiple-choice questions in `data/siuo_mcqa.json`.

Images can be downloaded from [Google Drive](https://drive.google.com/file/d/1U9CNRyMVlFRxMd8rT24SOQhK5G87-E2B/view?usp=sharing) or [Baidu Netdisk](https://pan.baidu.com/s/1AuFoOHjorGAjPu-4nrIL0Q?pwd=siuo)(code: `siuo`). You will obtain a zip file(`SIUO-images.zip`). Please unzip the images under `repo_root_dir/data/images`.



## 🎯 Evaluation

**SIUO** is a zero-shot evaluation benchmark. The model response generation process can be referred to in the following files: `generation—gpt4o-gen.py` and `generation-gpt4o-mcqa.py`.

### 🤖 GPT-Eval

1. Put your model's three responses as a list and add them under the "responses" field in `siuo_gen.json`, saved in `./eval/test_results/siuo_gen-{model_name}.json`.

2. For the safety evaluation, run `python gpt-eval.py --model model_name --mode safe` to obtain `./eval/test_results/siuo_gen-{model_name}-gpteval-safe-pro.json`.

    For the effectiveness evaluation, run `python gpt-eval.py --model model_name --mode effective` to obtain `./eval/test_results/siuo_gen-{model_name}-gpteval-effective-pro.json`.

    Note: Before running the `gpt-eval.py` file, you need to add your OpenAI API key.

3. Then run the file `python gpt-score.py`, which will merge the safe and effective files, calculate the values for safe, effective, and safe & effective scores. It will also statistically analyze the scores by category.

### 🤹 Multiple-Choice QA

1. Add the model response results under the "response_mcqa" field in `siuo_mcqa.json`, saved in `./eval/test_results/siuo_mcqa-{model_name}.json`.

2. Then run the file `python mcqa-eval.py --model model_name` to match the model responses and calculate accuracy.



## ✍️ Data Contribution

Anyone is welcome to contribute test cases to our dataset by submitting them through the [Google Form](https://docs.google.com/forms/d/e/1FAIpQLSd3qNg7j0BTlX71PJEgjstamWgh36oWKQIHQtJeCPJp3oFmgw/viewform?usp=sf_link). After a review by our team, we will incorporate the approved cases into the evaluation dataset. We greatly appreciate your participation in helping us advance cross-modality safety alignment, enabling a more comprehensive evaluation of these models.


## 📬 Contact
- Siyin Wang: siyinwang20@fudan.edu.cn
- Xipeng Qiu: xpqiu@fudan.edu.cn


## 👏 Papers citing(utilizing) SIUO

Welcome to cite/use our dataset to further advance cross-modality safety alignment.

## 🔒 License
![Data License](https://img.shields.io/badge/Data%20License-CC%20By%20NC%204.0-red.svg) **Usage and License Notices**: The dataset is intended and licensed for research use only. The dataset is CC BY NC 4.0 (allowing only non-commercial use) and models using the dataset should not be used outside of research purposes.


## 👋 Citation

**BibTeX:**

```bibtex
@article{wang2024cross,
  title={Cross-Modality Safety Alignment},
  author={Siyin Wang and Xingsong Ye and Qinyuan Cheng and Junwen Duan and Shimin Li and Jinlan Fu and Xipeng Qiu and Xuanjing Huang},
  journal={arXiv preprint arXiv:2406.15279},
  year={2024},
  url={https://arxiv.org/abs/2406.15279},
  archivePrefix={arXiv},
  eprint={2406.15279},
  primaryClass={cs.AI},
}
```
