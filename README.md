# BrainNet
Adaptation of @titu1994's Inception v4 and Inception ResNet v4 architectures to MRI images of the human brain. The paper on these architectures is available at <a href="http://arxiv.org/pdf/1602.07261v1.pdf"><b>"Inception-v4, Inception-ResNet and the Impact of Residual Connections on Learning"</b></a>.

## PLEASE NOTE
Applying a giant network like these to voxel-wise segmentation is not an efficient approach and today there are much better methods out there. This repo serves as an example on how to run experiments on Google Cloud, not how to segment brain images.

## Experiment
This repository contains code for training the networks to segment white matter and gray matter on MRI scans from the <a href="http://www.oasis-brains.org/">The Open Access Series of Imaging Studies</a> (OASIS) archive.

To start the experiment, clone the repository and run

```
$ ./experiment.sh
```

Data is downloaded, extracted and preprocessed automatically.

## Google Cloud
Provision a Google Cloud CPU or GPU instance with `google-cloud.sh` using either of the following commands:

```
$ ./google-cloud.sh --create-cpu-instance
$ ./google-cloud.sh --create-gpu-instance
```

SSH into the instance once it is up and running, clone, and invoke `experiment.sh` from there.
