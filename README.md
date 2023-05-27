## Installation

```conda create -n freenerf python=3.6.15```

```conda activate freenerf```

```pip install -r requirements.txt```

install jaxlib with the correct CUDA version.
```
pip install --upgrade jaxlib==0.1.68+cuda110 -f https://storage.googleapis.com/jax-releases/jax_cuda_releases.html
```

## Running the code

start the training process by calling

```python train.py --gin_configs configs/{CONFIG} ```

where you replace `{CONFIG}` with the config you want to use. 

### Rendering test images

You can render and evaluate test images by running

```python eval.py --gin_configs configs/{CONFIG} ```

where you replace `{CONFIG}` with the config you want to use. Similarly, you can render a camera trajectory (which we used for our videos) by running

```python render.py --gin_configs configs/{CONFIG} ```

## Citation

If you find our work useful, please cite it as
```
@InProceedings{Yang2023FreeNeRF,
    author    = {Jiawei Yang and Marco Pavone and Yue Wang},},  
    title     = {FreeNeRF: Improving Few-shot Neural Rendering with Free Frequency Regularization},
    booktitle = {Proc. IEEE Conf. on Computer Vision and Pattern Recognition (CVPR)},
    year      = {2023},
}
```
