# Replication Study of Self-Attentive Classification-Based Anomaly Detection in Unstructured Logs
 
 This repository contains the replicated implementation of [Self-attentive classification-based anomaly detection in unstructured logs](https://ieeexplore.ieee.org/document/9338283) for NLP class of fall 2022.
 
  Logsy is a classification-based method to learn log representations that allow to distinguish between normal system log data and anomaly samples from auxiliary log datasets, easily accessible via the internet. The idea behind such an approach to anomaly detection is that the auxiliary dataset is sufficiently informative to enhance the representation of the normal data, yet diverse to regularize against overfitting and improve generalization. We replicate the study of LogSy. Taking advantage of semantic-aware classification of log sequences, a sequence of log messages, LogSy outperforms its baselines, PCA and DeepLog. We replicate LogSy experiments with its original publicly available data sets and add an analysis of detection time. Our results confirm the superior performance of LogSy and its fast detection compared to its baselines. We also provide practical suggestions and possible future works.
 
 ![Test Image 1](/diagram.JPG)

##  Dataset
[Thunderbird (1.9 GB)](http://0b4af6cdc2f0c5998459-c0245c5c937c5dedcca3f1764ecc9b2f.r43.cf2.rackcdn.com/hpc4/tbird2.gz) & [Spirit (864 MB)](http://0b4af6cdc2f0c5998459-c0245c5c937c5dedcca3f1764ecc9b2f.r43.cf2.rackcdn.com/hpc4/spirit2.gz) & [Liberty (641 MB)](http://0b4af6cdc2f0c5998459-c0245c5c937c5dedcca3f1764ecc9b2f.r43.cf2.rackcdn.com/hpc4/liberty2.gz) & [BlueGene/L (60 MB)](http://0b4af6cdc2f0c5998459-c0245c5c937c5dedcca3f1764ecc9b2f.r43.cf2.rackcdn.com/hpc4/bgl2.gz) & [RAS](https://www.usenix.org/sites/default/files/4372-intrepid_ras_0901_0908_scrubbed.zip.tar)

Three target data sets, BGL, Thunderbird, and Spirit are used for this study.
In addition to them two data sets, liberty and RAS, are used only as auxiliary data.

More data and information is provided in this [website](https://www.usenix.org/cfdr-data).

 ## requirements
numpy

pandas

tqdm

keras

tensorflow

## running instruction of LogSy

1. Install the requirements.txt

``` shell script
$ pip install -r requirements.txt
```

2. Download and unzip the data sets 
then store the log files in one folder.

3. Inside the folder containing the data sets, move data_set_processing.py file there and run it:
``` shell script
$ python data_set_processing.py
```

4. Evaluate LogSy by running the jupyter notebook of each data set.

- anomaly_detection_tbird.ipynb -> LogSy with Thunderbird as target data

- anomaly_detection_bgl.ipynb -> LogSy with BGL as target data

- anomaly_detection_spirit.ipynb -> LogSy with Spirit as target data

Inside the notebooks, you can manipulate the split rates for test and train.

## running instruction of baselines
Logsy is compared with two other unsupervised methods of anomaly detection, PCA and DeepLog. 
Look at the readme files inside their folders for detailed running instruction of them.
..
