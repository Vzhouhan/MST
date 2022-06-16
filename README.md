# Mask-guided Spectral-wise Transformer for Efficient Hyperspectral Image Reconstruction (CVPR 2022)
[![winner](https://img.shields.io/badge/MST++-Winner_of_NTIRE_2022_Challenge_on_Spectral_Reconstruction_from_RGB-179bd3)](https://github.com/caiyuanhao1998/MST-plus-plus/)
[![arXiv](https://img.shields.io/badge/arxiv-paper-179bd3)](https://arxiv.org/abs/2111.07910)
[![zhihu](https://img.shields.io/badge/zhihu-知乎中文解读-179bd3)](https://zhuanlan.zhihu.com/p/501101943)
![visitors](https://visitor-badge.glitch.me/badge?page_id=caiyuanhao1998/MST)

[Yuanhao Cai](caiyuanhao1998.github.io), [Jing Lin](https://scholar.google.com/citations?hl=zh-CN&user=SvaU2GMAAAAJ), Xiaowan Hu, [Haoqian Wang](https://scholar.google.com.hk/citations?user=eldgnIYAAAAJ&hl=zh-CN), [Xin Yuan](https://xygroup6.github.io/xygroup/), [Yulun Zhang](yulunzhang.com), [Radu Timofte](https://people.ee.ethz.ch/~timofter/), and [Luc Van Gool](https://ee.ethz.ch/the-department/faculty/professors/person-detail.OTAyMzM=.TGlzdC80MTEsMTA1ODA0MjU5.html)

*The first two authors contribute equally to this work*


#### News
- **2022.06.14 :** Code and models have been released. This repo supports 12 learning-based methods to serve as a baseline for Spectral Compressive Imaging. The model zoo will be enlarged. 🔥
- **2022.05.20 :** Our work [DAUHST](https://arxiv.org/abs/2205.10102) is on arxiv. Code and models are coming soon. :dizzy:
- **2022.04.02 :** Further work [MST++](https://github.com/caiyuanhao1998/MST-plus-plus/) has won the NTIRE 2022 Spectral Reconstruction Challenge. :trophy: 
- **2022.03.09 :** Our work [CST](https://arxiv.org/abs/2203.04845) is on arxiv. Code and models are coming soon. :dizzy:
- **2022.03.02 :** Our paper has been accepted by CVPR 2022, code and models are coming soon. :rocket: 

|            *Scene 2*             |             *Scene 3*             |             *Scene 4*             |             *Scene 7*             |
| :------------------------------: | :-------------------------------: | :-------------------------------: | :-------------------------------: |
| <img src="./figure/frame2channel12.gif"  height=170 width=170> | <img src="./figure/frame3channel21.gif" width=170 height=170> | <img src="./figure/frame4channel28.gif" width=170 height=170> |  <img src="./figure/frame7channel4.gif" width=170 height=170> |

<hr />

> **Abstract:** *Hyperspectral image (HSI) reconstruction aims to recover the 3D spatial-spectral signal from a 2D measurement in the coded aperture snapshot spectral imaging  (CASSI) system. The HSI  representations are highly similar and correlated across the spectral dimension. Modeling the inter-spectra interactions is beneficial for HSI reconstruction. However, existing CNN-based methods show limitations in capturing spectral-wise similarity and long-range dependencies. Besides, the HSI information is modulated by a coded aperture (physical mask) in CASSI. Nonetheless, current algorithms have not fully explored the guidance effect of the mask for HSI restoration. In this paper, we propose a novel framework, Mask-guided Spectral-wise Transformer (MST), for HSI reconstruction. Specifically, we present a Spectral-wise Multi-head Self-Attention (S-MSA) that treats each spectral feature as a token and calculates self-attention along the spectral dimension. In addition, we customize a Mask-guided Mechanism (MM) that directs S-MSA to pay attention to spatial regions with high-fidelity spectral representations. Extensive experiments show that our MST significantly outperforms state-of-the-art (SOTA) methods on simulation and real HSI datasets while requiring dramatically cheaper computational and memory costs.* 
<hr />

## Diagram of Our Method
![Illustration of MST](/figure/MST.png)


## Comparison with State-of-the-art Methods
This repo is a baseline and toolbox containing 12 learning-based algorithms for spectral compressive imaging.

We are going to enlarge our model zoo in the future.


<details close>
<summary><b>Supported algorithms:</b></summary>

* [x] [MST](https://arxiv.org/abs/2111.07910) (CVPR 2022)
* [x] [MST++](https://arxiv.org/abs/2111.07910) (CVPRW 2022)
* [x] [HDNet](https://arxiv.org/abs/2203.02149) (CVPR 2022)
* [x] [BIRNAT](https://ieeexplore.ieee.org/abstract/document/9741335/) (TPAMI 2022)
* [x] [DGSMP](https://arxiv.org/abs/2103.07152) (CVPR 2021)
* [x] [GAP-Net](https://arxiv.org/abs/2012.08364) (Arxiv 2020)
* [x] [TSA-Net](https://link.springer.com/chapter/10.1007/978-3-030-58592-1_12) (ECCV 2020)
* [x] [ADMM-Net](https://openaccess.thecvf.com/content_ICCV_2019/html/Ma_Deep_Tensor_ADMM-Net_for_Snapshot_Compressive_Imaging_ICCV_2019_paper.html) (ICCV 2019)
* [x] [λ-Net](https://ieeexplore.ieee.org/document/9010044) (ICCV 2019)
* [ ] [SRN](http://128.84.4.34/abs/2108.07739) (Arxiv 2021)
* [ ] [DAUHST](https://arxiv.org/abs/2205.10102) (Arxiv 2022)
* [ ] [CST](https://arxiv.org/abs/2203.04845) (Arxiv 2022)


</details>

![comparison_fig](/figure/compare_fig.png)

### Quantitative Comparison on Simulation Dataset

|                            Method                            | Params (M) | FLOPS (G) | PSNR  | SSIM  |                          Model Zoo                           |                      Simulation  Result                      |                         Real  Result                         |
| :----------------------------------------------------------: | :--------: | :-------: | :---: | :---: | :----------------------------------------------------------: | :----------------------------------------------------------: | :----------------------------------------------------------: |
|    [λ-Net](https://ieeexplore.ieee.org/document/9010044)     |   62.64    |  117.98   | 28.53 | 0.841 | [Google Drive](https://drive.google.com/drive/folders/11DwTFdgtG7sRnBwvkxxfN9rcOICsEdpC?usp=sharing) / [Baidu Disk](https://pan.baidu.com/s/1xXkL2p4_mCLeTGa68wEbNQ?pwd=mst1) | [Google Drive](https://drive.google.com/drive/folders/1csOZ2Kfto_tWIiSD0hc2nzKjR4Ze7ftA?usp=sharing) / [Baidu Disk](https://pan.baidu.com/s/1-0LjvHnkINW8YYaBiA4-VA?pwd=mst1) |                                                              |
| [TSA-Net](https://link.springer.com/chapter/10.1007/978-3-030-58592-1_12) |   44.25    |  110.06   | 31.46 | 0.894 | [Google Drive](https://drive.google.com/drive/folders/1f29eS8WqXu31310nD-7mRR81XfLBYKBd?usp=sharing) / [Baidu Disk](https://pan.baidu.com/s/1riGZ83AXXkcjHiGVNrNeYg?pwd=mst1) | [Google Drive](https://drive.google.com/drive/folders/1BOXBIu2Ze-L__XuLRUu4y9-lq0fw2FJd?usp=sharing) / [Baidu Disk](https://pan.baidu.com/s/1icqxYnsD27zrDQ95STfRvw?pwd=mst1) |                                                              |
|          [DGSMP](https://arxiv.org/abs/2103.07152)           |    3.76    |  646.65   | 32.63 | 0.917 | [Google Drive](https://drive.google.com/drive/folders/1j1k8mYKWh8FVe77Cz8hj69nI2lK2D5QC?usp=sharing) / [Baidu Disk](https://pan.baidu.com/s/1v-uqYJZ5mQxOupLc6E_C1g?pwd=mst1) | [Google Drive](https://drive.google.com/drive/folders/1PjnTYEEDfWlTpe0jzCmImxxXLfy5Viva?usp=sharing) / [Baidu Disk](https://pan.baidu.com/s/1Y1AJICGUqUJEV-74Eg2FEg?pwd=mst1) |                                                              |
|         [GAP-Net](https://arxiv.org/abs/2012.08364)          |    4.27    |   78.58   | 33.26 | 0.917 | [Google Drive](https://drive.google.com/drive/folders/1AF3P42DZtBzKpWvjTVKYoLmGHsL2f_SL?usp=sharing) / [Baidu Disk](https://pan.baidu.com/s/1hraGGd_HEsfCkSGv5QyOaw?pwd=mst1) | [Google Drive](https://drive.google.com/drive/folders/16_kqEj4nlE_KlHzu8Q6zQCizTTBII82F?usp=sharing) / [Baidu Disk](https://pan.baidu.com/s/12azFFSEOic7iNTFGmC7wMw?pwd=mst1) |                                                              |
| [ADMM-Net](https://openaccess.thecvf.com/content_ICCV_2019/html/Ma_Deep_Tensor_ADMM-Net_for_Snapshot_Compressive_Imaging_ICCV_2019_paper.html) |    4.27    |   78.58   | 33.58 | 0.918 | [Google Drive](https://drive.google.com/drive/folders/1I9JqdyikulUVjXcdciHaJxfAceqfaF2G?usp=sharing) / [Baidu Disk](https://pan.baidu.com/s/1ddkA9TazTq0rZReFYgGHMg?pwd=mst1) | [Google Drive](https://drive.google.com/drive/folders/1WT0QYfC5dbigl9znD_JFNHpH0k_rTDc-?usp=sharing) / [Baidu Disk](https://pan.baidu.com/s/1b2sRrJaS3PKYqqQErmtIJg?pwd=mst1) |                                                              |
| [BIRNAT](https://ieeexplore.ieee.org/abstract/document/9741335/) |    4.40    |  2122.66  | 37.58 | 0.960 | [Google Drive](https://drive.google.com/drive/folders/1bwhy0csM6GSNY0Qe9RS7_U3Bm9JJjHoc?usp=sharing) / [Baidu Disk](https://pan.baidu.com/s/1HDMQu3jWvQ9X1yQA5dprGg?pwd=mst1) | [Google Drive](https://drive.google.com/drive/folders/1fp4-D1-RGx9bICSmzpIiKBRAEmDOE3gD?usp=sharing) / [Baidu Disk](https://pan.baidu.com/s/1pHfEKypguCLydNsmCGojpw?pwd=mst1) |                                                              |
|          [HDNet](https://arxiv.org/abs/2203.02149)           |    2.37    |  154.76   | 34.97 | 0.943 | [Google Drive](https://drive.google.com/drive/folders/1F41BlUQulzPCf5yNo-q6V6Mdtr7bPV6-?usp=sharing) / [Baidu Disk](https://pan.baidu.com/s/1mCoGHT22cw7ElVSaXgU5Lw?pwd=mst1) | [Google Drive](https://drive.google.com/drive/folders/1oUrgFUWIKR-96zAT2Y42UlAM6l5NVJsf?usp=sharing) / [Baidu Disk](https://pan.baidu.com/s/1Nb5IE02iAClMBC4OHcnePQ?pwd=mst1) | [Google Drive](https://drive.google.com/file/d/1vLAMTAi1BvL1lskvjqBJEyBEvSIqu-kV/view?usp=sharing) / [Baidu Disk](https://pan.baidu.com/s/1PA5GRXqoAnYUkEUgtPtXtQ?pwd=mst1) |
|          [MST-S](https://arxiv.org/abs/2111.07910)           |    0.93    |   12.96   | 34.26 | 0.935 | [Google Drive](https://drive.google.com/drive/folders/176f_PammL0ZrIg3lVaQwd6Vr6Ui8FANs?usp=sharing) / [Baidu Disk](https://pan.baidu.com/s/1ZQ08_Ec3a_-8YYAa5ms5PQ?pwd=mst1) | [Google Drive](https://drive.google.com/drive/folders/1afMG9PndlvjDTtl7UJZoElmDe5FtpCoW?usp=sharing) / [Baidu Disk](https://pan.baidu.com/s/1xzJRVjnI-7A54Rj_zi3crA?pwd=mst1) | [Google Drive](https://drive.google.com/file/d/1HTDXpPW0yOy4zRpPk3Wgw5DYVwhZUr2g/view?usp=sharing) / [Baidu Disk](https://pan.baidu.com/s/137SBN6yL3irU-5ZIhMQ_Hg?pwd=mst1) |
|          [MST-M](https://arxiv.org/abs/2111.07910)           |    1.50    |   18.07   | 34.94 | 0.943 | [Google Drive](https://drive.google.com/drive/folders/176f_PammL0ZrIg3lVaQwd6Vr6Ui8FANs?usp=sharing) / [Baidu Disk](https://pan.baidu.com/s/1ZQ08_Ec3a_-8YYAa5ms5PQ?pwd=mst1) | [Google Drive](https://drive.google.com/drive/folders/1hnEuwYO9luwLmPeT98cUaik_zCPK6z30?usp=sharing) / [Baidu Disk](https://pan.baidu.com/s/1OUuozfd3zLqzBjHnf6evCQ?pwd=mst1) | [Google Drive](https://drive.google.com/file/d/1HTDXpPW0yOy4zRpPk3Wgw5DYVwhZUr2g/view?usp=sharing) / [Baidu Disk](https://pan.baidu.com/s/137SBN6yL3irU-5ZIhMQ_Hg?pwd=mst1) |
|          [MST-L](https://arxiv.org/abs/2111.07910)           |    2.03    |   28.15   | 35.18 | 0.948 | [Google Drive](https://drive.google.com/drive/folders/176f_PammL0ZrIg3lVaQwd6Vr6Ui8FANs?usp=sharing) / [Baidu Disk](https://pan.baidu.com/s/1ZQ08_Ec3a_-8YYAa5ms5PQ?pwd=mst1) | [Google Drive](https://drive.google.com/drive/folders/18ZF5wC1LRmqOh6VDeXD4eB8mP0Dvv6jb?usp=sharing) / [Baidu Disk](https://pan.baidu.com/s/1imed0w1CWqx7IOlSpVh7qw?pwd=mst1) | [Google Drive](https://drive.google.com/file/d/1HTDXpPW0yOy4zRpPk3Wgw5DYVwhZUr2g/view?usp=sharing) / [Baidu Disk](https://pan.baidu.com/s/137SBN6yL3irU-5ZIhMQ_Hg?pwd=mst1) |
|          [MST++](https://arxiv.org/abs/2111.07910)           |    1.33    |   19.42   | 35.99 | 0.951 | [Google Drive](https://drive.google.com/drive/folders/1rbV8LYD5k1RVR4usMORoXxY2szlFsr_9?usp=sharing) / [Baidu Disk](https://pan.baidu.com/s/1QUx_MpYCBSU4Zas5gpao2g?pwd=mst1) | [Google Drive](https://drive.google.com/drive/folders/14sz-y99fEAJDQAN1itE5K-BlMHC1Tt3z?usp=sharing) / [Baidu Disk](https://pan.baidu.com/s/1s3btC7QQrasW1NqFzOm8fQ?pwd=mst1) | [Google Drive](https://drive.google.com/file/d/1Ezz-kpyy2gaEfEASQ1w6U68_wsk3VJJZ/view?usp=sharing) / [Baidu Disk](https://pan.baidu.com/s/1WsrSlJsntJQ0MQ8OHTN7hg?pwd=mst1) |

The performance are reported on 10 scenes of the KAIST dataset. The test size of FLOPS is 256 x 256.

Note: access code for `Baidu Disk` is `mst1`

## 1. Create Environment:

- Python 3 (Recommend to use [Anaconda](https://www.anaconda.com/download/#linux))

- NVIDIA GPU + [CUDA](https://developer.nvidia.com/cuda-downloads)

- Python packages:

```shell
pip install -r requirements.txt
```

## 2. Prepare Dataset:

Download cave_1024_28 ([One Drive](https://bupteducn-my.sharepoint.com/:f:/g/personal/mengziyi_bupt_edu_cn/EmNAsycFKNNNgHfV9Kib4osB7OD4OSu-Gu6Qnyy5PweG0A?e=5NrM6S)), CAVE_512_28 ([Baidu Disk](https://pan.baidu.com/s/1ue26weBAbn61a7hyT9CDkg), code: `ixoe`), KAIST_CVPR2021 ([Baidu Disk](https://pan.baidu.com/s/1LfPqGe0R_tuQjCXC_fALZA), code: `5mmn`), TSA_simu_data ([One Drive](https://1drv.ms/u/s!Au_cHqZBKiu2gYFDwE-7z1fzeWCRDA?e=ofvwrD)), TSA_real_data ([One Drive](https://1drv.ms/u/s!Au_cHqZBKiu2gYFTpCwLdTi_eSw6ww?e=uiEToT)), and then put them into the corresponding folders of `datasets/` and recollect them as the following form:

```shell
|--MST
    |--real
    	|-- test_code
    	|-- train_code
    |--simulation
    	|-- test_code
    	|-- train_code
    |--visualization
    |--datasets
        |--cave_1024_28
            |--scene1.mat
            |--scene2.mat
            ：  
            |--scene205.mat
        |--CAVE_512_28
            |--scene1.mat
            |--scene2.mat
            ：  
            |--scene30.mat
        |--KAIST_CVPR2021  
            |--1.mat
            |--2.mat
            ： 
            |--30.mat
        |--TSA_simu_data  
            |--mask.mat   
            |--Truth
                |--scene01.mat
                |--scene02.mat
                ： 
                |--scene10.mat
        |--TSA_real_data  
            |--mask.mat   
            |--Measurements
                |--scene1.mat
                |--scene2.mat
                ： 
                |--scene5.mat
```

Following TSA-Net and DGSMP, we use the CAVE dataset (cave_1024_28) as the simulation training set. Both the CAVE (CAVE_512_28) and KAIST (KAIST_CVPR2021) datasets are used as the real training set. 

## 3. Simulation Experiement:

(1)  Training:	

```shell
cd MST/simulation/train_code/

# MST_S
python train.py --template mst_s --outf ./exp/mst_s/ --method mst_s 

# MST_M
python train.py --template mst_m --outf ./exp/mst_m/ --method mst_m  

# MST_L
python train.py --template mst_l --outf ./exp/mst_l/ --method mst_l 

# GAP-Net
python train.py --template gap_net --outf ./exp/gap_net/ --method gap_net 

# ADMM-Net
python train.py --template admm_net --outf ./exp/admm_net/ --method admm_net 

# TSA-Net
python train.py --template tsa_net --outf ./exp/tsa_net/ --method tsa_net 

# HDNet
python train.py --template hdnet --outf ./exp/hdnet/ --method hdnet 

# DGSMP
python train.py --template dgsmp --outf ./exp/dgsmp/ --method dgsmp 

# BIRNAT
python train.py --template birnat --outf ./exp/birnat/ --method birnat 

# MST_Plus_Plus
python train.py --template mst_plus_plus --outf ./exp/mst_plus_plus/ --method mst_plus_plus 

# λ-Net
python train.py --template lambda_net --outf ./exp/lambda_net/ --method lambda_net
```

The training log, trained model, and reconstrcuted HSI will be available in `MST/simulation/train_code/exp/` . 

(2)  Testing :	

Download the pretrained model zoo from ([Google Drive](https://drive.google.com/drive/folders/1zgB7jHqTzY1bjCSzdX4lKQEGyK3bpWIx?usp=sharing) / [Baidu Disk](https://pan.baidu.com/s/1CH4uq_NZPpo5ra2tFzAdfQ?pwd=mst1), code: `mst1`) and place them to `MST/simulation/test_code/model_zoo/`

Run the following command to test the model on the simulation dataset.

```python
cd MST/simulation/test_code/

# MST_S
python test.py --template mst_s --outf ./exp/mst_s/ --method mst_s --pretrained_model_path ./model_zoo/mst/mst_s.pth

# MST_M
python test.py --template mst_m --outf ./exp/mst_m/ --method mst_m --pretrained_model_path ./model_zoo/mst/mst_m.pth

# MST_L
python test.py --template mst_l --outf ./exp/mst_l/ --method mst_l --pretrained_model_path ./model_zoo/mst/mst_l.pth

# GAP_Net
python test.py --template gap_net --outf ./exp/gap_net/ --method gap_net --pretrained_model_path ./model_zoo/gap_net/gap_net.pth

# ADMM_Net
python test.py --template admm_net --outf ./exp/admm_net/ --method admm_net --pretrained_model_path ./model_zoo/admm_net/admm_net.pth

# TSA_Net
python test.py --template tsa_net --outf ./exp/tsa_net/ --method tsa_net --pretrained_model_path ./model_zoo/tsa_net/tsa_net.pth

# HDNet
python test.py --template hdnet --outf ./exp/hdnet/ --method hdnet --pretrained_model_path ./model_zoo/hdnet/hdnet.pth

# DGSMP
python test.py --template dgsmp --outf ./exp/dgsmp/ --method dgsmp --pretrained_model_path ./model_zoo/dgsmp/dgsmp.pth

# BIRNAT
python test.py --template birnat --outf ./exp/birnat/ --method birnat --pretrained_model_path ./model_zoo/birnat/birnat.pth

# MST_Plus_Plus
python test.py --template mst_plus_plus --outf ./exp/mst_plus_plus/ --method mst_plus_plus --pretrained_model_path ./model_zoo/mst_plus_plus/mst_plus_plus.pth

# λ-Net
python test.py --template lambda_net --outf ./exp/lambda_net/ --method lambda_net --pretrained_model_path ./model_zoo/lambda_net/lambda_net.pth
```

- The reconstrcuted HSIs will be output into `MST/simulation/test_code/exp/`  

- Place the reconstructed results into `MST/simulation/test_code/Quality_Metrics/results` and  

```shell
Run cal_quality_assessment.m
```

to calculate the PSNR and SSIM of the reconstructed HSIs.

(3)  Visualization :	
- Put the reconstruted HSI in `MST/visualization/simulation_results/results` and rename it as method.mat, e.g., mst_s.mat.

- Generate the RGB images of the reconstructed HSIs

```shell
 cd MST/visualization/
 Run show_simulation.m 
```

- Draw the spetral density lines

```shell
cd MST/visualization/
Run show_line.m
```

## 4. Real Experiement:

(1)  Training:	

```shell
cd MST/real/train_code/

# MST_S
python train.py --template mst_s --outf ./exp/mst_s/ --method mst_s 

# MST_M
python train.py --template mst_m --outf ./exp/mst_m/ --method mst_m  

# MST_L
python train.py --template mst_l --outf ./exp/mst_l/ --method mst_l 

# GAP-Net
python train.py --template gap_net --outf ./exp/gap_net/ --method gap_net 

# ADMM-Net
python train.py --template admm_net --outf ./exp/admm_net/ --method admm_net 

# TSA-Net
python train.py --template tsa_net --outf ./exp/tsa_net/ --method tsa_net 

# HDNet
python train.py --template hdnet --outf ./exp/hdnet/ --method hdnet 

# DGSMP
python train.py --template dgsmp --outf ./exp/dgsmp/ --method dgsmp 

# BIRNAT
python train.py --template birnat --outf ./exp/birnat/ --method birnat 

# MST_Plus_Plus
python train.py --template mst_plus_plus --outf ./exp/mst_plus_plus/ --method mst_plus_plus 

# λ-Net
python train.py --template lambda_net --outf ./exp/lambda_net/ --method lambda_net
```

The training log, trained model, and reconstrcuted HSI will be available in `MST/real/train_code/exp/` . 

(2)  Testing :	

```python
cd MST/real/test_code/

# MST_S
python test.py --template mst_s --outf ./exp/mst_s/ --method mst_s --pretrained_model_path ./model_zoo/mst/mst_s.pth

# MST_M
python test.py --template mst_m --outf ./exp/mst_m/ --method mst_m --pretrained_model_path ./model_zoo/mst/mst_m.pth

# MST_L
python test.py --template mst_l --outf ./exp/mst_l/ --method mst_l --pretrained_model_path ./model_zoo/mst/mst_l.pth

# GAP_Net
python test.py --template gap_net --outf ./exp/gap_net/ --method gap_net --pretrained_model_path ./model_zoo/gap_net/gap_net.pth

# ADMM_Net
python test.py --template admm_net --outf ./exp/admm_net/ --method admm_net --pretrained_model_path ./model_zoo/admm_net/admm_net.pth

# TSA_Net
python test.py --template tsa_net --outf ./exp/tsa_net/ --method tsa_net --pretrained_model_path ./model_zoo/tsa_net/tsa_net.pth

# HDNet
python test.py --template hdnet --outf ./exp/hdnet/ --method hdnet --pretrained_model_path ./model_zoo/hdnet/hdnet.pth

# DGSMP
python test.py --template dgsmp --outf ./exp/dgsmp/ --method dgsmp --pretrained_model_path ./model_zoo/dgsmp/dgsmp.pth

# BIRNAT
python test.py --template birnat --outf ./exp/birnat/ --method birnat --pretrained_model_path ./model_zoo/birnat/birnat.pth

# MST_Plus_Plus
python test.py --template mst_plus_plus --outf ./exp/mst_plus_plus/ --method mst_plus_plus --pretrained_model_path ./model_zoo/mst_plus_plus/mst_plus_plus.pth

# λ-Net
python test.py --template lambda_net --outf ./exp/lambda_net/ --method lambda_net --pretrained_model_path ./model_zoo/lambda_net/lambda_net.pth
```

- The reconstrcuted HSI will be output into `MST/real/test_code/exp/`  

(3)  Visualization :	

- Put the reconstruted HSI in `MST/visualization/real_results/results` and rename it as method.mat, e.g., mst_plus_plus.mat.

- Generate the RGB images of the reconstructed HSI

```shell
cd MST/visualization/
Run show_real.m
```

## Citation
If this repo helps you, please consider citing our works:


```shell


# MST
@inproceedings{mst,
	title={Mask-guided Spectral-wise Transformer for Efficient Hyperspectral Image Reconstruction},
	author={Yuanhao Cai and Jing Lin and Xiaowan Hu and Haoqian Wang and Xin Yuan and Yulun Zhang and Radu Timofte and Luc Van Gool},
	booktitle={Proceedings of the IEEE Conference on Computer Vision and Pattern Recognition (CVPR)},
	year={2022}
}


# MST++
@inproceedings{mst_pp,
  title={MST++: Multi-stage Spectral-wise Transformer for Efficient Spectral Reconstruction},
  author={Yuanhao Cai and Jing Lin and Zudi Lin and Haoqian Wang and Yulun Zhang and Hanspeter Pfister and Radu Timofte and Luc Van Gool},
  booktitle={Proceedings of the IEEE/CVF Conference on Computer Vision and Pattern Recognition (CVPR) Workshops},
  year={2022}
}


# HDNet
@inproceedings{hdnet,
	title={HDNet: High-resolution Dual-domain Learning for Spectral Compressive Imaging},
	author={Xiaowan Hu and Yuanhao Cai and Jing Lin and  Haoqian Wang and Xin Yuan and Yulun Zhang and Radu Timofte and Luc Van Gool},
	booktitle={Proceedings of the IEEE Conference on Computer Vision and Pattern Recognition (CVPR)},
	year={2022}
}

```
