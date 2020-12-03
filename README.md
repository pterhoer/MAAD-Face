# MAAD-Face: A Massively Annotated Attribute Dataset for Face Images

A publicly available face dataset with 123.9M attribute annotations from 47 soft-biometric attributes.
MAAD-Face might help to develop privacy-preserving and bias-mitigating face recognition solutions.

Version 1.0 (23.09.2020)

## Table of Contents

- [Abstract](#abstract)
- [Database Properties](#database-properties)
- [Annotated Sample Images](#annotated-sample-images)
- [Download](#download)
- [Citing](#citing)
- [Acknowledgment](#acknowledgment)
- [License](#license)


## Abstract

<img src="images/maad_4_2.png" width="290" align="right" >

Soft-biometrics play an important role in face recognition and related fields since these might lead to biased performances, threatens the user, or are valuable for commercial aspects. Current face database are specifically constructed for the development of face recognition applications. Consequently, these databases contain large amount of diverse face but lack in the number of attribute annotations and the overall annotation correctness. In this work, we propose MAAD-Face, a new face database that is characterized by the large number of its high-quality attribute annotations. MAAD-Face consists of 3.3M faces of over 9k individuals. Using a novel annotation transfer-pipeline that allows an accurate label-transfer from multiple source-datasets to a target-dataset, MAAD-Face consists of 123.9M attribute annotations of 47 different binary attributes. Consequently, it provides 15 and 137 times more attribute labels than CelebA and LFW. Our investigation on the annotation quality by three human evaluators demonstrated the superiority of the MAAD-Face annotations over the other databases. Finally, we make use of the large amount of high-quality annotations from MAAD-Face to study the usefulness of soft-biometrics for recognition, providing insights about which attributes support genuine and imposter decision.

For more details, please take a look at the [Research Paper](https://arxiv.org/abs/2012.01030).

## Database Properties

MAAD-Face consists of over 3.3M face images from over 9k different subjects. It provides attribute labels for 47 soft-biometric attributes with a total number of 123.9M attribute annotations. Consequently, it provides 15 and 137 times more attribute labels than [CelebA](http://mmlab.ie.cuhk.edu.hk/projects/CelebA.html) and [LFW](http://vis-www.cs.umass.edu/lfw/). Moreover, three human evaluators analysed the correctness of the attribute annotations for CelebA, LFW and MAAD-Face. As shown in the Table below, it does not only provide more attribute annotation but also  annotations of higher quality than the other investigated databases.

<img src="images/Table_databases.png" width="700" >

The results of the human evaluation for each attribute of MAAD-Face is shown below.

<img src="images/Table_MAAD-Face_attribute_evaluation.png" width="700" >

## Annotated Sample Images

Below some sample images are shown including their corresponging 47 attribute annotations.
A positive attribute label refers to 1, a negative attribute label refers to -1, and a undefined attribute annotation is marked as 0.

<img src="images/samples.png" width="700" >

## Download

[MAAD-Face](https://github.com/pterhoer/MAAD-Face/releases/tag/MAADFACE) provides attribute annotations for the face images of the [VGGFace2](http://www.robots.ox.ac.uk/~vgg/data/vgg_face2) database. 
- To get the **face images**, please visit the [VGGFace2 webside](http://www.robots.ox.ac.uk/~vgg/data/vgg_face2/data_infor.html) and download the images.
- The **attribute annotations** of MAAD-Face are stored under [releases](https://github.com/pterhoer/MAAD-Face/releases/tag/MAADFACE). 
The annotations can be downloaded either as csv or pickle file.
- The csv-file ("MAAD-Face.csv") provides the labels for a single image in each row. The first entry of the row specifies the filename of the face image, followed by an identity marker and the 47 attribute annotations. The first row provides information for the different column entries.
- The pickle-file ("MAAD-Face.pkl") provides the same information and can be loaded as a pandas (python) dataframe.
- The attribute files contain the attribute annotations for the train- and test-set of VGGFace 2, in that order.

```
import pandas as pd
# load dataframe
maad_face = pd.read_pickle("Maad_Face.pkl") 
# convert dataframe to numpy array if necessary
maad_face.to_numpy() 
```



## Citing


If you use this work, please cite the following papers as well as the [VGGFace2](http://www.robots.ox.ac.uk/~vgg/data/vgg_face2) database.


```
@misc{maadface,
      title={{MAAD-Face}: A Massively Annotated Attribute Dataset for Face Images}, 
      author={Philipp Terh\"{o}rst and 
              Daniel F\"{a}hrmann and 
              Jan Niklas Kolf and 
              Naser Damer and 
              Florian Kirchbuchner and 
              Arjan Kuijper},
      year={2020},
      eprint={2012.01030},
      archivePrefix={arXiv},
      primaryClass={cs.CV}
}
```

```
@inproceedings{DBLP:conf/btas/TerhorstHKZDKK19,
  author    = {Philipp Terh{\"{o}}rst and
               Marco Huber and
               Jan Niklas Kolf and
               Ines Zelch and
               Naser Damer and
               Florian Kirchbuchner and
               Arjan Kuijper},
  title     = {Reliable Age and Gender Estimation from Face Images: Stating the Confidence
               of Model Predictions},
  booktitle = {10th {IEEE} International Conference on Biometrics Theory, Applications
               and Systems, {BTAS} 2019, Tampa, FL, USA, September 23-26, 2019},
  pages     = {1--8},
  publisher = {{IEEE}},
  year      = {2019},
  url       = {https://doi.org/10.1109/BTAS46853.2019.9185975},
  doi       = {10.1109/BTAS46853.2019.9185975},
  timestamp = {Mon, 14 Sep 2020 18:11:03 +0200},
  biburl    = {https://dblp.org/rec/conf/btas/TerhorstHKZDKK19.bib},
  bibsource = {dblp computer science bibliography, https://dblp.org}
}
```



## Acknowledgment
This work was supported by the German Federal Ministry of Education and Research (BMBF) as well as by the Hessen State Ministry for Higher Education, Research and the Arts (HMWK) within the National Research Center for Applied Cybersecurity (ATHENE), and in part by the German Federal Ministry of Education and Research (BMBF) through the Software Campus project.


## License

This project is licensed under the terms of the Attribution-ShareAlike 4.0 International ([CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/)) license.
All images used in this project belongs to the [VGGFace2](http://www.robots.ox.ac.uk/~vgg/data/vgg_face2). 
The copyright of the images remains with the original owners.
The copyright of the annotations remains with the Fraunhofer Institute for Computer Graphics Research IGD Darmstadt 2020.
