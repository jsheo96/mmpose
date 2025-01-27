<!-- [ALGORITHM] -->

<details>
<summary align="right"><a href="https://arxiv.org/abs/2104.02300">DEKR (CVPR'2021)</a></summary>

```bibtex
@inproceedings{geng2021bottom,
  title={Bottom-up human pose estimation via disentangled keypoint regression},
  author={Geng, Zigang and Sun, Ke and Xiao, Bin and Zhang, Zhaoxiang and Wang, Jingdong},
  booktitle={Proceedings of the IEEE/CVF Conference on Computer Vision and Pattern Recognition},
  pages={14676--14686},
  year={2021}
}
```

</details>

<!-- [ALGORITHM] -->

<details>
<summary align="right"><a href="http://openaccess.thecvf.com/content_CVPR_2019/html/Sun_Deep_High-Resolution_Representation_Learning_for_Human_Pose_Estimation_CVPR_2019_paper.html">HRNet (CVPR'2019)</a></summary>

```bibtex
@inproceedings{sun2019deep,
  title={Deep high-resolution representation learning for human pose estimation},
  author={Sun, Ke and Xiao, Bin and Liu, Dong and Wang, Jingdong},
  booktitle={Proceedings of the IEEE conference on computer vision and pattern recognition},
  pages={5693--5703},
  year={2019}
}
```

</details>

<!-- [DATASET] -->

<details>
<summary align="right"><a href="http://openaccess.thecvf.com/content_CVPR_2019/html/Li_CrowdPose_Efficient_Crowded_Scenes_Pose_Estimation_and_a_New_Benchmark_CVPR_2019_paper.html">CrowdPose (CVPR'2019)</a></summary>

```bibtex
@article{li2018crowdpose,
  title={CrowdPose: Efficient Crowded Scenes Pose Estimation and A New Benchmark},
  author={Li, Jiefeng and Wang, Can and Zhu, Hao and Mao, Yihuan and Fang, Hao-Shu and Lu, Cewu},
  journal={arXiv preprint arXiv:1812.00324},
  year={2018}
}
```

</details>

Results on CrowdPose test without multi-scale test

| Arch                                          | Input Size |  AP   | AP<sup>50</sup> | AP<sup>75</sup> |  AR   | AR<sup>50</sup> |                     ckpt                      |                      log                      |
| :-------------------------------------------- | :--------: | :---: | :-------------: | :-------------: | :---: | :-------------: | :-------------------------------------------: | :-------------------------------------------: |
| [HRNet-w32](/configs/body/2d_kpt_sview_rgb_img/disentangled_keypoint_regression/crowdpose/hrnet_w32_crowdpose_512x512.py) |  512x512   | 0.663 |      0.857      |      0.715      | 0.719 |      0.893      | [ckpt](https://download.openmmlab.com/mmpose/bottom_up/dekr/hrnet_w32_crowdpose_512x512-685aff75_20220924.pth) | [log](https://download.openmmlab.com/mmpose/bottom_up/dekr/hrnet_w32_crowdpose_512x512-20220924.log.json) |
| [HRNet-w48](/configs/body/2d_kpt_sview_rgb_img/disentangled_keypoint_regression/crowdpose/hrnet_w48_crowdpose_640x640.py) |  640x640   | 0.682 |      0.869      |      0.736      | 0.742 |      0.911      | [ckpt](https://download.openmmlab.com/mmpose/bottom_up/dekr/hrnet_w48_crowdpose_640x640-ef6b6040_20220930.pth) | [log](https://download.openmmlab.com/mmpose/bottom_up/dekr/hrnet_w48_crowdpose_640x640-20220930.log.json) |

Results on CrowdPose test with multi-scale test. 3 default scales (\[2, 1, 0.5\]) are used

| Arch                                                                | Input Size |  AP   | AP<sup>50</sup> | AP<sup>75</sup> |  AR   | AR<sup>50</sup> |                                 ckpt                                 |
| :------------------------------------------------------------------ | :--------: | :---: | :-------------: | :-------------: | :---: | :-------------: | :------------------------------------------------------------------: |
| [HRNet-w32](/configs/body/2d_kpt_sview_rgb_img/disentangled_keypoint_regression/crowdpose/hrnet_w32_crowdpose_512x512_multiscale.py)\* |  512x512   | 0.692 |      0.874      |      0.748      | 0.755 |      0.926      | [ckpt](https://download.openmmlab.com/mmpose/bottom_up/dekr/hrnet_w32_crowdpose_512x512-685aff75_20220924.pth) |
| [HRNet-w48](/configs/body/2d_kpt_sview_rgb_img/disentangled_keypoint_regression/crowdpose/hrnet_w48_crowdpose_640x640_multiscale.py)\* |  640x640   | 0.696 |      0.869      |      0.749      | 0.769 |      0.933      | [ckpt](https://download.openmmlab.com/mmpose/bottom_up/dekr/hrnet_w48_crowdpose_640x640-ef6b6040_20220930.pth) |

\* these configs are generally used for evaluation. The training settings are identical to their single-scale counterparts.
