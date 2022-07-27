## Progressive Representation Recalibration for Lightweight Super-resolution (PRRN)
The testing code for our paper **"Progressive Representation Recalibration for Lightweight Super-resolution"**, accepted by Neurocomputing [[pdf](https://www.sciencedirect.com/science/article/pii/S0925231222009080)]

## [NTIRE 2022 Workshop and Challenge](https://data.vision.ee.ethz.ch/cvl/ntire22/) @ CVPR 2022
## Our Methods PRRN also participated in [Efficient Super-Resolution Challenge](https://codalab.lisn.upsaclay.fr/competitions/1865). [Challenge Report](https://openaccess.thecvf.com/content/CVPR2022W/NTIRE/papers/Li_NTIRE_2022_Challenge_on_Efficient_Super-Resolution_Methods_and_Results_CVPRW_2022_paper.pdf)

## Baseline model (IMDN)

* Number of parameters: 893,936 (0.89M)

    ```python
    number_parameters = sum(map(lambda x: x.numel(), model.parameters()))
    ```

* Average PSNR on validation data: 29.13 dB

* Average inference time (Titan Xp) on validation data: 0.10 second 

    Note: The best average inference time among three trials is selected.

Run [test_demo.py](test_demo.py) to test the model

## Our model (PRRN)

* Number of parameters: 414008

* Average PSNR on validation data: 29.05 dB

* Average inference time (Tesla V100) on validation data: 0.05 second

## How to use the code during test phase.

1. `git clone https://github.com/house-leo/PRRN`
2. Put your model script under the `models` folder.
3. Put your pretrained model under the `model_zoo` folder.
4. Modify `model_path` in `test_demo.py`. Modify
the imported models.
5. `python test_demo.py`

## Citation:
If you find this work useful for your research, please cite:

```
@article{WEN2022240,
title = {Progressive representation recalibration for lightweight super-resolution},
journal = {Neurocomputing},
author = {Ruimian Wen and Zhijing Yang and Tianshui Chen and Hao Li and Kai Li},
volume = {504},
pages = {240-250},
year = {2022},
issn = {0925-2312}
}
```
