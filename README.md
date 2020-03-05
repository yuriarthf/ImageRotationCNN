# Image Rotation CNN

This is a CNN system built to correct rotated images to its upright form. With the code in this repository it's possible to train a new CNN using images together with labeled targets, load the pretrained model located at the _model_ folder, predict the rotation of images, correct the images which the rotations were predicted, save the images' numpy array and image name versus prediction pair CSV.

## Prerequisities

* Create a virtual environment with the command `virtualenv -p PATH_TO_PYTHON3 ENV_FOLDER`.

* Activate the environment with `source ENV_FOLDER/bin/activate`.

* Install required packages by running `pip install -r REPOSITORY_FOLDER/requirements.txt`.

* Create a new jupyter kernel linked to the virtual environment by running `python -m ikykernel install --name='NAME_OF_THE_KERNEL'`

* Run `jupyter notebook` and browse the `Challenge.ipynb` file, change the kernel of the notebook to the one you just created and it's good to go.

### CNN architecture
The CNN architecture used was the one of the CIFAR10 example: [Keras CIFAR10 example](https://keras.io/examples/cifar10_cnn/). It performed better than the VGG16 + Dense layers architecture in the short run (small number of epochs). Though, It took a long time per epoch, so this network was only trained for 5 epochs (reaching very good results). The network could be trained for a longer perior afterwards in order to reach better results.

## Dataset used

* __Train dataset__: [Download link](https://www.dropbox.com/s/lbobq9xt3nchq5q/train.rotfaces.zip?dl=0)
* __Test dataset__: [Download link](https://www.dropbox.com/s/ustfubunhfe47mj/test.rotfaces.zip?dl=0)

__OBS:__ In order for the code to run, these datasets must be unzipped to the `data` folder. Or the code should be modified (not a hard task).

## Other files

* Zip containing the corrected images and numpy array file containing the images' arrays.\
[Download link](https://www.dropbox.com/sh/olqhll9olollrae/AADkatfskcIoiUXfhWsVVzMla?dl=0)
