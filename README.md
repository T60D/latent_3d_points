## Learning Representations And Generative Models For 3D Point Clouds
Created by <a href="http://web.stanford.edu/~optas/" target="_blank">Panos Achlioptas</a>, <a href="http://web.stanford.edu/~diamanti/" target="_blank">Olga Diamanti</a>, <a href="http://mitliagkas.github.io" target="_blank">Ioannis Mitliagkas</a>, <a href="http://geometry.stanford.edu/member/guibas/" target="_blank">Leonidas J. Guibas</a>.

<!-- ![prediction example](https://github.com/charlesq34/pointnet/blob/master/doc/teaser.png) -->

### Introduction
This work is based on our [arXiv tech report](https://arxiv.org/abs/1707.02392). We proposed a novel deep net architecture for auto-encoding point clouds. The learned representations was amenable to xxx.
<!-- You can also check our [project webpage](http://stanford.edu/~rqi/pointnet) for a deeper introduction. -->


### Citation
If you find our work useful in your research, please consider citing:

	@article{qi2016pointnet,
	  title={Learning Representations And Generative Models For 3D Point Clouds},
	  author={Achlioptas, Panos and Diamanti, Olga and Mitliagkas, Ioannis and Guibas, Leonidas J},
	  journal={arXiv preprint arXiv:1707.02392},
	  year={2017}
	}


<!-- 
### Installation

Install <a href="https://www.tensorflow.org/get_started/os_setup" target="_blank">TensorFlow</a>. You may also need to install h5py. The code has been tested with Python 2.7, TensorFlow 1.0.1, CUDA 8.0 and cuDNN 5.1 on Ubuntu 14.04.

If you are using PyTorch, you can find a third-party pytorch implementation <a href="https://github.com/fxia22/pointnet.pytorch" target="_blank">here</a>.

To install h5py for Python:
```bash
sudo apt-get install libhdf5-dev
sudo pip install h5py
```

### Usage
To train a model to classify point clouds sampled from 3D shapes:

    python train.py

Log files and network parameters will be saved to `log` folder in default. Point clouds of <a href="http://modelnet.cs.princeton.edu/" target="_blank">ModelNet40</a> models in HDF5 files will be automatically downloaded (416MB) to the data folder. Each point cloud contains 2048 points uniformly sampled from a shape surface. Each cloud is zero-mean and normalized into an unit sphere. There are also text files in `data/modelnet40_ply_hdf5_2048` specifying the ids of shapes in h5 files.

To see HELP for the training script:

    python train.py -h

We can use TensorBoard to view the network architecture and monitor the training progress.

    tensorboard --logdir log

After the above training, we can evaluate the model and output some visualizations of the error cases.

    python evaluate.py --visu

Point clouds that are wrongly classified will be saved to `dump` folder in default. We visualize the point cloud by rendering it into three-view images.

If you'd like to prepare your own data, you can refer to some helper functions in `utils/data_prep_util.py` for saving and loading HDF5 files.

### Part Segmentation
To train a model for object part segmentation, firstly download the data:

    cd part_seg
    sh download_data.sh

The downloading script will download <a href="http://web.stanford.edu/~ericyi/project_page/part_annotation/index.html" target="_blank">ShapeNetPart</a> dataset (around 1.08GB) and our prepared HDF5 files (around 346MB).

Then you can run `train.py` and `test.py` in the `part_seg` folder for training and testing (computing mIoU for evaluation).

### License
Our code is released under MIT License (see LICENSE file for details).

### TODO
Add test script for evaluation on OOS shape or point cloud data.
 -->