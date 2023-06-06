# RUC-Net: A Residual-Unet-Based Convolutional Neural Network for Pixel-Level Pavement Crack Segmentation
This is my own PyTorch implementation of 2023 U-Net (RUC-Net) used for crack segmentation. https://www.mdpi.com/1424-8220/23/1/53
# Architecture of RUC-Net
![image](https://github.com/americanexplorer13/rucnet/assets/57260643/485f078c-f300-4d9b-a19a-dc2c70460152)
# Usage
pytorch == 2.0.0
# Bias and limitations
If you would look through my code, you will notice 3 differents from original paperwork: first of all, last conv layer were changed from conv3x3 to conv1x1. I suppose, it's a typo. Second, GroupNorm instead of BatchNorm. It's preferable to use GN if your batch_size < 32, but if you want, just change it in this code. I used scSE block, however in original paperwork they propose to use different blocks in order to give you different results on your data, so if you want to use different block you should probably find it in github + I put scse block on last downsample block. I don't really know is it a good idea or not, but in my case it gives me better results than without it so if you wish, just remove it from code.
