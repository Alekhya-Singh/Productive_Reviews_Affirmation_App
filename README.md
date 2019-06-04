# Productive_Reviews_Affirmation_App

The advancements in Cloud Computing has driven the explosion of e-commerce; it has become the preferred means of purchasing certain products and services. An integral part of a product/service listed on websites is the ‘Review’.  Customer reviews are very important to users and the service providers. Reviews form a crucial part in the decision-making process for a person intending on making the said purchase. Statistics suggest that 90% of customers read reviews online before visiting a business. However, not all reviews prove to be helpful - ensuring a review is ‘Productive’ would help customers and businesses immensely. 

The Productive Reviews Affirmation Application focuses on enriching the review writing process. This application augments the reviewer using Machine Learning (ML). The application helps in validating the helpfulness of review provided by the user. The ML system has been trained on existing reviews, it then processes a review and encourages the composer to provide additional details, should there be a need

The dataset chosen for the solution consists of reviews for fine-foods from Amazon and other Amazon categories. The data, sourced from Kaggle, spans a period of more than 10 years. The data consists of over 560,000 reviews up to October 2012. Link to the dataset on Kaggle- https://www.kaggle.com/snap/amazon-fine-food-reviews.

![image](https://user-images.githubusercontent.com/43326618/58918009-700b4200-8720-11e9-8e0f-fa1cb7711bf5.png)

### Implementation Steps:

    1. Data collection and storage -
        a. The dataset is over 568,0454 Amazon Fine Food Reviews scrapped from the website. This has been downloaded from Kaggle.
        b. Collected data is stored in the IBM Cloud – Object Storage. 

    2. Machine learning model using PySpark on IBM Watson studio -
        a. The stored data is then processed in a Spark runtime where the data has been wrangled, modeled and fitted into a chosen ML Algorithm. This ML model then analyzes new text(reviews) and ascertains if the review is useful or not based on the training data.
        b. The final models are then written back to Object Storage, from where it is downloaded.

    3. Local environment –
        a. Spark has been installed and configured on macOS Mojave.
        b.  The locally running Spark has been integrated with Anaconda such that the Web App created using Flask can be run using Spark as the Kernel.

    4. Web App and ML integration using Flask framework -
        a. We have developed web-app in flask framework, where ‘user review form’ with necessary field level validation has been created which can be easily linked with any different web app in future. 
        b. Above developed Machine Learning model is downloaded from cloud and is integrated with user review form and web page in the flask app main file to make it as one whole fully functional app. 

    5. Using Spark submit, the flask web server was started, and the web app was accessible through local host on port 8081. The input review string from the user is first converted into data frame, tokenized and analysed using the ML model for the usefulness prediction. 
    
![image](https://user-images.githubusercontent.com/43326618/58917967-5a961800-8720-11e9-9d7e-818789246801.png)    
    
### Performance:
 
Performance of the system is based on the accuracy of the model and how efficiently the system provides the helpfulness of the reviews. The reviews entered by the user as input should give a result that shows whether the entered text is a useful review or need to add more details. After testing the model with 15% of the data, the system reached an accuracy of 83% (on a certain randomized seed).   

### Conclusion:

Rapid evolution of Cloud Technologies has driven the boom of the online market. Due to the increased demand for online capabilities, a critical need for research in this important area is needed. Poor quality reviews hurt business as these reviews are the major reason that helps people to buy goods online. Reviews substitute the in-person analyses of a given product prior to making a purchase. Access to other people’s opinions is crucial. In this project I have built a viable solution to ensure Reviews online are Productive.


