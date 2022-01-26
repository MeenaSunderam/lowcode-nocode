# SageMaker Canvas

SageMaker Canvas leverages the same technology as Amazon SageMaker to automatically clean and combine your data, create hundreds of models under the hood, select the best performing one, and generate new individual or batch predictions. It supports multiple problem types such as binary classification, multi-class classification, numerical regression, and time series forecasting. These problem types let you address business-critical use cases, such as fraud detection, churn reduction, and inventory optimization, without writing a single line of code.

You can launch SageMaker Canvas from Amazon SageMaker Service.  Create a SageMaker Domain and an user.  SageMaker Studio and Canvas applications will be made available for all users.  Drop down the "Launch App" and click on Canvas

![image](https://user-images.githubusercontent.com/7538839/151232431-8fada292-ecb3-4fb6-829d-71200c221e37.png)

SageMaker Canvas UserInterface provide you with 2 key functionalities
- Datasets:  You can upload a datasets in to SageMaker Canvas
- Models: You can start building your model using the datasets in Canvas

![image](https://user-images.githubusercontent.com/7538839/151233690-e2314bdf-63bd-401a-85db-60c7776121a3.png)

### Building a Model in Canvas

1.  Click on Datasets -> Import

![image](https://user-images.githubusercontent.com/7538839/151234114-3f21b829-b4ad-4d08-ae85-95416b80d373.png)

2.  Load the dataset (Customer-Churn.csv) from the S3 bucket or directly using upload from your local machine.  To load the data to your S3 bucket, refer to the notebook "load_data.pynb"

![image](https://user-images.githubusercontent.com/7538839/151234607-4df4dc81-3430-4e98-9d44-5b1fa4944db8.png)

3.  Click on Models -> New Model. Provide a name for the model.  Now you will be able to add datasets to the Model

![image](https://user-images.githubusercontent.com/7538839/151234847-2601d5e5-2041-40d6-b9ce-bc96715669b8.png)

4.  Data Preparation on Canvas is currently limited.  You can however select columns, filter data or join multiple datasets in Canvas.  
    a.  You can view the data distribution 
    b.  Select / Drop columns of interest 
    c.  Filter data 
    d.  Join multiple datasets 
    
    For any data preparation activities, a model recipe gets created.  

![image](https://user-images.githubusercontent.com/7538839/151235437-a3619938-ff3d-4fa6-a26f-ea76b5a05f61.png)

5.  Once the data is prepared, it is time to build the model.  
    a.  Select the target variable (in this case - "Churn")
    b.  Canvas detects the type of ML problem - in this case, it identifies the problem as "Binary Classification"
    c.  Model build has 2 options - Quick Build and Standard Build
    
![image](https://user-images.githubusercontent.com/7538839/151236116-9bf4f730-43d7-4701-8220-2b958955c979.png)
 
 6.  I am selecting Quick Build.  The difference is for Quick Build, it runs through a small sample set of model candidates based on the prediction type.  However in Standard Build, it runs through a vast number of model candidates and usually take 1 - 2 hrs to complete.

![image](https://user-images.githubusercontent.com/7538839/151236576-12e079a3-eead-4240-9c33-14f388c50595.png)


