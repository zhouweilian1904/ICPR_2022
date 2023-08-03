# ICPR_2022
The accepted paper for the 26th International Conference on Pattern Recognition (ICPR2022).

W. Zhou, S. -I. Kamata, Z. Luo and X. Chen, "Hierarchical Unified Spectral-Spatial Aggregated Transformer for Hyperspectral Image Classification," 2022 26th International Conference on Pattern Recognition (ICPR), 2022, pp. 3041-3047, doi: 10.1109/ICPR56361.2022.9956396. (https://ieeexplore.ieee.org/document/9956396)

**Please kindly cite the papers if this code is useful and helpful for your research.**

Spectral branch
-------------------------------
Spectral vision transformer (SVT).

![image](https://github.com/zhouweilian1904/ICPR_2022/blob/main/spectral%20only%20self-attention%202.png)


Spatial Branch
-------------------------------
Pyramid hierarchical local-global Transformer (PHT).

![image](https://github.com/zhouweilian1904/ICPR_2022/blob/main/whole%20structure.png)

Cross-scale fusion in the PHT
-------------------------------

![image](https://github.com/zhouweilian1904/ICPR_2022/blob/main/cross%20scale%20fusion.png)

**Abstract:**

Vision Transformer (ViT) has recently been introduced into the computer vision (CV) field with its self-attention mechanism and gotten remarkable performance. However, simply applying ViT for hyperspectral image (HSI) classification is not applicable due to 1) ViT is a spatial-only self-attention model, but rich spectral information exists in HSI; 2) ViT needs sufficient training samples, but HSI suffers from limited samples; 3) ViT does not well learn local features; 4) multi-scale features for ViT are not considered. Furthermore, the methods which combine convolutional neural network (CNN) and ViT generally suffer from a large computational burden. Hence, this paper tends to design a suitable pure ViT based model for HSI classification as the following points: 1) spectral-only vision transformer with all tokens’ aggregation; 2) spatial-only local-global transformer; 3) cross-scale local-global feature fusion, and 4) a cooperative loss function to unify the spectral and spatial features. As a result, the proposed idea achieves competitive classification performance on three public datasets than other state-of-the-art methods.

--------------------------------
**Datasets:**

We have uploaded several datasets: https://drive.google.com/drive/folders/1IQxuz4jpwf6goB_2ZwVLEZz1ILScymdO?usp=share_link
1. Indian Pines, 
2. PaviaU, 
3. PaviaC, 
4. Botswana, 
5. Houston 2013, 
6. KSC, 
7. Mississippi_Gulfport, 
8. Salinas, 
9. Simulate_database, 
10. Augmented_IndianPines, 
11. Augmented_Mississippi_Gulfport, 
12. Augmented_PaviaU
13. The disjoint datasets (IP, PU, HU) can be referred in https://github.com/danfenghong/IEEE_TGRS_SpectralFormer.


--------------------------------
**How to use:**

you can find and add some arguments in *main.py* for your own testing.

For example:

python main.py --model zhou_ICPR2022 --dataset IndianPines --training_sample 0.1 --cuda 0 --epoch 200 --batch_size 100 --patch_size 9

--------------------------------
