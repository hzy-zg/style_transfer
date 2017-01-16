# Artistic Style Transfer in Keras

This is a Keras implementation of [A Neural Algorithm of Artistic Style](https://arxiv.org/abs/1508.06576) by Leon A. Gatys, Alexander S. Ecker and Matthias Bethge.

<div align='center'>
<img src = './examples/bases/chicago.jpg' height="200px">
</div>

<div align = 'center'>
<img src = './examples/thumbnail/the_scream.jpg' height = '200px'>
<img src = './examples/results/my_result_at_iteration_0.png' height = '200px'>
<img src = './examples/results/my_result_at_iteration_499.png' height = '200px'>
</div>

Neural Styler lets you create artistic images by combining a base picture with the style of another. For example, the images above show multiple iterations of the [Chicago skyline](http://www.nursing.uic.edu/sites/default/files/chicagoskyline_2.jpg) combined with Edvard Munch's [The Scream](https://en.wikipedia.org/wiki/The_Scream).

## API

`Neural_Styler` is the class abstraction which defines the loss and optimization.

## API

Styling an image is done through `generate.py` as follows:

```python
python generate.py examples/bases/chicago.jpg examples/styles/umbrella_girl.jpg examples/results/my_result
```

`generate.py` is actually a command line parser that makes use of the `Neural_Styler()` class abstraction.

**Parameters**

- `input_img`: tensor containing: content_img, style_img and output_img.
- `convnet`: (string), defines which VGG to use: vgg16 or vgg19.
- `style_layers`: list containing name of layers to use for style
  reconstruction. Defined in Gatys et. al but can be changed.
- `content_layer`: string containing name of layer to use for content
  reconstruction. Also defined in Gatys et. al.
- `content_weight`: weight for the content loss.
- `style_weight`: weight for the style loss.
- `tv_weight`: weight for the total variation loss.
- `iterations`: iterations for optimization algorithm
- `output_img_path`: path to output image.

You can see the default paramaters and a more detailed documentation [here]().

## Requirements

- Keras (and associated requirements)
- Python 2.7

## Attribution

- This implementation uses some code from Francois Chollet's [Neural Style Transfer](https://github.com/fchollet/keras/blob/master/examples/neural_style_transfer.py).
- The hierarchy also borrows from Giuseppe's gist which you can view [here](https://gist.github.com/giuseppebonaccorso/ef09a03424c9a49ae9b087bd364a5813).
