---
---

The idea is to enable a iiif service to improve the speed of rendering of a gallery view by merging all the thumnail images into a spritesheet, so that hundreds of images do not need to be downloaded individually. The challenge is to configure the thumbnail service in the manifest to render an individual thumbnail sprite out of the spritesheet on the client side.

Is this possible? I'm not clear enough yet on the capabilities of the fragment selector framework to be sure. I've set up a simple manifest for tinkering.

## Setup

<figure style="float: right">
    <img src="{{site.url}}{{site.baseurl}}/spritesheet/spritesheet.jpg"
         alt="Spritesheet with two thumbnail images">
    <figcaption>Spritesheet with two thumbnail images</figcaption>
</figure>

- created prezi3 manifest and static IIIF resources with [biiif](https://github.com/IIIF-Commons/biiif) for two-image item
	- tidied it up to validate (fixed language tags)
- created spritesheet with [sstool from Leshy Labs](https://www.leshylabs.com/apps/sstool/)
	- saved as spritesheet.jpg, and saved list as sprites.txt

Sprite coordinates:

```
1_thumb,0,0,100,100
2_thumb,0,101,100,100
```

Manifest: [manifest.json]({{site.url}}{{site.baseurl}}/manifest.json)

View in 
[Mirador](https://projectmirador.org/embed/?manifest={{site.url}}{{site.baseurl}}/manifest.json)
|
[Universal Viewer](https://uv-v4.netlify.app/#?manifest={{site.url}}{{site.baseurl}}/manifest.json)

## SVGs?

<figure style="float: right">
    <img src="{{site.url}}{{site.baseurl}}/2-back/thumb.svg" style="border: 1px solid black"
         alt="SVG that uses a viewBox">
    <figcaption>SVG that uses a viewBox</figcaption>
</figure>

<p>
<svg viewBox="0 101 100 100" width="100" height="100" xmlns="http://www.w3.org/2000/svg">
  <image href="{{ site.url }}/{{ site.baseurl }}/spritesheet/+tiles/full/max/0/default.jpg" height="201" width="100"/>
</svg>
</p>