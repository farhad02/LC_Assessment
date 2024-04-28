# Comprehensive Complexity Assessment of Emerging Learned Image Compression on CPU and GPU
This repository contains the data associated with the paper "Comprehensive Complexity Assessment of Emerging Learned Image Compression on CPU and GPU", presented in IEEE ICASSP 2023.

## Paper
The paper can be accessed through IEEE: https://ieeexplore.ieee.org/abstract/document/10096046

The preprint is available on: https://arxiv.org/abs/2212.05466

**Abstract**

Learned Compression (LC) is the emerging technology for compressing image and video content, using deep neural networks. Despite being new, LC methods have already gained a compression efficiency comparable to state-of-the-art image compression, such as HEVC or even VVC. However, the existing solutions often require a huge computational complexity, which discourages their adoption in international standards or products. This paper provides a comprehensive complexity assessment of several notable methods, that shed light on the matter, and guide the future development of this field by presenting key findings. To do so, six existing methods have been evaluated for both encoding and decoding, on CPU and GPU platforms. Various aspects of complexity such as the overall complexity, share of each coding module, number of operations, number of parameters, most demanding GPU kernels, and memory requirements have been measured and compared on Kodak dataset. The reported results (1) quantify the complexity of LC methods, (2) fairly compare different methods, and (3) a major contribution of the work is identifying and quantifying the key factors affecting the complexity.

## Methodology
The methodology to collect the data is given in Fig.2  of the paper, copied here.

![image](https://github.com/farhad02/LC_Assessment/assets/25692764/e9dd5c0e-36c0-4745-b340-27426e51a2ef)

For each measurement a warm-up step is performed where the codec model is loaded into the device (CPU or GPU). Loading time Is excluded from the measurements. A dummy encoding/decoding runs first to warm-up the GPU to high working frequencies. Next synchronization is done between the host and device, for more accurate GPU measurement. Finally, the encoding/decoding are performed for each image on a codec fully annotated for sub-module measurements. For time measurements, the following tolls are used: Nsight System, Time library, and and [PTFlops library](https://github.com/sovrasov/flops-counter.pytorch).

The evaluations are done using the [CompressAI Library](https://interdigitalinc.github.io/CompressAI/), and on the following codecs, with the annotations given in the paranthesis:

1- Factorized Prior (FP), [ICLR2018](https://arxiv.org/abs/1802.01436)

2- Scale Hyperprior (HP), [ICLR2018](https://arxiv.org/abs/1802.01436)

3- Mean and Scale HP (MS-HP), [Neurips2018](https://arxiv.org/abs/1809.02736)

4- Autoregresive Context, (ARC), [Neurips2018](https://arxiv.org/abs/1809.02736)

5- Discretized Gaussian Mixture likelihood (DGM), [CVPR2020](https://arxiv.org/abs/2001.01568)

6- DGM with Attention (DGM-ATT), [CVPR2020](https://arxiv.org/abs/2001.01568)

 
## Data

The data provided in the folder "FALCON_ICASSP2023_WP1_V1.0" includes the detailed profiling results of this project, organized in .xlsx files. The subfolder "Timing" includes the timings of encoding and decoding operations on CPU and GPU (marked with CUDA). The information is given for images in [KODAK dataset](https://r0k.us/graphics/kodak/). The tabulated data contains sheets that are either given per image, which includes the image name, named kodim01 to kodim24, or as average results. The subfolder "NSightSystems_Kernels_Memory" includes GPU profiling reports from NSight Systems. The tab AVG includes the raw average results for Kodak dataset, and the tab Summarized gives a summary of kernel shares. For interpretation of raw information in Nsight Systems refer to the software's [documentation](https://docs.nvidia.com/nsight-systems/UserGuide/index.html). Moreover, the tab Memory summarizes the memory operations during encoding and decoding.

## Data mirror
The data can also be accessed through [Zenodo](https://zenodo.org/records/11080556).

## License and terms of use
This data is licensed under CC-BY-4.0,. The data can be used and distributed freely, with proper reference to the paper.

## Citation

If this work is useful to your research, please cite the paper as follows:

    @INPROCEEDINGS{10096046,
        author={Pakdaman, Farhad and Gabbouj, Moncef},
        booktitle={ICASSP 2023 - 2023 IEEE International Conference on Acoustics, Speech and Signal Processing (ICASSP)}, 
        title={Comprehensive Complexity Assessment of Emerging Learned Image Compression on CPU and GPU}, 
        year={2023},
        pages={1-5},
        doi={10.1109/ICASSP49357.2023.10096046}
  }

## Project information
This data is associated with the project [FALCON](https://www.tuni.fi/en/research/falcon), under Work Package 1 (WP1). The This project has received funding from the European Union’s Horizon 2020 research and innovation programme under the Marie Skłodowska-Curie grant agreement No 101022466.
