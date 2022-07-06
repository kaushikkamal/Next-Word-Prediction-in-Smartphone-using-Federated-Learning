# Next Word Prediction in Smartphone using Federated Learning #

In the present time, people are obsessed with using smartphones for their work, entertainment, personal affairs etc. One of the main problems faced by almost all smartphone users is that while chatting or typing anything, they have to write long sentences which at times becomes very frustrating and time-consuming. When we type using our PCs, it is not very difficult but when it comes to typing using a smartphone, which is smaller than a PC, the scenario becomes different and it gets irritating and difficult at the same time for many people. In this project, we will try to develop something for the small devices which will predict the next word(s) possible or suitable after the word(s) typed by the user. Therefore, one does not have to write the whole sentence, the algorithm will predict the next word for the user. This project will require knowledge from fields such as statistics, machine learning, federated learning, Recurrent Neural Networks (RNN) etc. We train an RNN language model using a distributed, on-device learning framework known as federated learning for the purpose of next word prediction in smartphones. The main goal of this project is to help users of small devices to text as fast as possible. Also in this project, we are going to develop a mobile application in which we will implement the algorithms of next word prediction. The implementation of federated learning into our project will help us to personalize the prediction of the next word(s) using personal writing history.

## Motivation

The motivation for this study has been the challenge of implementing federated learning. A similar problem has been commercially realised on an mobile device through the development of [Gboard](https://en.wikipedia.org/wiki/Gboard). This mobile keyboard application that is powered by features like auto-correction and next word prediction has already crossed over 1 billion downloads as recorded in 2019. Other similar applications like [Swype](https://en.wikipedia.org/wiki/Swype) and [SwiftKey](https://en.wikipedia.org/wiki/Microsoft_SwiftKey) have also employed neural networks for making prediction and gained popularity based on their improved performance.

There is an ever increasing number of users using hand-held devices like smartphones, smartwatches, sensors, and edge devices like Raspberry Pis. These generate and store a wealth of data that is mostly private but can be utilized to develop models which can prove to be much more accurate in making predictions about the users’ behavior. This can be used to optimize the performance of various intelligent applications. This has been one of the key motivations for this project which is focused on implementing next word prediction using federated learning without breaching the privacy of the users.

Another motivation behind this project is to reduce the typing time duration of the users who type using a smartphone. Some of the existing keyboard systems are extremely timeconsuming as the prediction algorithms sometimes don’t predict the words accurately and some other systems don’t consider the users’ security and store the whole users’ writing history without giving them the opportunity to select or choose the data they want to share with the system.

## Objectives

- Designing a suitable algorithm to predict the next word(s) possible after the previous
word(s) is/are typed.
- Developing a mobile application and implementing the prediction algorithm.
- Implementing federated learning to personalize the prediction of the next word(s) using
the personal writing history of users.
- Ensuring that user data is stored for learning the model only with users’ consent and
feeding only the enabled words to the model.

## Problem definition

Given the word(s) by the users, the aim is to predict all the suitable word(s) after the typed word(s) on the basis of the writing history of the respective users. To perform the predictive operation, the users’ writing history is fed to the deep learning model which is built using LSTM followed by tokenization of the words into unique integer values. The probabilities of each word occurring after the typed word(s) are calculated and the words with the highest probabilities are predicted and showed as output word(s) to the respective user.

The global model gets automatically trained periodically thereby saving the new word(s) if any used by the users. The model is saved and converted into [tensorflow lite](https://www.geeksforgeeks.org/introduction-to-tensorflow-lite/) model and used it in mobile application.

## Datasets

A [movie dialog dataset](https://www.cs.cornell.edu/~cristian/Cornell_Movie-Dialogs_Corpus.html) is used in this project. This dataset contained the dialogues of different characters of different movies.

# Implementation #

Some features and screenshots of the implementated mobile application is described below:

- ## Word prediction process

    The process in which the deep learning model does the prediction operation in a real time device using the
    mobile application is shown below:

    <br>

    <p float="centre" align="center">
        <img src="assets/how mock.png"  height="500" />
        <img src="assets/how are mock.png"  height="500" />
    </p>

- ## Restrict mode and theme switching feature

    When restrict mode is enabled, the users history will not be saved that means no violation of privacy policies. User can change the theme of the app based on their liking.

    <br>

    <p float="left" align="center">
        <img src="assets/how are restrict mock.png"  height="500" />
        <img src="assets/how are restrict white mock.png"  height="500" />  
    </p>

- ## Test on Assamese words

    The model was also trained and tested with a regional language which is Assamese.

    <br>

    <p float="left" align="center">
        <img src="assets/assamese 1 mock.png"  height="500" />
        <img src="assets/assamese 2 mock.png"  height="500" />
    </p>

- ## Updating model

    The mobile application automatically updates the model during the time period 2 am to 4 am. The screenshots while the update was going on and when the update was completed by the application are given below:

    <br>

    <p float="left" align="center">
        <img src="assets/updaing model mock.png"  height="500" />
        <img src="assets/updated model mock.png"  height="500" />
    </p>

- ## Settings page

    The mobile application consists of a settings page where the users can manage the partial appearance of the application according to their respective preferences. The features included in the settings page are as follows:

    <br>

    <p float="left" align="center"> 
        <img src="assets/settings 1 mock.png"  height="500" />
        <img src="assets/settings 2 mock.png"  height="500" />
    </p>

    <br>

    -   **Change the count of the predicted words:**  
            According to the individual needs, different users can keep different predicted word count from 2 to 10.

    -   **Change the radius of border outlines:**  
            Different users can use different shapes of the borders according to their taste.

    -   **Change the theme:**  
            According to the preferences of the users, they have the provision of using different themes.


## Full Working of the Application
    
<br>

https://user-images.githubusercontent.com/30615934/177505404-4d8b164d-8b72-4d77-9082-18a9bf95915f.mp4
    
## Collaborator

[Ojosmita Bachistha Goswami](https://github.com/Ojosmita)
