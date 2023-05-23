<div id = 'top'></div>

# EMG-Signal-for-Gesture-Recognition ✋
*Machine learning based  EMG Signal analysis for Gesture Recognition* 

<div align='center'>
  
|<a href='https://drive.google.com/file/d/1D-TNMB92HCPmb8BEV5W2UBFqL8hZzKN6/view?usp=share_link'>Paper link</a>|<a href='https://archive.ics.uci.edu/ml/datasets/EMG+data+for+gestures'>Dataset link</a>|
|---|---|

<img src ="https://github.com/SaraElwatany/EMG-Signal-for-Gesture-Recognition/blob/main/snaps/Handgesture.png">

</div> 

________________________________________________

## Content

* <a href='#overview'>Overview</a>
* <a href='#code'>Code explaination</a>
* <a href='#model'>Model evaluation</a>
* <a href='#team'>Taem members</a>

________________________________________________

<div id='overview'>
  
### 1) Overview
```
-The paper we are discussing titled "Machine Learning-Based Hand Gesture Recognition via EMG Data"
 by Zehra Karapinar Senturk and Melahat Sevgul Bakay focuses on a machine learning-based 
 approach for hand gesture recognition using EMG data

-The authors explore the use of machine learning algorithms to recognize and classify specific hand gestures
 based on the patterns observed in the EMG signals.

-Our main application is virtual rehabilitation by combining gesture recognition with VR technology. 
```
<div align='center'>

<img src ="https://github.com/SaraElwatany/EMG-Signal-for-Gesture-Recognition/blob/main/snaps/Poster.jpg">

</div>

</div> 


</div>

<div id='code'>
  
### 2) <a href='https://github.com/SaraElwatany/EMG-Signal-for-Gesture-Recognition/blob/main/CodeGuide.txt'>Code explaination</a>
  *<p align='center'>Requirements</p>*
```
sklearn == 1.2.2
numpy==1.22.4
pandas == 2.0
matplotlib == 3.6.0
scipy == 1.10.1  
``` 
#### A)Preprocessing:
preprocess the EMG raw signal data by applaying Notch filter then Band pass filter.

|`Raw EMG signal` | `Notch filtered signal` | `Band pass filtered signal` |
|---|---|----|
|<img src ='https://github.com/SaraElwatany/EMG-Signal-for-Gesture-Recognition/blob/main/snaps/rawsignal.png'>|<img src ='https://github.com/SaraElwatany/EMG-Signal-for-Gesture-Recognition/blob/main/snaps/notch.png'>|<img src ='https://github.com/SaraElwatany/EMG-Signal-for-Gesture-Recognition/blob/main/snaps/bandpass.png'>|
  
#### B) Feature extraction & selection:
After we preprocess the EMG signal , we now do feature extraction to extract the following 12 features from each of the 8 channels:

| `integrated EMG IEMG` | `simple square integrated SSI`| `Root mean squared rms` | `mean absolute value MAV` | `Variance` | `waveform length WL`| `peak to peak ptp` | `difference absolute mean value DAMV` | `difference absolute standard deviation value DASDV` | `Willison amplitude WAMP` | `min` | `max` |
|---|---|----|---|---|----|---|---|----| --- | --- | ----|

|`features`|`after extraction`|
|---|----|
|<img src ='https://github.com/SaraElwatany/EMG-Signal-for-Gesture-Recognition/blob/main/snaps/features.png'>|<img src ='https://github.com/SaraElwatany/EMG-Signal-for-Gesture-Recognition/blob/main/snaps/featuresextraction.png'>|

Then , we apply feature selection techniques *Kbest in our case*
|`Feature selection`|`Feature scores`|
|---|---|
| <img src ='https://github.com/SaraElwatany/EMG-Signal-for-Gesture-Recognition/blob/main/snaps/featuresselection.png'>| <img src ='https://github.com/SaraElwatany/EMG-Signal-for-Gesture-Recognition/blob/main/snaps/featuresscores.png'> |

#### C) Classification:
we used the following three classifiers to construct our model:
<div align='center'>
  
|`classifier`|`code`|
|-------|-------|
|`Random forest`|<img src ='https://github.com/SaraElwatany/EMG-Signal-for-Gesture-Recognition/blob/main/snaps/rf.png'>|
|`SVM`|<img src ='https://github.com/SaraElwatany/EMG-Signal-for-Gesture-Recognition/blob/main/snaps/svm.png'>|
|`MLP neural network`|<img src ='https://github.com/SaraElwatany/EMG-Signal-for-Gesture-Recognition/blob/main/snaps/mlp.png'>|
</div>  

</div>


<div id='model'>
  
### 3) Model evaluation
*<p align='center'>Performance comparsion</p>*
<img src ='https://github.com/SaraElwatany/EMG-Signal-for-Gesture-Recognition/blob/main/snaps/comparsion.png'>  

<div align='center'>  
  
|`Classifier`|`Confusion Matrix`|
|----|----|
|`SVM`|<img src ='https://github.com/SaraElwatany/EMG-Signal-for-Gesture-Recognition/blob/main/snaps/svmcm.png'>|
|`RF`|<img src ='https://github.com/SaraElwatany/EMG-Signal-for-Gesture-Recognition/blob/main/snaps/rfcm.png'>|
|`MLP`|<img src ='https://github.com/SaraElwatany/EMG-Signal-for-Gesture-Recognition/blob/main/snaps/mlpcm.png'>|

</div>  
</div>

<div id='team'>
  
### Submitted by 3rd year SBME2024 students💉:
* [Aya Amr](https://github.com/ayaamrr) 
* [Sara Ayman](https://github.com/SaraElwatany) 
* [Shuaib Abdelsalam](https://github.com/ShuaibSaleh)
* [Abdelrahman Saeed](https://github.com/Abdelrahman-Yousef) 
* [Mahmoud Rabea](https://github.com/MahmoudRabea13) 
</div>

<p align="right"><a href="#top">back to top</a></p>
