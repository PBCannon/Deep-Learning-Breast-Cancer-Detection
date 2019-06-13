# KNOW YOUR LEMONS 
**DEEP LEARNING & COMPUTER VISION** 
**BREAST CANCER DETECTION (MAMMOGRAM SCANS CBIS-DDSM DATABASE)**
@PBCANNON/DEEP-LEARNING-BREAST-CANCER-DETECTION

## PROJECT OVERVIEW:
In Singapore, breast cancer is the #1 diagnosed cancer in women. With a staggering 1000 new cases and 400 deaths per year, breast health is a priority for Singaporean women. The most efficient way to ensure good prognosis, is through early detection of abnormalities. In the picture above, small specks are observed in the red box. These specks are calcium deposits and are correlated with early onset of cancer. In this project, I trained a deep learning model to classify images of various abnormalities in mammogram scans. 

## PROJECT GOALS:
- Convert DICOM images to png & explore dataset
- Perform NLP on health professional diagnostic notes to classify benign & malignant abnormalities
- Label Mammogram Scans and create dataset
- Train a Deep Learning Model on mammogram scans using computer vision model

## PART 1: DATA CLEANING, DATA EXPLORATION & NLP
The first part of the project was to convert the images and extrapolate the corresponding professional diagnostic notes for each image. Medical scans are very large and need to be calibrated to fit computer vision programs. Once this was done, the quality and accuracy of labeling was assessed. Using NLP and classification models (XGBoost), the professional diagnostic predicted malignancy at 85% accuracy. Unfortunately, these notes were derived from other sources than the images, therefore the computer model with cancer as a label, could only predict cancer in 50% of the images. 

## PART 2: CREATING THE DATASET 
The presence of calcium deposits within the breast tissue is not a predictor of cancer. I decided to re-label the dataset and classify images according to the type of calcium deposit found in the mammogram scan. Macrocalcifications are usually benign and are low risk, whereas Dense or Amorphous breasts should be looked at more closely. Microcalcifications are associated with high cancer risk, whereas calcifications in blood vessels are associated with risks cardiovascular disease (CVD).


## PART 3: COMPUTER VISION MODEL 
I trained a Resnet model (resnet34) to classify each mammogram scan into one of the four labels from above. It was able to classify images at 80% accuracy. The reason for the lower score is most likely due to the limitation of the dataset. As we can see from the image, many of the images contained more than one calcification type. A multi-label classifier may be accurate at depicting the abnormalities found in the breast tissue.   


