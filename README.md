<h1>AesExpert </h1>

_Let MLLM perceive image aesthetics like humans. Try it now!_


 <div>
    <a href="https://yipoh.github.io/aes-expert/"><img src="https://img.shields.io/badge/Homepage-AesExpert-pink"/></a>
    <a href="https://arxiv.org/abs/2404.09624"><img src="https://img.shields.io/badge/Arxiv-2404:09624-red"/></a>
    <a href="https://huggingface.co/qyuan/AesMMIT_LLaVA_v1.5_7b_240325"><img src="https://img.shields.io/badge/%F0%9F%A4%97%20Hugging%20Face-Model%20Release-green"></a>
    <a href="https://pan.baidu.com/s/15vRoUcXBZodVWwkvfEJa9Q?pwd=h9vn"><img src="https://img.shields.io/badge/BaiduYun%20-Model%20Release-blue"></a>
    <a href="https://pan.baidu.com/s/1QL547GVxzL9VbPJYtpK8OA?pwd=aesm"><img src="https://img.shields.io/badge/%F0%9F%A4%97%20Hugging%20Face-Dataset%20Release-green"></a>
    <a href="https://pan.baidu.com/s/1QL547GVxzL9VbPJYtpK8OA?pwd=aesm"><img src="https://img.shields.io/badge/BaiduYun%20-Dataset%20Release-blue"></a>
    <a href="https://fb3a-113-200-174-24.ngrok-free.app/"><img src="https://img.shields.io/badge/Chatbot%20-AesExpert-yellow"></a>

   </div>

<h5> If you like this work, please give us a star ⭐ on GitHub.  </h2>


<h1>Introduction</h1> 
</div>

 <br>

</h5>
</p> 
<p align="center">
    <img src="figs/teaserFig.png"/>
<p>
    <p align="justify">The highly abstract nature of image aesthetics perception (IAP) poses significant challenge for current multimodal large language models (MLLMs). 
          The lack of human-annotated multi-modality aesthetic data further exacerbates this dilemma, resulting in MLLMs falling short of aesthetics perception capabilities. 
          To address the above challenge, we first introduce a comprehensively annotated Aesthetic Multi-Modality Instruction Tuning (AesMMIT) dataset, which serves as the footstone for building multi-modality aesthetics foundation models. 
          Specifically, to align MLLMs with human aesthetics perception, we construct a corpus-rich aesthetic critique database with 21,904 diverse-sourced images and 88K human natural language feedbacks, which are collected via progressive questions, ranging from coarse-grained aesthetic grades to fine-grained aesthetic descriptions. 
          To ensure that MLLMs can handle diverse queries, we further prompt GPT to refine the aesthetic critiques and assemble the large-scale aesthetic instruction tuning dataset, <i>i.e.</i> AesMMIT, which consists of 409K multi-typed instructions to activate stronger aesthetic capabilities. 
          Based on the AesMMIT database, we fine-tune the open-sourced general foundation models, achieving multi-modality Aesthetic Expert models, dubbed AesExpert. 
          Extensive experiments demonstrate that the proposed AesExpert models deliver significantly better aesthetic perception performances than the state-of-the-art MLLMs, including the most advanced GPT-4V and Gemini-Pro-Vision.</p>

## News
- [2025/01/12] We have released AesMMIT dataset on [BaiduYun](https://pan.baidu.com/s/1QL547GVxzL9VbPJYtpK8OA?pwd=aesm) and [HuggingFace](https://pan.baidu.com/s/1QL547GVxzL9VbPJYtpK8OA?pwd=aesm)! 🤗🤗🤗
- [2024/07/20] Welcome to our [Project Page](https://yipoh.github.io/aes-expert/)! 🔥🔥🔥
- [2024/07/16] We have released AesExpert (LLaVA-v1.5-7b) on [BaiduYun](https://pan.baidu.com/s/13yOBdLySG3U7kf-YgbTofw?pwd=25rx ) and [HuggingFace](https://huggingface.co/qyuan/AesMMIT_LLaVA_v1.5_7b_240325)! Check it out!🤗🤗🤗

## Quick Start

### LLaVA-v1.5

#### Install LLaVA.

```shell
git clone https://github.com/haotian-liu/LLaVA.git
cd LLaVA
pip install -e .
```

#### Simple Interactive Demos.

*See the codes and scripts below.*

<details>
<summary>Example Code (Single Query)</summary>
    
```python
from llava.mm_utils import get_model_name_from_path
from llava.eval.run_llava import eval_model
model_path = "qyuan/AesMMIT_LLaVA_v1.5_7b_240325" 
prompt = "Describe the aesthetic experience of this image in detail."
image_file = "figs/demo1.jpg"
args = type('Args', (), {
    "model_path": model_path,
    "model_base": None,
    "model_name": get_model_name_from_path(model_path),
    "query": prompt,
    "conv_mode": None,
    "image_file": image_file,
    "sep": ",",
})()
eval_model(args)
```
</details>


## Acknowledgement
We thank [Teo Wu](https://github.com/teowu) and [Zicheng Zhang](https://github.com/zzc-1998) for their awesome works [Q-Future](https://github.com/Q-Future).

## Citation

If you find our work interesting, please feel free to cite our paper:

```bibtex
@article{AesExpert,
    title={AesExpert: Towards Multi-modality Foundation Model for Image Aesthetics Perception},
    author={Yipo Huang and Xiangfei Sheng and Zhichao Yang and Quan Yuan and Zhichao Duan and Pengfei Chen and Leida Li and Weisi Lin and Guangming Shi},
   journal={arXiv:2404.09624},
    year={2024},
}
```


