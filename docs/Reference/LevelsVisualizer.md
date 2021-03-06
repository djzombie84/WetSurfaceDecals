# Levels Visualizer

The levels visualizer is part of the [Wet Decal](../WetDecal) inspector. Each colour channel in a detail layer has a levels visualizer.

It shows how the texture data (shown on the left) is converted into wetness values (shown on the right). Values at the top of the right hand box indicate maximum wetness (controlled by the `Saturation` setting). Values at the bottom of the right hand box indicate minimum wetness (i.e. completely dry).

![Level Visualizer](../images/LevelsVisualizer.png)

## Input Range Threshold

Controls _which part_ of the input gets mapped into the output.

When the threshold is set to `0` all values in the input texture will result in a completely dry surface. This is shown by the output (on the right) being completely on the bottom:

![All Dry](../images/ThresholdCompletelyDry.gif)

When the threshold is set to `1` all values in the input texture will result in a completely wet surface. This is shown by the output (in the left) being completely on the top:

![All Wet](../images/ThresholdCompletelyWet.gif)

Intermediate values will move the range and control how much of the texture is considered to be wet.

![Reducing from max to min threshold](../images/ThresholdMovingRange.gif)

## Input Range Softness

Controls _how much_ of the input gets mapped into the output.

When the softness is `0` a single slice through the input texture will be taken. Values above the slice will be considered completely wet and values below the slice will be considered completely dry. This results in a very sharp transition from wet to dry at the edge of puddles.

![Softness Zero](../images/SoftnessZero.gif)

When the softness is `1` the entire range of the input texture will be taken. Values at the top of the input range (or above) will be considered completely wet. Values at the bottom of the input range (or below) will be considered completely dry.

![Softness One](../images/SoftnessOne.gif)

## Output Range

Controls the maximum and minimum amount of wetness in the output range.

![Min Max Slider](../images/MinMaxSlider.gif)