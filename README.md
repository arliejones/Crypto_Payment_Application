# Crypto Payment Application
This program is an application that users can run to find fintech professionals from among a list of candidates, hire them, and pay them. The program integrates the Ethereum blockchain network to enable users to pay the professionals whom they hire with cryptocurrency.

----

## Technologies
This application is written in the Python programming language. The code is edited in Visual Studio Code. The Python libraries, tools, and modules used in this application are: Streamlit, web3, bip44, dataclasses, typing, dotenv, os, & requests.

[Streamlit](https://docs.streamlit.io/), [web3](https://web3py.readthedocs.io/en/stable/), [bip44](https://pypi.org/project/bip44/), [dataclasses](https://docs.python.org/3/library/dataclasses.html), [typing](https://docs.python.org/3/library/typing.html), [dotenv](https://pypi.org/project/python-dotenv/), [os](https://python101.pythonlibrary.org/chapter16_os.html), [requests](https://requests.readthedocs.io/en/latest/)


----

## Installation Guide (NEEDS UPDATE)
For the user to run their own version of this program, they must generate their own key pair using a personal mnemonic seed phrase. This can be changed in the SAMPLE.env file. 

For the program to run correctly, the user must make sure that all libraries and modules are correctly imported in the beginning of the code. This looks like:

    import pandas as pd
    import djgonwog


----

## Usage (NEEDS UPDATE)

**The program is comprised of 4 parts:**

1. Establish a Baseline Performance

In this section, the code will run to establish a baseline performance for the trading algorithm. It uses short and long window SMA values as trading signals. It uses the SVC classifier model from SKLearn's support vector machine (SVM) learning method to fit the training data and make predictions based on the testing data. The program then plots the actual returns vs the strategy returns (shown below).

![](Resources/svm.png)

This plot shows the results of the predicted strategy returns vs the actual returns. The plot shows that when the predicted strategy returns match the start of the actual returns, it learns from the model and begins to show higher returns vs the actual as time goes on. From late 2018 to 2021, the SVM model slightly outperforms the actual, showing an overall higher cumulative return. 

2. Tune the Baseline Trading Algorithm

In this section, the program will adjust the model's input features to find the best trading outcomes. It will first adjust the size of the training dataset by slicing the data into different periods. By increasing the dataset to 12 months, the prediction accuracy of the model improved. Secondly, it will adjust the window periods, but saw underperformance so will stay at original.

3. Evaluate a New Machine Learning Classifier

This section will apply the original parameters to a second machine learning model, using Logistic Regression. The program will backtest the model to evaluate its performance, shown as a plot in the visualization below.

![](Resources/lr.png)

This plot shows the new predicted strategy returns found from Logistic Regression vs the origianl actual returns. We can see that the Logistic Regression model greatly outperforms what we saw earlier in the SVM model. However, towards the end of 2021 the LR model begins to tank to meet the actual returns.

4. Create an Evaluation Report

In this program we are evaluating 2 different machine learning models to find the best trading strategy. First, we used the SVM model, which showed us better cumulative returns, but really didnt prove to be noticably profitable vs trading at the actual returns. Second, we used the Logistic Regression model. This model proved to greatly outperform the SVM model, showing almost double the cumulative returns and offering a better trading. However, it is extremely more volatile. The best trading strategy would be up to the risk profile of the trader. The SVM model proves small profits and less risk and the Logistic Regression model proves larger profits but high volatiility and more risk.

----

## Contributors

Arlie Jones

[E-mail](arliejones98@gmail.com)  |  [LinkedIn](https://www.linkedin.com/in/arlie-jones-020092159/)

----

## License

None