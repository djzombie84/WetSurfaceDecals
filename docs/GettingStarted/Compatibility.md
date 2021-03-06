## What Items In the Scene Are Visible?

Wet Stuff works by modifying the internals of the Unity renderer to make dry materials appear wet. You can easily verify if a particular item will be affected by Wet Stuff with the _Frame Debugger_.

1. Open the frame Debugger through `Window > Frame Debugger` or `Window > Analysis > Frame Debugger`
2. Select the `RenderDeferred.GBuffer` entry.
3. Change the dropdown box to `RT2`. You should see something like this:

![GBuffer Barrel](../images/GBufferNormals.png)

If you can see your object here then it will be visible to Wet Stuff and will be modified by the wetness effect.

For example the image above shows the barrel and the ground so you know that they will both be modified by Wet Stuff. However it does not show the skybox so you know that it will not not be modified by Wet Stuff.

## HDRP Support

It is not currently possible to support the HDRP. We are waiting for extra some features to be added by Unity which will make it possible (an equivalent to the `https://docs.unity3d.com/ScriptReference/Camera.AddCommandBuffer.html` method).

## URP Support

The URP is not a deferred renderer and is thus incompatible with how Wet Stuff works. However, Unity [plan to add](https://docs.unity3d.com/Packages/com.unity.render-pipelines.lightweight@5.10/manual/faq.html#does-lwrp-support-a-deferred-renderer) a deferred mode to URP in the future which we _may_ add support for.