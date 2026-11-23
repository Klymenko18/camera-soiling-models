# Camera soiling models

| Files | Use |
|---|---|
| `fpn_resnet18_correct_clear_ce.ckpt` | WoodScape FPN–ResNet18 checkpoint for segmenting lens contamination. This is the authors’ cross-entropy checkpoint trained on the Correct Clear Files subset. |
| `brisque_model_live.yml` and `brisque_range_live.yml` | OpenCV BRISQUE model and feature ranges for general image-quality scoring. Pass both files to `cv2.quality.QualityBRISQUE_create`. |

Clone with Git LFS installed, then run `git lfs pull` to retrieve the checkpoint.

The FPN checkpoint is 156,745,498 bytes. Its SHA-256 is `9a76f077194418c24e29aa2c8d213c5f6adbc879da04f799660a617538c400a9`. The output classes are clean, transparent, semi-transparent, and opaque.

Sources

- [WoodScape Revision authors’ repository](https://github.com/filipberanek/woodscape_revision/tree/e9dc1382355bf1c46d497d65b0066f50fdb0280d)
- [OpenCV BRISQUE sample models](https://github.com/opencv/opencv_contrib/tree/4.x/modules/quality/samples)
