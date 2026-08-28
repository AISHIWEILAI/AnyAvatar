<div align="center">

# AnyAvatar: High-Fidelity Gaussian Head Avatars under Uncalibrated Camera Settings

<h3>🎉 Accepted to ACM MM 2026 (Poster)</h3>

**Yujian Liu**<sup>1,2,&#42;</sup>, **Dongxu Shen**<sup>3,&#42;</sup>, **Haoran Li**<sup>1,&#42;</sup>, **Yuting Liu**<sup>1</sup>, **Chuang Chen**<sup>1</sup>, **Xinyi Jiang**<sup>1</sup>, **Zhupeng Jiang**<sup>1</sup>, **Peng Cao**<sup>4,†</sup>, **Shidang Xu**<sup>2,†</sup>, **Xiaoli Liu**<sup>1,†</sup>

<sup>1</sup> AiShiWeiLai AI Research  <sup>2</sup> South China University of Technology  
<sup>3</sup> The Hong Kong University of Science and Technology (Guangzhou)  <sup>4</sup> Northeastern University

[Project](https://syncanimation.github.io/AnyAvatar.github.io/) / [Paper](https://github.com/syncanimation/AnyAvatar.github.io)

<img src="static/images/pipeline.png" alt="AnyAvatar" width="100%"/>

</div>

## Usage

### Step 1. Coarse Camera Pose Initialization

Obtain coarse camera poses with [VGGT](https://github.com/facebookresearch/vggt). Please refer to the official VGGT repository for installation and inference.

In our implementation, we use the **first frame of the neutral expression** to estimate camera poses.

### Step 2. VHAP Training

<div align="center">
<img src="static/images/Mesh.png" alt="FLAME mesh heads from VHAP" width="100%"/>
</div>

We use the camera poses estimated by VGGT to train VHAP. For specific instructions, please refer to [VHAP/README.md](VHAP/README.md).

After this step, we obtain the FLAME mesh heads that will be used for Gaussian training.

### Step 3. Gaussian Rendering

<div align="center">
<img src="static/videos/high_renders.gif" alt="AnyAvatar high-fidelity renders" width="40%"/>
</div>

With the mesh heads obtained from VHAP, we can start training Gaussian head avatars. For specific instructions, please refer to [AnyAvatar/README.md](AnyAvatar/README.md).

## Acknowledgments

We thank the authors of [VHAP](https://github.com/ShenhanQian/VHAP) and [GaussianAvatars](https://github.com/ShenhanQian/GaussianAvatars) for their contributions to multi-view Gaussian head avatars. Part of this work is built upon their open-source efforts. We also thank [Haoran Li](https://github.com/Haoran-Li-0708) and Xueni Guo for contributing portrait data.

## License

This work is licensed under [CC BY-NC 4.0](http://creativecommons.org/licenses/by-nc/4.0/). See [LICENSE](LICENSE) for details.
