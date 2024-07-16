<div align="center">
    
 <div>
    <a href="https://github.com/yipoh/AesExpert"><img src="https://img.shields.io/github/stars/yipoh/AesExpert"/></a>
    <a href="https://arxiv.org/abs/2404.09624"><img src="https://img.shields.io/badge/Arxiv-2404:09624-red"/></a>
    <a href="https://huggingface.co/qyuan/AesMMIT_LLaVA_v1.5_7b_240325"><img src="https://img.shields.io/badge/%F0%9F%A4%97%20Hugging%20Face-Model%20Release-green"></a>
    <a href="https://pan.baidu.com/s/15vRoUcXBZodVWwkvfEJa9Q?pwd=h9vn"><img src="https://img.shields.io/badge/BaiduYun%20-Model%20Release-blue"></a>

   </div>

 <h1>AesExpert: Towards Multi-modality Foundation Model for Image Aesthetics Perception </h1>

  <div>
      <a href="https://github.com/yipoh" target="_blank">Yipo Huang</a><sup>1</sup>,
      <a href="https://github.com/yipoh/AesBench" target="_blank">Xiangfei Sheng</a><sup>1</sup>,
      <a href="https://github.com/zc-cpu" target="_blank">Zhichao Yang</a><sup>1</sup>,
      <a href="https://github.com/dylanqyuan" target="_blank">Quan Yuan</a><sup>1</sup>,
      <a href="https://github.com/yipoh/AesBench" target="_blank">Zhichao Duan</a><sup>1</sup>,
  </div>

   <div>
      <a href="https://faculty.xidian.edu.cn/chenpengfei/en/index.htm" target="_blank">Pengfei Chen</a><sup>1</sup>,
      <a href="https://scholar.google.com/citations?user=xMvuFI8AAAAJ&hl=en&oi=ao" target="_blank">Leida Li</a><sup>1</sup><sup>#</sup>,
      <a href="https://scholar.google.com/citations?user=D_S41X4AAAAJ&hl=en&oi=ao" target="_blank">Weisi Lin</a><sup>2</sup>,
      <a href="https://scholar.google.com/citations?hl=zh-CN&user=11aRt9oAAAAJ&view_op=list_works&sortby=pubdate" target="_blank">Guangming Shi</a><sup>1</sup>,
  </div>


  <div>
  <sup>1</sup>Xidian University, <sup>2</sup>Nanyang Technological University
       </div>   

<div>
<sup>#</sup>Corresponding author
   </div>


<h5 align="center"> If you like this work, please give us a star ⭐ on GitHub.  </h2>




</div>

 <br>

</h5>
</p> 
<p align="center">
    <img src="figs/teaserFig.png"/>
<p>
    <p align="center">Performance of the proposed AesExpert on various aesthetic perception dimensions, in comparison with the most advanced GPT-4V and Gemini-Pro-Vision, as well as the open-sourced LLaVA-1.5-13B.</p>
    </p> 
     </p> 
     </p> 

## News
- [2024/07/16] We have released AesMMIT(LLaVA-v1.5-7b) on [BaiduYun](https://pan.baidu.com/s/13yOBdLySG3U7kf-YgbTofw?pwd=25rx ) and [HuggingFace](https://huggingface.co/qyuan/AesMMIT_LLaVA_v1.5_7b_240325)! Check it out!🤗🤗🤗

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

