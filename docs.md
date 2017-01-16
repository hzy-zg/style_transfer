## generate.py 

`generate.py` acts as the command line parser and containts default training parameters.

**Flags.**

- `base_img_path`: path to base image (required).
- `style_img_path`: path to style image (required).
- `output_img_path`: path location for saving output (required).
- `--iters`: number of iterations for L-BFGS optimizer.
- `--content_weight`: weight for content feature loss. Default has been set to `7.5e0`.
- `--style_weight`:  weight for style feature loss. Default has been set to `1e2`.
- `--tv_weight`: weight for total variation loss. Default has been set to `2e2`.
- `--width`: output image width. If specified, output image height is changed accordingly.
- `--convnet`: vgg model to use: 16 or 19. Default has been set to `vgg16`.


## neural_styler.py


