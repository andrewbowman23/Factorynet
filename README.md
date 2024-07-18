# Factorynet Hackathon

FactoryNet is a project from the Digital Manufacturing Research Team at the Air Force Research Laboratory (AFRL) that aims to provide a repository of searchable, human labeled, manufacturing relevant images. The most innovative and strategic advancements in manufacturing technology are leveraging digital data to increase efficiency, eliminate errors, and realize agility. A common thread across such efforts is to integrate AI into manufacturing processes and factory environments via new technologies such as augmented reality (AR), virtual reality (VR), and advanced robotics. While AI can be an incredibly powerful tool, it requires reliable and high-quality training data. Public labeled image databases, such as ImageNET and the MNIST handwriting dataset, have become ubiquitous for training and benchmarking algorithms but are often limited for specific applications due to a lack of depth in the associated domains or lack of breadth outside a singular domain. FactoryNET will create a public open image dataset focusing on the manufacturing environment which we believe will accelerate digital manufacturing initiatives at AFRL and across the broader manufacturing community.

# Problem Statement

# Data Description

## Files

All images and labels are stored in the folder `data`. Each image has been given a unique name using a millisecond unix timestamp. The labels for an image are stored in a csv file with the same unix timestamp. For example, `1711609735362.csv` stores the labels for `1711609735362.jpg`.

## Labels

Labels can be associated with different locations of their image through bounding boxes. These boxes are defined by an X coordinate, Y coordinate, height, and width. The origin of the image is in the top left. Height defines the length of the bounding box in the Y while width defines the length of the bounding box in the X. Headers are not included in the CSV files. This format is defined below with an example following.

label, X location, Y location, height, width

### `1711609735362.csv` Example

circular saw,177,309,286,397

* label: circular saw
* X location: 177
* Y location: 309
* height: 286
* width: 397
