# Comprehensive Complexity Assessment of Emerging Learned Image Compression on CPU and GPU
This repository contains the data associated with the paper "Comprehensive Complexity Assessment of Emerging Learned Image Compression on CPU and GPU", presented in IEEE ICASSP 2023.

## Paper
The paper can be accessed through IEEE: https://ieeexplore.ieee.org/abstract/document/10096046

The preprint is available on: https://arxiv.org/abs/2212.05466

**Abstract**

Learned Compression (LC) is the emerging technology for compressing image and video content, using deep neural networks. Despite being new, LC methods have already gained a compression efficiency comparable to state-of-the-art image compression, such as HEVC or even VVC. However, the existing solutions often require a huge computational complexity, which discourages their adoption in international standards or products. This paper provides a comprehensive complexity assessment of several notable methods, that shed light on the matter, and guide the future development of this field by presenting key findings. To do so, six existing methods have been evaluated for both encoding and decoding, on CPU and GPU platforms. Various aspects of complexity such as the overall complexity, share of each coding module, number of operations, number of parameters, most demanding GPU kernels, and memory requirements have been measured and compared on Kodak dataset. The reported results (1) quantify the complexity of LC methods, (2) fairly compare different methods, and (3) a major contribution of the work is identifying and quantifying the key factors affecting the complexity.

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
