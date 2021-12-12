---
title: OCR on PDF Files
date: 2021-08-25 08:27:12
updated: 2021-12-06 23:06:31
tags: Computer
---

Use Acrobat to export the pdf file to single page tiff image.

![Untitled](./Untitled.png)

Let's have a look at the output images:

Right click→ properties

![Untitled](./Untitled_1.png)

Most of them are already in perfect condition: 300 dpi or higher, binary image with only 1 bit depth, which is good for the final pdf's small volume.

Of course, there would also be some exceptions, such as this one, with a significantly larger file size.

![Untitled](./Untitled_2.png)

We just need to throw them all into Comic Enhancer Pro

![Untitled](./Untitled_3.png)

Press on the button to process scanned books.

![Untitled](./Untitled_4.png)

The best effect comes from curve. 

![Untitled](./Untitled_5.png)

X axis is the grayscale of original, while y is the projected new grayscale intensity. We need to suppress the tint gray that was the picture on the back side, while maintaining proper intensities on the characters.

![Untitled](./Untitled_6.png)

Most of the gray suppressed to close to white, and the dark parts, text included, are also enhanced.

The adjusting method is like adjusting a Bezier curve, intuitive enough.

![Untitled](./Untitled_7.png)

In pursuit of extremely tiny file size, we only need binary image. Tick on the `shaking` check box to achieve decent (though limited) gray effect.

![Untitled](./Untitled_8.png)

Let the batch begin. Some images might require an individual profile.

![Untitled](./Untitled_9.png)

Launch FreePic2Pdf

![Untitled](./Untitled_10.png)

![Untitled](./Untitled_11.png)

![Untitled](./Untitled_12.png)

Click Go, and be patient before it finishes.

![Untitled](./Untitled_13.png)

Recognition results are quite impressive, we can hardly detect errors in the copied text. (Sumatra PDF, strongly recommended, btw)

![Untitled](./Untitled_14.png)

Not perfect on English or Equations, but I'll say it has exceed my anticipation. And the quality of pictures are unbelievable. 

![Untitled](./Untitled_15.png)

![Untitled](./Untitled_16.png)

Searching or annotating is more than usable, which *is* the purpose of our effort. (Drawboard PDF, also strongly recommended, btw)

![Untitled](./Untitled_17.png)

File size dropped from 49MB to 35MB, the saving is not remarkable, because the original file was already doing a good job by making most of its pictures binary. 

One last thing, the index or bookmarks. it can be readily solved by PdgCntEditor.

![Untitled](./Untitled_18.png)

Still very easy drag-and-drop, the original file has included a good index, we'll make just make use of it.

![Untitled](./Untitled_19.png)

Copy and paste — and done, yeah, it's *that simple.*

![Untitled](./Untitled_20.png)

Sometimes you'll need to specify the page number of the 1st page, but basically, that's pretty much it.

![Untitled](./Untitled_21.png)

Maybe we'll open up a page to talk about `PdgCntEditor` some day.