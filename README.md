# SAR Real Time Imaging on Raspberry Pi

This repo contains code from Kaiqi Chen and SAR Senior Design group of 21 class. The code could reconstruct the 2D image of the scanning area with the wav signal collected.

### How to setup the environment

`conda env create -f environment.yml`

### How to run the code

```
# common usage
python main.py {wav file path} {drone's velocity} {start offset} {end offset} {image save path}

# {wav file path}: directory path indicate where the wav file saved;
# {drone's velocity}: drone's moving velocity in the air [m/s];
# {start offset}: fraction of unstable velocity in the signal, '1/5' means the leading 1/5 component should be clipped
# {end offset}: fraction of unstable velocity in the signal, '1/5' means the ending 1/5 component should be clipped
# {image save path}: directory where image is expected to be exported
----------------------------------------------------------------------------------------------------------------------
# sample code base on the set-up repo
python main.py ./wav/sample.wav 2 0 0 ./images
``` 

