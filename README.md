Model trained on SNP500 data

The S&P 500 is a stock index consisting of 503 shares of 500 selected publicly traded companies with the largest capitalization on US stock exchanges.

Works on all charts, there is an example with Bitcoin

There are plans to improve and make at least a second improved version

The main idea of ​​the first version is taken from: https://github.com/krishnaik06/Stock-Price-Prediction-using-Keras-and-Recurrent-Neural-Networ

Have 4 models with different time chains 150, 60, 30, 5

From my personal observations, I can say that the 150 model most accurately predicts the price trend
and model 5 has the most tangents with the real price and is especially good in an active market

in order to try out the models, you must first download them and the stocks_v2 file

load the model via
model = keras.saving.load_model('path/150stocks.keras')

use function
X_train, X_test, y_train, y_test, sc = DataCompile(first argument, second argument)

X_train, X_test, y_train, y_test - training and test data sets
sc - value scaler (needed for vizualization of results)

first argument - dataframe column with asset price
second argument - lenght of time chain (number at the beginning of the model name)

and then for visualise results

Visualizator(sc, X_test, y_test)

displays five graphs on which the real price of the asset is drawn in red, and how the model predicted the price behavior is drawn in blue
