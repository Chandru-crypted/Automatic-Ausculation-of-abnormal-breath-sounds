# Automatic-Ausculation-of-abnormal-breath-sounds

## Table of contents
* [Introduction](https://github.com/Chandru-crypted/Automatic-Ausculation-of-abnormal-breath-sounds#automatic-ausculation-of-abnormal-breath-sounds#Introduction)
* [Technologies](https://github.com/Chandru-crypted/Automatic-Ausculation-of-abnormal-breath-sounds#automatic-ausculation-of-abnormal-breath-sounds#Technologies)
* [Inspiration](https://github.com/Chandru-crypted/Automatic-Ausculation-of-abnormal-breath-sounds#automatic-ausculation-of-abnormal-breath-sounds#Inspiration)
* [Working](https://github.com/Chandru-crypted/Automatic-Ausculation-of-abnormal-breath-sounds#automatic-ausculation-of-abnormal-breath-sounds#Working) 

## Introduction(link)
This project tries a shot at classifying abnormal breath sounds, feel free to explore the below mentioned links to understand about abnoramaliity of lung or breath sounds 

https://www.respiratorytherapyzone.com/breath-sounds-guide/

https://www.practicalclinicalskills.com/heart-lung-sounds-reference-guide-details/71/Wheeze 

## Technologies
* Python 
* wavfile from scipy.io 
* numpy
* matplotlib


## Inspiration 
https://drive.google.com/file/d/1N8N9VMoAXP7eUU-TqlKf85qLXHAbE-bt/view?usp=sharing

## Working
Our code logic was based on the unique characterstics of the abnormalities, basic flow of the main programme is given below : 

1) Normalisation  
2) Classify the sound as "hard" or "soft" breath
3) Filtering sound signal
4) Finding peaks 
5) Finding the average ratio of Inhale time is to Exhale time
6) Finding the amplitude of avrage inhale and exhale breaths
7) Final classification 

To get a further idea , you can see a part of classification we have done based one the previous computed values : 


```python
elif classification_of_breath == 'Mild breath' and ratio == 1.0 : 
    print("It is Wheeze - continous sound abnormality")
elif (classification_of_breath == 'Hard breath' and ratio == 1.0 )and (comp_amp > 20):
    print("It is crackles Coarse - abnormal")
elif (classification_of_breath == 'Soft breath' and ratio == 1.0 )and (comp_amp > 2):
    print("It is crackles Fine - abnormal")
```

