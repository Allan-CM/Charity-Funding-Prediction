# Module 21 Report 

## Overview of the Analysis
The purpose of this analysis of this analysis was to create a neural networking model to help determine the best applicants for fudning with the best chance of success. 

## Results 

## Data Preoricessing
    1. What variables are the target(s) for your model? 
        Since we are trying to determine pplicants with the best chance of success the target 
        of my model was IS_SUCCESSFUL which basically determine if the moeny was used effectively. 
    2. What variables are the features for your model? 
        --> Affiliated section of idustry (APPLICATION_TYPE)
        --> Goverment organiization classigication (Classificaiton)
        --> Use Case for funding (USE_CASE)
        --> Organization type (ORGANIZATION)
        --> Active Status (STATUS)
        --> Income classification (INCOME_AMT)
        --> Specical considerations for application (SPECIAL_CONSIDERATIONS)
        --> Funding amoount requested (ASK_AMT)
    3. What variable(s) should be removed from the input data because they are neither targets nor features?
        --> The identificatio column (EIN/NAME) as this data would not really contribute to a comapny's success 
## Compiling, Training, and Evaluation the model
    1. How many neurons, layers, and activation functions did you select for your neural network model, and why? (Refer to Pic 1 in Resources Folder)
        --> Input Layer: I used 43 input features as this was the model/system was expecting based on our training data
        --> First hidden layer: 80 neurons were selected to increase its capacity to learn complex patters and Relu was selected as it computation effective and introduces non-linearity to the network. 
        --> Second Hidden Layer: 30 neurons were selcted to reduce dimensionlaity and overfitting from first hhidden layer inouts
        --> Output Layer: 1 neuron was used as it we want a binary classifier which is fit for 1 and 0s. Sigmoid function was used as it is best for squashing vlayues between o and 1 which is what we need for a binary classifier. 
    2. Were you able to achieve the target model performance? (Refer to Pic 2.1 and 2.2 Resouces Folder)
        No I was not able to acheieve the target model performance. The best I was able to rach was about 74.%
    3. What steps did you take in your attempts to increase model performance? (Refer to optimization jupyter notebook for workflow)
        --> In my first optimization attempt I decrease the nubmer of neurons in both layers to see if overfitting was the issue with the accuracy. 
        --> In my second optimization attempt I increased the nubmer of neurons but the accruacry did not change much. Still got very similar score form all my previous models
        --> 3rd optimization atempt: 
            --> Binned the ask amount column as i noticed 5000 dollar asking were most common rest were very small which with would create outliers. So i truend the column into a string and binned the amount based on wether the nubmer of pople asking for a given amount was about a 1000. This created two groups 5000 which was the only group which met the crtieria and the other data was labelled as other
            --> I also Increased the number of neurons in each layer but ensuring the nubmer of neurons decreased after each layer. 
            --> Added a third hidden layers 
            --> The frist 2 hidden alyer function was changed to leaky Relu as it prevents premature deactivation of neuron by better dealing with negative nubmers. 
            --> Increased the nubmer of epochs/iterations from 100 to 200. 
            This final optimization semms to increase the aacccuracy score resulting in better scores as we were getting higher nubmers earlier on but the overall score was very similar to our previous models despuite the many changes. 


Overall the deep learning nueral network did a somewhat good job of calssifying ourd ata but I would enver recommend this for practical use as the accrucary score for most models were aroudn 73%. One model I would recommend is random forst as it is an ensemble learning method thats good at measuring feature importance, can handle non-linear data, robust against overfitting, and ahndles both nubmerical and categorical data well. 
       

    
