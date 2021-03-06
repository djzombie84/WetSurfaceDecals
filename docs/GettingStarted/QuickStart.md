## 1. Import Wet Decals

Import the Wet Decals asset into your project. This will create two folders:

 - `Assets/PlaceholderSoftware/WetStuff`

This folder contains the changelog, prefabs and demo scenes.

 - `Assets/Plugins/PlaceholderSoftware/WetStuff`

This folder contains the core effect.

## 2. Add `WetStuff` script to your cameras

Add the `WetStuff` script to each camera in your scene. Cameras must have this script attached for the decals to be visible from that camera.

> **Ensure that the camera is rendering using the Deferred pipeline.**

## 3. Place `WetDecalPuddle` prefab into your scene

Drag the `WetDecalPuddle` prefab located in `Assets/PlaceholderSoftware/WetStuff/Prefabs` into your scene view and move it until it overlaps a surface, the surface should appear wet. See the [Wet Decal](../WetDecal) guide for more information on how to build your own decals.