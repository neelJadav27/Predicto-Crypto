# Predicto-Crypto
<h3>Implementation Details</h3>
The aim of the project is to use Hadoop as a database and store all the data files on Hadoop and then retrieving those files into python application to develop and test the Cryptocurrency prediction model. The implementation of project is divided into two major parts:

  1. Hadoop clusters setup and data storage
  2. Prediction model development in python

<h3>Project Architecture</h3>
<image src="https://user-images.githubusercontent.com/85033138/149033808-31d5fe8e-1e94-4d05-bf4b-93b705eb2790.png"/>

<h3>Prediction model development</h3>
The prediction model is developed in python programming language as it has a lot of extensions, libraries and documentation available for support and is a good language for developing a prediction model. The aim of the model is to predict values of a particular Cryptocurrency taking the previous data into account and also show accuracy of the model so that the user can make an informed decision with all the information available. The dataset is .cave files of 10 different Cryptocurrency selected from available Cryptocurrency on the basis of current trends and popularity. The dataset is a sequential data and changes its values with respect to time. Each .csv file of a particular currency has multiple rows of data which changes with time and shows the following attributes:
  1.Date and time: date and time with one minute of increment.
  2.Open: the opening price of the Cryptocurrency for the minute in any currency
  3.Close: the closing price of the Cryptocurrency for the minute in any currency
  4.High: the highest price of the Cryptocurrency for the minute in any currency
  5.Low: the lowest price of the Cryptocurrency for the minute in any currency
  6.Volume: the amount of coins traded(bought/sold) of the Cryptocurrency for the minute
  
All the above-mentioned attributes are very important for prediction and can help build a better model. All the other attributes present in the file were dropped before moving forward. The .csv files were imported using Fastquant API; other APIs as yfinance, binance etc were also taken into consideration however, they allowed to fetch data only up to a limited period and that would not be enough to build a model. After importing the data from API, the csv files were made and that data was stored in Hadoop Distributed file system. Once the data was stored on Hadoop cluster we need to retrieve that data in order to process and clean the data to build the model. For this, our team is using Snakebite – it is a python package developed by spotify engineering to access HDFS and allow interaction between HDFS and python application. We have used it to retrieve the .csv files and use it in preparing our model. The data is sequential and changes with time so we are performing regression analysis on the data and hence trying to predict values the Cryptocurrency will have in the future.

Once the python application has access to the data we are using multiple libraries and extensions available in python to store & process the data. These are:

<b>1. Fastquant:</b> it can access historical stock and Cryptocurrency data very quickly and takes data from binance so it can be trusted.

<b>2. Pandas:</b> pandas is a library for python for data analysis and manipulation. We are using it as our data is a numerical time series data.

<b>3. Numpy:</b> Numpy is used for adding more support in python to process large, multidimensional arrays and matrices. It also gives ability to work and process these large datasets.

<b>4. Plotly:</b> Plotly allows nonchalant creation of graphs and plots in python from any given data set. We have used it to plot our prediction values on a graph for better representation of data.

<b>5. Sklearn:</b> Sci-Kit learn is a machine learning library which includes various features to create algorithms for models. We have used it for pre-processing of our data using MinMaxScaler.

<b>6. TensorFlow:</b> TensorFlow-Keras is also a machine learning and artificial intelligence library which enables us in building deep neural networks.
