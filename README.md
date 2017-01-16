# Style Transfer in Keras

Add the style of a painting to any base image of your choosing!

<p align="center">
 <img src="./examples/bases/chicago.png" width="300px"> <img src="./examples/results/chicago_scream.jpg" width="300"/> 
</p>

This implementation is based off of [A Neural Algorithm of Artistic Style](https://arxiv.org/abs/1508.06576) by Leon A. Gatys, Alexander S. Ecker and Matthias Bethge.

## Implementation Details

## Documentation

Use `generate.py` to style an image. Example usage:

```
python generate.py \
examples/bases/chicago.jpg \
examples/styles/umbrella_girl.jpg \
examples/results/my_result \
--width=400
```

## Requirements

- Keras (and associated requirements)
- Python 2.7

## Attribution

- This implementation uses some code from Francois Chollet's [Neural Style Transfer](https://github.com/fchollet/keras/blob/master/examples/neural_style_transfer.py).
- The hierarchy also borrows from Giuseppe's gist which you can view [here](https://gist.github.com/giuseppebonaccorso/ef09a03424c9a49ae9b087bd364a5813).

