# iiif-thumbnail-sprites
Experiment in using a spritesheet to convey thumnbail images for a IIIF manifesto

The idea is to enable a iiif service to improve the speed of rendering of a gallery view by merging all the thumnail images into a spritesheet, so that hundreds of images do not need to be downloaded individually. The challenge is to configure the thumbnail service in the manifest to render an individual thumbnail sprite out of the spritesheet on the client side.

Is this possible? I'm not clear enough yet on the capabilities of the fragment selector framework to be sure. I've set up a simple manifest for tinkering.

