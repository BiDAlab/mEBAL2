![Sin titulo](https://github.com/BiDAlab/mEBAL2/blob/master/Images/mEBAL2_icon.jpg)
***
# About

mEBAL2 [1] is a new multimodal database for eyeblink detection and attention level estimation obtained from an e-learning environment, a new upgraded version from the well-known database [mEBAL](https://github.com/BiDAlab/mEBAL) [2]. This database is the largest existing public eyeblink database, with 21,100 labeled image sequences (10,550 eyeblinks and 10,550 no-blink events) and students’ cognitive activity labels synchronized with all the eyeblink data from 180 different students, while conducting a number of e-learning tasks of varying difficulty or taking a real course on HTML initiation through the edX MOOC platform. **This information is avalible on this web [[Download Database](#instructions-for-downloading-mEBAL2)].**

mEBAL2 was introduced in [arXiv technical report](https://arxiv.org/abs/2309.07880v1) and is currently under consideration at the “Pattern Recognition Letters”.

mEBAL2 has improved previous databases in terms of sample numbers in eyeblink and cognitive information. In particular, **three different sensors** are simultaneously considered: **Near Infrared (NIR)** and **RGB cameras** to capture face gestures, also an **Electroencephalography (EEG)** band to capture the cognitive activity of the user and eyeblink events.

Also, this new version of mEBAL comes with significant improvements:

- Additional 120 users with 7.550 eye blink events, making it three times bigger, and more than 2,5 million frames recorded from 180 students. Furthermore, a new real
e-learning environment has been added for monitoring purposes, specifically a MOOC.

The following sections describe the [motivation](#Motivation), [tasks](#Tasks), [sensors](#Sensors), [public database](#Database), and the mEBAL2 database will be shared with the community to move forward in this area:






The following table shows the sensors and the information captured:

![Sin titulo](http://atvs.ii.uam.es/atvs/github/mEBAL/Table1.jpg)
<br/>

# Motivation

Eyeblink has proven to be a valuable indicator in various fields such as ocular activity, attention, fatigue, emotions, etc., for this reason, eyeblink detection based on image processing has become essential regarding applications involving human behavior analysis. 

Eyeblink detection is a useful tool to improve e-learning platforms [3, 4] to get high-quality online education, for at least two reasons. **First, since the 70s, there are studies relating the eyeblink rate with cognitive activity like attention**. Recent research suggest that lower eyeblink rates can be associated with high attention periods, while higher eyeblink rates are related to low attention levels. **And second, blink detection can be used in the detection of fraud/cheating/lies** and combined with other features like heart rate, gaze tracking, micro-gestures or blood oxygen saturation, can improve the security of e-learning platforms.

However, the state of the art demonstrates that public eyeblink detectors based on image processing are far from resolving the eyeblink detection problem. At the moment, there are very few public data-driven algorithms (e.g., neural networks), mainly because of the lack of large eyeblink databases. Most existing datasets useful for research in this area, have only a few hundred samples, representing a strong restriction to train data-driven approaches (e.g. deep learning). Also, current public databases restrict their samples to RGB cameras, without using other sensors that have proven to be useful in similar tasks such as NIR cameras in gaze tracking or iris and pupil detection. In the mEBAL2 [1] article it is demonstrated that the approaches trained with both spectra (visible and NIR) have a good generalization capacity for unseen scenarios, **showing the how useful the NIR** camaras can be.

For this reason, we hope that mEBAL2 will be valuable for the scientific community, thanks to the multimodal nature: **Cognitive Activity and EyeBlink Detection**.



# Tasks

The database was divided into two groups. The first group of 60 students did a series of tasks that were carefully designed to reach certain goals, and the second group of 120 students did a real lesson from a MOOC, entitled “Introduction to Development of Web Applications” (WebApp), which is available in the [edX platform](https://www.edx.org/learn/web-development/universidad-autonoma-de-madrid-introduccion-al-desarrollo-de-aplicaciones-web?index=product&queryID=48c101d7ce1f73f79e2beaecb358ec7b&position=1&linked_from=autocomplete&c=autocomplete). 

The tasks for both groups were designed with two goals. First, to generate changes in the students’ cognitive activity such as mental load, attention, visual attention, etc., looking to cause variations of the eyeblink rate. And second, to generate a realistic setting of online assessments. The tasks can be categorized into five groups:

- **Enrollment form**: Student’s data are obtained here. This is a simple task that targets a relaxed state with attention levels between normal and low. 

- **Logical questions**: These require more complex interactions, and some of them include crosswords and mathematical problems, for the first group. For the MOOC course, some of the activities involve writing HTML codes and generating more efficient ones.

- **Visual tasks**: These demand visual attention from the students under different situations, such as: watching prerecorded classes, describing images, detecting errors in HTML code, etc. 

- **Reading tasks**: Reading documents has proven to have an impact on eyeblink rates and it’s highly common in e-learning environments. 

- **Multiple choice questions**: These are essential to help evaluate the students on assessment platforms and most Learning Management Systems provide templates to perform these assessments.




# Sensors

mEBAL2 contains synchronized information from multiple sensors while the students use an interface designed for e-learning tasks. Therefore, a multimodal acquisition framework was designed to monitor cognitive and eyeblink activity based on the [edBB platform](https://github.com/BiDAlab/edBBdb) [3, 4], an e-learning platform for remote education assessment:
   
![Sin titulo](http://atvs.ii.uam.es/atvs/github/mEBAL/Framework_mEBAL2.jpg)

   The acquisition setup consisted of the next components: 

   - An **EEG headset** by NeuroSky that captures 5 channels of electroencephalographic information **(𝛼, 𝛽,𝛾, 𝛿, 𝜃)**. These signals provide temporal information related to the cognitive activity of the student. The sensor also provides a temporal sequence with the eye blink strength. The sampling rate of the band is 1 Hz. The EEG band is used to capture the **cognitive activity of the student** and **the eye blink candidates**. **We have made a manual refinement of these eye blink candidates detected by the band to eliminate false positives**. These refined eye blinks will be used as eye blink groundtruth.
  
   - An **Intel RealSense** (model D435i), which comprises **1 RGB** and **2 NIR cameras**. It is  configured to 30 Hz, one frame every 33ms. It's known that an average blink takes 100ms to 400ms, therefore, an eye blink can take between 3 to 13 frames.
  
We used facial landmark detection to track the eyes position and classify the images as blink or no-blink based on the eye blink groundtruth.



# Database

mEBAL comprises a total of 3,000 blink samples from both eyes acquired with 1 RGB and 2 NIR cameras. Each sample comprises 19 frames (around 600 ms.) for a total number of images of **342,000** (3,000 × 19 × 2 × 3). Aspects such as the user position and changes in the illumination were considered during the acquisition in order to simulate realistic e-learning scenarios. 11 out of the 38 students used glasses.

mEBAL was collected in a constrained environment, but it is rich in pose, illumination changes, and other naturally-occurring factors. It can be seen in the next figure:
![Sin titulo](http://atvs.ii.uam.es/atvs/github/mEBAL/Examples_Blink3.jpg)


The mEBAL dataset was obtained from the **raw data provided in the [edBBdb](https://github.com/BiDAlab/edBBdb)** [3]. The eye blink and attention level information was labelled following a semi-supervised method. First, eye blink candidates were selected using the EEG band signals (eye blink strength is an attribute provided by the EEG band SDK). Second, we made a manual refinement of the eye blink samples detected by the band to eliminate false positives. Once the eye blink samples were validated, we stored the 9 frames previous and posterior to the eye blink event (19 frames in total for each eye blink). These frames can be used to exploit the temporal information proposed in some approaches of the literature. Finally, we used facial landmark detection to track the eye position.

**The video recorded during the session and the cropped eyes are provided in our contributed mEBAL database**. Additionally, we include **the cognitive temporal signals α, β,γ , δ, θ** provided by the EEG band.

The next table shows the most popular eye blink detection databases. As can be seen, all available databases comprise only a few hundred samples, however mEBAL **includes 3000 blink samples**:

![Sin titulo](http://atvs.ii.uam.es/atvs/github/mEBAL/Table_eye_blink_detection_databases3.jpg)

This means that is **8 times** larger than HUST-LEBW database, the existing database with largest number of eye blinks. Data is critical to train end-to-end approaches such as those based on neural networks. Furthermore, **mEBAL is unique in to use 3 sensors and to include the attention level**.



# Instructions for Downloading mEBAL2

1) [Download license agreement](http://atvs.ii.uam.es/atvs/files/mEBAL_License_Agreement.pdf), send by email one signed and scanned copy to **atvs@uam.es** according to the instructions given in point 2.

2) Send an email to **atvs@uam.es**, as follows:

   *Subject:* **[DATABASE: mEBAL2]**

   Body: Your name, e-mail, telephone number, organization, postal mail, purpose for which you will use the database, time and date at which you sent the email with the signed      license agreement.

3) Once the email copy of the license agreement has been received at ATVS, you will receive an email with a username, a password, and a time slot to download the database.

4) [Download the database](http://atvs.ii.uam.es/atvs/intranet/free_DB/mEBAL/), for which you will need to provide the authentication information given in step 4. After you finish the download, please notify by email to **atvs@uam.es** that you have successfully completed the transaction.

5) For more information, please contact: **atvs@uam.es**


# References


+ [2] Daza, R.; Morales, A.; Fierrez, J.; and Tolosana, R. 2020. mEBAL: A Multimodal Database for Eye Blink Detection and Attention Level Estimation. In *ACM International Conference on Multimodal Interaction*. [[pdf](https://arxiv.org/pdf/2006.05327v2.pdf)]

+ [3] Hernandez-Ortega, J.; Daza, R.; Morales, A.; Fierrez, J.; and Ortega Garcia, J. 2019. edBB: Biometrics and Behavior for Assessing Remote Education. In *AAAI Workshop on Artificial Intelligence for Education*. [[pdf](https://arxiv.org/pdf/1912.04786.pdf)]

+ [4] Daza, R.; Morales, A.; Tolosana, R.; Gomez, L. F.; Fierrez, J.; and Ortega-Garcia, J. 2023. edBB-Demo: Biometrics and Behavior Analysis for Online Educational Platforms. In *Proc. AAAI Conf. on Artificial Intelligence (Demonstration)*. [[pdf](https://arxiv.org/pdf/2211.09210.pdf)]
  
+ [3] Hernandez-Ortega, J.; Daza, R.; Morales, A.; Fierrez, J.; and Tolosana, R. 2020. Heart Rate Estimation from Face Videos for Student Assessment: Experiments on edBB. In *IEEE Computers, Software, and Applications Conference*. [[pdf](https://arxiv.org/pdf/2006.00825.pdf)]





# Contact:

For more information contact Aythami Morales, associate professor UAM at aythami.morales@uam.es

