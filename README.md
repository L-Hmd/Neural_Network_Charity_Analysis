# Neural_Network_Charity_Analysis

### Overview of the analysis: 

Using machine learning, we designed and trained the deep learning neural networks model capable of predicting which organization will be successful if funded by the nonprofit foundation Alphabet Soup.

### Results:
**Data Preprocessing**
* What variable(s) are considered the target(s) for your model?
  * IS_SUCCESSFUL Column is the target variable
* What variable(s) are considered to be the features for your model?
  * The remaining columns became the features for the model.
* What variable(s) are neither targets nor features, and should be removed from the input data?
  * Columns EIN and NAME were dropped as they have no impact to the outcome.

**Compiling, Training, and Evaluating the Model**
* How many neurons, layers, and activation functions did you select for your neural network model, and why?
  * My neural network model had two hidden layers and an output layer. The first layer had 80 neurons; the second had 30. I applied the relu activation function to the 1st and 2nd layers as the relu works better with nonlinear data, and the model's training goes faster. For the output layer, I used the sigmoid function. Here are the performance metrics of this model.
   
   ![image](https://user-images.githubusercontent.com/100629325/195735418-008134d0-9b1a-4d1d-96a5-2c07e38c2882.png)

* Were you able to achieve the target model performance?
  * My model, with an accuracy rage of 72.7%, has not reached the target model performance of 75%.
  
* What steps did you take to try and increase model performance?
  * I optimized my model to increase the model performance to over 75% by the following three attempts:
    
    * Attempt #1: I adjusted the input data by dropping more features ("STATUS," "SPECIAL_CONSIDERATIONS"). I also increased the number of epochs in the training regiment from 30 to 50. The performance accuracy had reduced from 72.7% to 72.6%.
    
    ![image](https://user-images.githubusercontent.com/100629325/195692858-b3b2bc14-ab17-4e0f-b581-ede4dfcb92d3.png)

    ![image](https://user-images.githubusercontent.com/100629325/195735571-74ef79bd-d06a-4dc3-9523-a72807144c40.png)

    * Attempt #2: Adding Additional neurons to hidden layers and additional hidden layers are added. The accuracy score had further reduced to 72.5%.
      
    ![image](https://user-images.githubusercontent.com/100629325/195689709-0cb9e18b-aa62-47df-af34-c2d2a544dcab.png)
    
    ![image](https://user-images.githubusercontent.com/100629325/195735623-4d9ed5fc-4563-4e87-853d-855536d112f0.png)
    
    * Attempt #3: Changing the activation function of the output layer from "sigmoid" to "tanh." The accuracy of the model dropped down more to 72.45%
      
    ![image](https://user-images.githubusercontent.com/100629325/195735698-cb261284-5e2e-4405-ac51-020692aadcd4.png)
### Summary:

My neutral networks model did not achieve the target performance. It initially had an accuracy rate of 72.7%, and after optimization, the accuracy score decreased to 72.5%. This loss in accuracy can come from the fact that the model is overfitted. The random forest tree model is a better technique to solve this problem as it is more robust and better fitted for tabular data.
