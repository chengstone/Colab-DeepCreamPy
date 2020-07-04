# Colab-DeepCreamPy
*Decensoring Hentai with Deep Neural Networks. The below links will support deeppomf, the mastermind of DeepCreamPy.*

[![Donate with PayPal to the original creator](https://img.shields.io/badge/paypal-donate-green.svg)](https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&hosted_button_id=SAM6C6DQRDBAE)
[![Twitter of the original creator](https://img.shields.io/twitter/follow/deeppomf.svg?label=Follow&style=social)](https://twitter.com/deeppomf/)

## Usage: Simply download `Colab-DeepCreamPy-2.0.ipynb` and open it inside your Google Drive or click [here](https://colab.research.google.com/github/styler00dollar/Colab-DeepCreamPy/blob/master/Colab-DeepCreamPy-2.0.ipynb) and copy the file with "File > Save a copy to Drive..." into your Google Drive.

# Info about Colab-DeepCreamPy
This master is not the newest version of DeepCreamPy because apperantly the decensor.py does not work out of the box with 2.2 and there is no GUI in Colab. This shouldn't matter, since the used model is uptodate.

# Info about Colab
- If you can't open `Colab-DeepCreamPy-2.0.ipynb` inside your Google Drive, try this [colab link](https://colab.research.google.com/github/styler00dollar/Colab-DeepCreamPy/blob/master/Colab-DeepCreamPy-2.0.ipynb) and save it to your Google Drive. The "open in Colab"-button can be missing in Google Drive, if that person never used Colab.
- Google Colab does assign a random GPU. It depends on luck.
- The Google Colab VM does have a maximum session length of 12 hours. Additionally there is a 30 minute timeout if you leave colab. The VM will be deleted after these timeouts.

# Description
This repository represents a deep learning-based tool to automatically replace censored artwork in hentai with plausible reconstructions inside a Google Colab virtual machine.

Before DeepCreamPy can be used, the user must color censored regions in their hentai green with an image editing program like GIMP or Photoshop. DeepCreamPy takes the green colored images as input, and a neural network automatically fills in the censored regions.

<p align="center">
	<img src="https://github.com/deeppomf/DeepCreamPy/blob/master/readme_images/mermaid_collage.png" width="800">
</p>

## Features
- Decensoring images of any size
- Decensoring of ANY shaped censor (e.g. black lines, pink hearts, etc.)
- Decensoring of mosaic decensors
- Limited support for decensoring black and white/monochrome images
- Generate multiple variations of decensors from the same image

## Limitations
The decensorship is for color hentai images that have minor to moderate censorship of the penis or vagina. If a vagina or penis is completely censored out, decensoring will be ineffective.

It does NOT work with:
- Hentai with screentones (e.g. printed hentai)
- Real life porn
- Censorship of nipples
- Censorship of anus
- Animated gifs/videos

## Contributions
Special thanks to deeppomf, ccppoo, IAmTheRedSpy, 0xb8, deniszh, Smethan, harjitmoe, itsVale, StartleStars and SoftArmpit. I, styler00dollar, only added Google Colab support.

## License
Source code and official releases/binaries are distributed under the [GNU Affero General Public License v3.0](LICENSE.md).

## Acknowledgements
Example mermaid image by Shurajo & AVALANCHE Game Studio under [CC BY 3.0 License](https://creativecommons.org/licenses/by/3.0/). The example image is modified from the original, which can be found [here](https://opengameart.org/content/mermaid).

Neural network code is modified from Forty-lock's project [PEPSI](https://github.com/Forty-lock/PEPSI), which is the official implementation of the paper [PEPSI : Fast Image Inpainting With Parallel Decoding Network](http://openaccess.thecvf.com/content_CVPR_2019/html/Sagong_PEPSI__Fast_Image_Inpainting_With_Parallel_Decoding_Network_CVPR_2019_paper.html). [PEPSI](https://github.com/Forty-lock/PEPSI) is licensed under the MIT license.

Training data is modified from gwern's project [Danbooru2017: A Large-Scale Crowdsourced and Tagged Anime Illustration Dataset](https://www.gwern.net/Danbooru2017) and other sources.

See [ACKNOWLEDGEMENTS.md](docs/ACKNOWLEDGEMENTS.md) for full license text of these projects.

## Donations
You can donate to the creator of DeepCreamPy via Paypal. [![Donate](https://img.shields.io/badge/Donate-PayPal-green.svg)](https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&hosted_button_id=SAM6C6DQRDBAE)
