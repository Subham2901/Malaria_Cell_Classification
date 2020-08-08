# Malaria Cell Classification
 ## Table of contents
* [Contributors](#Contributors)
* [Introduction](#Introduction)
* [Dataset & Preprocessing](#Dataset-And-Preprocessing)
* [Model Architecture](#Network-Architecture)
* [Loss Function & Optimizer](#Loss-Function-And-Optimizer)
* [Learning Rate](#Learning-Rate)
* [Result](#Result)
* [Citations](#Citations)

### Contributors:
This project is created by the joint efforts of
* [Subham Singh](https://github.com/Subham2901)
* [Sandeep Ghosh](https://github.com/Sandeep2017)
* [Amit Maity](https://github.com/Neel1097)

### Introduction:
Malaria caused by the Plasmodium parasites,
is a blood disorder, which is transmitted through the bite of a woman Anopheles mosquito. With almost 240 million cases mentioned each year, the sickness puts nearly forty percentage of the global populace at danger.  Thus,treatment of this disorder at the inital stages of occurance in the host's body is very neccessary,but for the treatment to take place the first step is the proper diagnosis of the host to detect malaria. Microscopic examinations of thick and thin blood smears for infected RBCs is commonly used for method of malaria diagnosis. Depending on the local protocol, the examination includes: 
* classifying and counting the normal and infected erythrocytes in the thin smear images; and/or 
* ountingparasites in thick smear images as specified in the WHOguidelines. Thus, the diagnostic accuracy is heavilydependent on manual expertise and can be adversely impacted by the burden posed by large scale analyses that are common in malaria endemic regionsAlternative techniques such as polymerase chain reaction (PCR) and rapid diagnostic tests (RDT) are also widely used. However,
PCR tests are limited in their performance while RDTs are less cost-effective in zones with high disease prevalence 
### Dataset and preprocessing:
We have used the [NIH malaria dataset](https://lhncbc.nlm.nih.gov/publication/pub9932),which contains 27,588 cell images with equal instances of parasitized and uninfected cells. Positive samples contained Plasmodium and negative samples contained no Plasmodium but other types of objects including staining artifacts/impurities. There are total __13,779 paratisized and 13,779 uninfected__ image samples.
#### preprocessing:
We augmented our data on the fly using the [Albumentations library](https://albumentations.ai/). We applied random flips and rotations with random changes in lighting by increasing/decreasing contrast, gamma & brightness. 
### Network Architecture:
We have created three model architecture using different API namely
* Sequential API : We have used [keras sequential API](https://keras.io/guides/sequential_model/) to build this architectire along with [keras image generators.](https://keras.io/api/preprocessing/image/)
* Functional API : We have used [funtional API](https://keras.io/guides/functional_api/) along with custom functional generator for this model architecture.
* Transfer Learning : We have used transfer learning with DenseNet201 along with functional API for this model.


