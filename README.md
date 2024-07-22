# Factorynet Hackathon

FactoryNet is a project from the Digital Manufacturing Research Team at the Air Force Research Laboratory (AFRL) that aims to provide a repository of searchable, human labeled, manufacturing relevant images. The most innovative and strategic advancements in manufacturing technology are leveraging digital data to increase efficiency, eliminate errors, and realize agility. A common thread across such efforts is to integrate AI into manufacturing processes and factory environments via new technologies such as augmented reality (AR), virtual reality (VR), and advanced robotics. While AI can be an incredibly powerful tool, it requires reliable and high-quality training data. Public labeled image databases, such as ImageNET and the MNIST handwriting dataset, have become ubiquitous for training and benchmarking algorithms but are often limited for specific applications due to a lack of depth in the associated domains or lack of breadth outside a singular domain. FactoryNET will create a public open image dataset focusing on the manufacturing environment which we believe will accelerate digital manufacturing initiatives at AFRL and across the broader manufacturing community.

# Problem Statement

The most successful machine vision AI systems require large amounts of accurately labeled images for training. The AFRL FactoryNet dataset aims to build the highest quality image dataset for the manufacturing domain. By sourcing images from web scraping, photographing machine shops and factories, and receiving contributions from manufacturing partners FactoryNet has a large volume of images with wide ranging subject matter. Building this into the most useful dataset possible comes with many challenges in defining the scope, organization, and curation strategies. One such challenge, and the current development stage of the dataset, is collecting and organizing the human labels for the images. Where does the most value lie in a dataset of images with multiple unstructured labels? One way to assess the emerging value and gain insight into the patterns and trends that will guide dataset development/expansion as well as ontology design is to test the images ability to inform a classifier. In the case of a dataset with an open ended amount of labels, the classes can be defined in many ways and finding classes that stand out as well defined and successfully labeled will reveal strengths and weaknesses in the dataset. *The challenge presented is to organize/consolidate freeform labels and create classifiers that show the image recognition capabilities enabled by this dataset.* Participants should aim to sanitize and propose structure to the image label data in an intuitive way that can enable image classification. Post-organization the participants should aim to show that classes yielded are useful and accurate by demonstrating they provide enough information to train and validate a classification model. The topic areas of this problem are data sanitization, dataset design, and creation/use of AI/ML models.

A full copy of the challenge problem is included in this repo [`here`](ChallengeProblem.pdf).

# Data Description

## Files

All images and labels are stored in the folder `data`. Each image has been given a unique name using a millisecond unix timestamp. The labels for an image are stored in a csv file with the same unix timestamp. For example, [`1711609735362.csv`](data/1711609735362.csv) stores the labels for [`1711609735362.jpg`](data/1711609735362.jpg).

## Labels

Labels can be associated with different locations of their image through bounding boxes. These boxes are defined by an X coordinate, Y coordinate, height, and width. The X and Y locations define the top left location of the bounding box. The origin of the image is in the top left. Height defines the length of the bounding box in the Y while width defines the length of the bounding box in the X. Headers are not included in the CSV files. This format is defined below with an example following.

label, X coordinate, Y coordinate, height, width

### [`1711609735362.csv`](data/1711609735362.csv) Example

circular saw,177,309,286,397

* label: circular saw
* X location: 177
* Y location: 309
* height: 286
* width: 397
