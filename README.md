![Sin titulo](https://lh3.googleusercontent.com/aESxNw5Dr7yYsuY7XWTULLTXvhXMD8hS0VmWHfLsHoGjyIFy-5uzXFEQC_NNFnvL3SXx0yquAjs0GwAjumFJTXH0iseBdmM_leUazNlNavxemqYsRs3mRvfK-HR9_XoMUVTKEbGLE8zEe1Y4i-UeUPUn1od-1zk8A8NHyuSkANCwYm4bYOpwKHIyPwHB7dkFrx55brNoZqtmcttIxt5vye0ddljDwo50DZlncDvBMx3Cuw54WX_VW5YjMH5Y6xI4eZxxZ0kDGN6hKoPPtfqONhcJuBCCAm8-4yRzkyUQ1quCQOZXt7ZQaa3uufdBW_hkMjSfLx3RAEOpPRLUj13qz-QiJutcH020AqIrHVqyFqMhGS1V8FU5xB-QPF24oMpR1eyDfOwBMiWDUFIxj5O0cnUG0xff9M9wF_Vt2bGV_E2fnlg1hcYrJhdF4kiowho0TQFWK58kzC9ucF-dWINzUAWwJf09RPWAaapPwCQkZz0TgDMzF1D51sJ6QKKZ8bx5WxD4u_lk4nWBc6nFxY7YiaGRFYTm7yH4RLZNn7EcwmsAyubhfOrUR2wSSNAKLqrr51DxkorVdI9k8jCUq7gBl6kOWKAdIbuV7_m9kmoZDDJp9Ap7WxEzFxUgVgvvPYKSe5RnyremNkRTbcCsZhXj0JUjicQ_xQMna43W21qZxzAp56Zn9UnaLg=w1328-h372-no)
***
# About
We present a platform for student monitoring in remote education consisting of a collection of sensors and software that capture biometric and behavioral data. We define a collection of tasks to acquire behavioral data that can be useful for facing the existing challenges in automatic student monitoring during remote evaluation. Additionally, we release an initial database including data from 20 different users completing these tasks with a set of **basic sensors:** webcam, microphone, mouse, and keyboard; and also from more **advanced sensors:** NIR camera, smartwatch, additional RGB cameras, and an EEG band. Information from the computer (e.g. system logs, MAC, IP, or web browsing history) is  also stored. **This information is avalible on this web [[Download Database](http://)].**

The following table shows the sensors and the information captured:

![Sin titulo](https://lh3.googleusercontent.com/mXGMSD09Z9qucUBldvBhV2gtBhR5SgDYVTCakRf7H3rH-RQ6F0uKCx6sCdLESPiRald2hHubPAExYXH1_0vpM6bsMkyVG4yMDFZ3w0Smz9x0u6nmIrUh6kRn8easFUw-faAs69kvP5rxdWJvYKH5Ph7lndh7V4gP26KV9d9EezgG9CKqPUfHcyH8E-GLTNFZOXCclAwXp6QV49ROYc_xVzKUX1Mzj45NAieYLf2oX1M2QYqOwHYFFb8rhiniaKFevlE2dPZIUsUO4po-7ACXYNA8Lc-OegYpUJoO0bPRHdSW1vcAklqVPiMwT8TF1kKqbIh8w9-nyoJcXMaqINy6kyblZ6764E7e3JGKSHzUQZGJPFxdqBfXI_hNCOSIGw6q7PyY45lgVm6gyl32iNJCYPEc_bM1hLGS3tHEnJ_HX2pFx0Q2sFULFmj6KA3ZWaXu26F1lvRqAJkBfda-1It6c5kQR4ZVGMKJ_AtVcaK93g1qp12xnM8x0Oxg6FvZRtA4lTOUYheoVQaVWFoHbmYHgi7aB-24-UMrDDbT__BIoRd3s_CSgQPbQ2ex6jaHuVZr3BJJB2CaR_fKCQvP4taiUwcvygo6JuhfOt3qvgio4iIJgSWXZ_I1Sef1S_B74Em_cqJdRyt0GCI6qOKpBC1mjqcjT-ULT5lnPbqrZF2AoM_B7bR4hKnmFg=w847-h334-no)


During each acquisition session each user completed three different types of tasks generating data of different nature: mouse and
keystroke dynamics, face data, and audio data among others. The tasks have been designed with two main goals in mind: i) analyse the capacity of such biometric and behavioral data for detecting anomalies during remote evaluation, and ii) study the capability of these data, i.e. EEG, ECG, or NIR video, for estimating other information about the users such as their attention level, the presence of stress, or their pulse rate.

<br/>The following sections describe the platform, the public database, the targets and share challenges with the community to advance in this area:


# Sensors

   The acquisition setup consisted of the next components: 

   - 3 individual **RGB cameras** (frontal, side, and cenital), and 1 **Intel Real-Sense** (model D435i), which is composed by 1 RGB and 2 Near Infrared sensors, and which also computes also depth images combining its 3 image channels.

   - A **Huawei Watch 2** that captures pulse information in real time and has also accelerometer, magnetometer, and gyroscope; useful to measure the arm movements.


   - An **EEG headset** by NeuroSky that captures 3 channels of electroencephalogram information. These data can be employed to know the focus level, stress, vigilance, etc. of the students
  
   - A **Personal Computer** with Microsoft Windows 10 OS, a microphone to acquire audio, a regular keyboard, a mouse, and a screen. The computer is employed both to complete the tasks and also to acquire the screen data, the mouse and keyboard dynamics, audio information during the evaluation, and several types of metadata (e.g. logging, app and web history, IP and MAC addresses, etc.)


# Tasks


The activities designed to conform the database consist of 8 different tasks that can be categorized in the following three groups:
 
 - **Enrollment form:** Its target consists in obtaining personal data of the users such as their name and surname, ID number, nationality, e-mail address, etc. This form is designed to acquire different events such as the mouse dynamics, clicks, mouse wheel, keyboard use, etc.
 
 - **Writing questions:** These comprehend questions that require a complex interaction from the user. They are oriented to measure the students’ cognitive abilities under different situations such as: solving logical problems, describing images, crosswords, finding differences, etc. Additionally, some activities have been designed to induce different states of emotions to the participants, e.g. stress or nervousness. These altered states are highly relevant when working with physiological and biological signals.
 
 - **Multiple choice questions:** These are questions aimed to detect the students’ attention and focus levels. Since multiple choice exams are largely used in online assessment platforms to evaluate their students, including these in our evaluation was essential.

The questions are selected from popular riddles and they present different levels of difficulty. The interface is designed to ensure data from different nature: free text typing (writing questions), fixed text typing (enrollment form), mouse movement (multiple choice questions), visual attention (describing images and finding differences), etc.


# Database and Challenges

The initial subset of the full database that is released with the present paper is composed by 20 users captured under controlled laboratory conditions during one session. The enrollment form includes demographic information from the user (age, gender, right-handed or left-handed). Additionally, we provide the performance (accuracy and time) achieved by each user in each specific task. Together with
the raw data obtained from the sensors, the database includes information processed to better understand and model the student behavior. This information is obtained using stateof-the-art algorithms:

- **Head Pose:** head pose (pitch, roll, and yaw) is estimated from the frontal webcam using the algorithm proposed in [1].

- **Mental State:** attention and meditation is estimated from the EEG signals according to the method developed by NeuroSky. The attention indicates the intensity of mental “focus”. The value ranges from 0 to 100. The attention level increases when a student focuses on a single thought or an external object, and decreases when distracted. The meditation indicates the level of mental relaxation. The value ranges from 0 to 100, and increases when users relax the mind and decreases when they are uneasy or stressed.

- **Face Biometrics:** size of the face (related to the distance to the front webcam) and authentication score are provided using the face detection algorithm proposed in [2] and the face authentication model [3].

Next figure shows an example of the information captured during the execution of the tasks:

![Sin titulo ](https://lh3.googleusercontent.com/t0h9gHZ7HVE4XLaqZcX1RmK0E_CT8aB7JOPIJgRvUD9SEcXNkohq1ilrGT86jzrQhhDiS5Xl-GmUPG0t68KN8DLencExf6ui4Z6CQWozarDYch6OKRhkhU2dMh4e9y2uZaecGzWW5dWFeg5HEghvJuFIamE_HkQMlQdWl2o14TWKoq0Vz7qkrnpXoqKkDpW2Kd5xeOy7RNqIkPJVZoyA1nGyXD3gLHkHBQ-LS-FLJMx4NLPePUyGPDzjBbEMX-mKAgHx5RIIohpWUDVLkBFfKvXbDRCl2QvyZjn6mM2jOgqXImKXQr2JQxEby4Ez3hZopMqRxD5EQIFD-WnCAECSq153lrkJCiRvaMM9bQxTrUllP4WBvZbJFcafP6IWm-TJEn8rQJpAHuftwwZxRkGBqUY2pcH3RUic6it8qG6-RVtCbJWFsK4OR8DRZSd6H8QVmStl-tG0zdK6n5ZZBwX5Dnp90A-eRff-IXosGjrVA2PR2RIXjnDqIRFMzx1hzezTYQAa85ZBSJLe97xRq3ETEclfzp9u0tLoEVv_IN2XWpgMWi1YWAFI1MON3udci6zoaxuybieGnYkgjrFlRjMXTC1TdJz5J38aLqqGdp29tm-C8EzrhmGmho1YEp8Rx5wshS-lZkg8OJ9PJoud60m9eJ3s76cHcBPAJT78xJeG4SH600NfD8DyNg=w836-h380-no)

We have designed an acquisition protocol incorporating all sensors presented in the previous sections.Some of the sensors are used to capture the groundtruth for the different challenges proposed. **We propose 5 challenges related to the monitorization of different behaviors relevant for e-learning platforms.**

For each challenge, we propose target and input data. The goal is to train new artificial intelligence models capable of predicting the
target from the input data.
**The 5 challenges proposed in this work are:** 

- **Challenge 1 - Attention Estimation:** an estimation of the attention level of the students during the execution of e-learning tasks is a very valuable resource. We propose to estimate the band signals (level of attention) from patterns captured from the basic sensors. The head pose and gaze estimation from the webcam, together with the mouse and keystroke dynamics can be used to predict attention of the students. **Target:** attention level obtained from the band signals. **Input:** front webcam video, mouse, and keystroke
sequences. [[Download Challenge 1](http://)]

- **Challenge 2 - Anomalous Behavior Detection:** the detection of non-allowed behaviors during the execution of evaluation tasks is an important challenge necessary to improve the trustworthiness in e-learning platforms. Ten users were instructed to perform non-allowed activities during the execution of the tasks. These activities comprise the use of material/resources with the correct responses to the questions. We propose the use of a smartphone as a non-allowed resource. These users try to hide the smartphone in their pockets. These events are labelled with a timestamp that identify the exact period when cheating really occurred.. We propose to use the basic sensors to detect these events. **Target:** detection of nonallowed events. **Input:** front webcam video, microphone, mouse, and keystroke dynamics. [[Download Challenge 2](http://)]
<br/><br/>The following image shows an example of this challenge:


<p align="center"><img src="https://lh3.googleusercontent.com/zCKm3M45FBaxdBwZIy1fKllTrSznRSwAVgy-tkI2cDhShL_Y2Xmu0esKvG6l4Oix3g_urZMNLvkgSVcfwJOQ1olv86JPTzrvV-UqUEBMddq0OpYgNxOzDF4kfwtNzvEsPSr5fPYCXqJAfQQEh3QEJSNKchNeln8c9Ep-mFGY_szw-l2mw4eAtD_p-xbCYJ_WNnrBVUczVtRZoVLsq_g5NWpFHRDxpdeSwLltLPhgDdIaNG62tnv7TAqWsXLpvq_LQ7jW9uXOEjyoQJZBPVI0VXPJecLQtPugygHJBRlvqJxnjOQzjZUbjkeRTWYY-y5QvYPTazY_kbM4CdXcTMr9waOaFQlAjykKaOPnP39K0Yj1I_a5-Ck_U6feCuRfG_EWE7mj6TJCSgHHX1QH5aBKRH3aM397Vxf5_a7jyVKFW0kvkPyFi006JeiFbu0mnPW_a7KG-oPyzO31y6bf7ej58HSFR6K425TFpUX9pTK-imhliX2AtvsOvI7WyiEJg5CyKNxX_EEoSJIJvp_zHphodr1gPahnRDLkfsecTgoxjM1qj-qh4tfpA62GbLUIEQFLgD3y4CLKgIxEwZ_sjWj6-G12urR-w-SQvaniWLmzEF4q9M733SiboYCFbxSY_BftQlAlXFUjwGO4HyVKrWxiKUu8i4JENXpkmVFVJsdh0RPK7zHxzqx-7g=w600-h272-no"></p>

- **Challenge 3 - Performance Prediction:** each task is evaluated and the performance is measured in terms of
accuracy (percentage of correct responses) and time spent to complete the task. We propose to estimate the performance of the student using both basic and advance sensors. **Target:** accuracy. **Basic Input:** front webcam video, mouse, and keystroke. **Advanced Input:** basic sensors plus pulse and EEC band signals. [[Download Challenge 3](http://)]

- **Challenge 4 - User Authentication:** student authentication is a critical step in a e-learning platforms. All users complete the same tasks, including the enrollment form that contains personal data. Data is anonymized but an ID number is provided to identify data from each user. The dataset is rich in biometric patterns useful for authentication (face, keystroke, mouse). **Target:** identity of the student. **Basic Input:** front webcam video, mouse, and keystroke dynamics. **Advanced Input:** IR cameras, smartwatch sensors, EEG band. [[Download Challenge 4](http://)]

- **Challenge 5 - Pulse Estimation:** the pulse is highly related to the emotional state and stress level of the students. In this challenge, we propose to estimate the pulse from the smartwatch using the front camera. Alternatively, the IR cameras can be used to analyse the potential of these sensors. **Target:** pulse of the student. **Basic Input:** front webcam video. **Advanced Input:** IR cameras. [[Download Challenge 5](http://)]


# Download

The information is available at the following links:

- **The initial subset of the full database** [[link](http://)]. 

- **Challenge 1.** Input data and processed data [[link](http://)].  [[TXT file](http://)] includes information about the challenge and the target proposed.

- **Challenge 2.** Input data and processed data [[link](http://)].  [[TXT file](http://)] includes information about the challenge and the target proposed.

- **Challenge 3.** Input data and processed data [[link](http://)].  [[TXT file](http://)] includes information about the challenge and the target proposed.

- **Challenge 4.** Input data and processed data [[link](http://)].  [[TXT file](http://)] includes information about the challenge and the target proposed.

- **Challenge 5.** Input data and processed data [[link](http://)].  [[TXT file](http://)] includes information about the challenge and the target proposed.





# License

Any entity using this dataset agrees to the following conditions:

THIS DATASET IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS "AS IS" AND ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE ARE DISCLAIMED. IN NO EVENT SHALL THE COPYRIGHT HOLDER BE LIABLE FOR ANY DIRECT, INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY, OR CONSEQUENTIAL DAMAGES (INCLUDING, BUT NOT LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS OR SERVICES; LOSS OF USE, DATA, OR PROFITS; OR BUSINESS INTERRUPTION) HOWEVER CAUSED AND ON ANY THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT LIABILITY, OR TORT (INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY OUT OF THE USE OF THIS SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.



# References

[1] Ruiz, N.; Chong, E.; and Rehg, J. M. 2018. Fine-Grained Head Pose Estimation Without Keypoints.


[2] Zhang, K.; Zhang, Z.; Li, Z.; and Qiao, Y. 2016. Joint face detection and alignment using multi-task cascaded convolutional networks. *IEEE Signal Processing Letters* 23(10):1499–1503.

[3] Cao, Q., et al. 2018. VGGFace2: A dataset for recognising faces across pose and age.


# Contact:

For more information contact Aythami Morales, associate professor UAM at aythami.morales@uam.es

