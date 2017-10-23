# face_detection_alignment
Face Detection and Alignment


## Pre-requisites
```bash
conda create -n py27_tf012 python=2.7
source activate py27_tf012
pip install jupyter
pip install --upgrade ipykernel
pip install scipy
conda install PIL
source activate py27_tf012
conda install -c menpo opencv3
conda install -c menpo dlib
```

(optional)install dlib on Mac
Clean up dlib installed via conda:
```bash
conda uninstall dlib
```
Install cmake and boost-bython with homebrew:
```bash
brew install cmake
brew install boost-python
```
Build dlib from source:
```bash
git clone https://github.com/davisking/dlib.git
cd dlib/
mkdir build
cd build/
cmake .. -DDLIB_USE_CUDA=0 -DUSE_AVX_INSTRUCTIONS=1; cmake --build .
cd ..
source activate py27_tf012
python setup.py install --yes USE_AVX_INSTRUCTIONS --no DLIB_USE_CUDA
```


## run preprocess.py
```bash
~/anaconda/envs/py27_tf012/bin/python preprocess.py \
--input-dir /Users/yuan/Downloads/workspace/out_aws_ibm_keras_age_not0_not2017_up_to_13248.csv_curated/inspection_not_needed_cropped_v2 \
--output-dir /Users/yuan/Downloads/workspace/out_aws_ibm_keras_age_not0_not2017_up_to_13248.csv_curated/tmp \
--crop-dim 512
```


## Reference
* https://hackernoon.com/building-a-facial-recognition-pipeline-with-deep-learning-in-tensorflow-66e7645015b8
