# DeepMindBreak
Decensoring Hentai with Deep Neural Networks

This project applies an implementation of [Globally and Locally Consistent Image Completion](http://hi.cs.waseda.ac.jp/%7Eiizuka/projects/completion/data/completion_sig2017.pdf) to the problem of hentai decensorship. Using a deep fully convolutional neural network, DeepMindBreak can replace censored artwork in hentai with plausible reconstructions. The user needs to only specify the censored regions for the algorithm to run.

# Limitations

This project is EXTREMELY LIMITED in capability. It is a proof of concept of ongoing research.

The decensorship works ONLY with color hentai images that have minor bar censorship of the penis or vagina.

It does NOT work with:
- Black and white images
- Scanned hentai
- Real life porn
- Mosaic censorship
- Censorship of nipples
- Animated gifs/videos

In particular, if a vagina or penis is completely censored out, THERE IS NO HOPE OF RECOVERY.

# Dependencies

- Python 2/3
- TensorFlow 1.5
- Pillow

# Model
The pretrained model can be downloaded from https://drive.google.com/open?id=1mWHYSj0LDSbJQQxjR4hUMykQkVve2U3Q.

# Usage

## I. Decensoring hentai

The decensorship process is fairly involved. A user interface will eventually be released to streamline the process.

Using image editing software like Photoshop or GIMP, paint the areas you want to decensor the color with RGB values of (0,255,0). For each censored region, crop 128 x 128 size images containing the censored regions from your images and save them as new ".png" images.

Move the cropped images to []. Decensor the images by running

```
$ python decensor.py
```

Decensored images will be saved to the "output" directory. Paste the decensored images back into the original image.

## II. Train the pretrained model

Put the your custom dataset for training the "data/images" directory and convert images to npy format.

```
$ cd data
$ python to_npy.py
```

Train pretrained model on your custom dataset.

```
$ cd src
$ python train.py
```

The dataset will not be released. I do not want to risk trouble for distributing copyrighted pornographic material.

# To do
- Add a user interface
- Incorporate GAN loss into training

Contributions are welcome!

# License

Model is licensed under CC BY-NC 3.0 License

Code is licensed under MIT License and is modified from tadax's project [Globally and Locally Consistent Image Completion with TensorFlow ](https://github.com/tadax/glcic), which is an implementation of the paper [Globally and Locally Consistent Image Completion](http://hi.cs.waseda.ac.jp/%7Eiizuka/projects/completion/data/completion_sig2017.pdf)

Example image is property of [besmiled](https://www.pixiv.net/member.php?id=7902059) and allowed through Fair Use:

Copyright Disclaimer: Under Section 107 of the Copyright Act 1976, allowance is made for "fair use" for purposes such as criticism, comment, news reporting, teaching, scholarship and research. Fair use is a use permitted by copyright statute that might otherwise be infringing. Non-profit, educational or personal use tips the balance in favor of fair use.

---

Copyright (c) 2018 tadax, deeppomf

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.