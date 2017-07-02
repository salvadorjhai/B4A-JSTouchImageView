# B4A-JSTouchImageView
[TouchImageView](https://github.com/MikeOrtiz/TouchImageView) Wrapped for B4A (Basic4Android)

==Copy .jar, .xml to your additional library folder==

### Sample
###### Initialize and set Image
```
' add JSTouchImageView on your activity via code or from designer
Dim touchImage As JSTouchImageView
touchImage.Initialize("touchImage")
Activity.AddView(touchImage, 0dip, 0dip, 100%x, 100%y)

' set image bitmap
touchImage.setImageBitmap(LoadBitmap(File.DirAssets, "image.jpeg"))
```

###### Get ScrollPosition and ZoomedRect (Using JavaObject)
```
Dim point As JavaObject = touchImage.ScrollPosition
Dim rect As JavaObject = touchImage.ZoomedRect

Dim currentZoom As Float = touchImage.CurrentZoom
Dim isZoomed As Boolean = touchImage.IsZoomed

LogColor($"x: ${point.GetField("x")} y: ${point.GetField("y")}"$, Colors.Blue)
LogColor($"left: ${rect.GetField("left")} top: ${rect.GetField("top")}"$, Colors.Blue)
LogColor($"right: ${rect.GetField("right")} bottom: ${rect.GetField("bottom")}"$, Colors.Blue)
LogColor($"currentZoom: ${currentZoom} isZoomed: ${isZoomed}"$, Colors.Blue)
```

### Acknowledgement
* Pexels.com - https://www.pexels.com
* MikeOrtiz - https://github.com/MikeOrtiz/TouchImageView

