# Sleep study - Detecting sleep for Insomniacs

### Introduction
Insomnia is a common sleep disorder which affects the life quality of patients. Sleep staging is an importanct step for diagnosis and treatment of insomnia. The gold standard of sleep staging is based on the measurement of PSG recordings. However, applying wearable PSG in real-world scenarios is of limitation. In this project, we are going to investigate the alternative measurements including heart rate, skin temperature and actigraphy by applying machine learning methodologies to classify sleep-wake stages.

### Dataset
The dataset is collected from about 70 insomnia patients who attended the sleep clinic at Woolcock Institute with the following measurements.
* **Sleep Staging**: The files are produced by the trained experts examining the PSG data for each epoch of 30s and classifying into one of the five stages in line with the sleep stages definition in the AASM manual. It provides ground truth labels for our sleep-wake classification.
* **Skin Temperature**: The raw data are collected by using multiple iButton devices attached to different parts (Forehead, Chest, Upperarm, Scapula, Forearm, Hand, Fingertip, Abdomen, Upperleg, Calf, Foot, Toe) of the patients in the sleep clinic. The temperature is recorded at every 15s.
* **Heart Rate**: The data is represented as beat-by-beat interval which each entry gives the time (in second, plus offset in millisecond) of a heart-beat and the duration since the previous beat.
* **Actigraphy**: Actigraphy is recorded for the patient’s movement activity through a wrist-based accelerometer device (for example, Philips Actiwatch 2) at every 30s. 

### Data Preparation
Similar to any other data project, we follow the end to end process from data collection, data extraction, cleaning, and feature engineering. Then we go through the cycle of model building, model evaluation and model tuning. And finally is the prediction on the new data set.

Like most of the real-world scenarios, the data is pretty mess. It is required to spend much time on data preparation. [A recent survey](http://www.forbes.com/sites/gilpress/2016/03/23/data-preparation-most-time-consuming-least-enjoyable-data-science-task-survey-says/) shows that data preparation is the most time consuming work. However, it paves the way to have better results if you have prepared the data precisely.

### Machine Learning Methods
We use SVM, XGBoost for classifying sleep-wake stages. 10-fold cross-validation is applied to evaluate the model performance respectively.
