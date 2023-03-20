# iiif-thumbnail-sprites
Experiment in using a spritesheet to convey thumnbail images for a IIIF manifesto

The idea is to enable a iiif service to improve the speed of rendering of a gallery view by merging all the thumnail images into a spritesheet, so that hundreds of images do not need to be downloaded individually. The challenge is to configure the thumbnail service in the manifest to render an individual thumbnail sprite out of the spritesheet on the client side.

Is this possible? I'm not clear enough yet on the capabilities of the fragment selector framework to be sure. I've set up a simple manifest for tinkering.

## Setup

- created prezi3 manifest and static IIIF resources with [biiif](https://github.com/IIIF-Commons/biiif) for two-image item
	- tidied it up to validate (fixed language tags)
- created spritesheet with [sstool from LeshyLabs](https://www.leshylabs.com/apps/sstool/)
	- saved as spritesheet.jpg, and saved list as sprites.txt

![Spritesheet](https://raw.githubusercontent.com/pbinkley/iiif-thumbnail-sprites/main/spritesheet.jpg)

