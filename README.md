## Algorithmic investment strategies using a hybrid approach LSTM-ARIMA
#### Kamil Kashif & Robert Ślepaczuk (My Supervisor)

## Description

### Aim
This project aims to check which of the used models helps obtaining the best strategy for trading equity indices for three stock exchanges (S&P 500, FTSE 100, CAC 40). The next day closing price is predicted, therefore it is a regression problem. The idea was to test ARIMA and LSTM individiaully plus the hybrid apporach where we use the residauls of ARIMA as an additional input to LSTM.

### Data
The prices are between 2000 and 2023 obtained from Yahoo! Finance. The inputs taken into control are: Closing Price, Volume, Realized Historical Volatility (VIX index for S&P 500 equity index) and in case of LSTM-ARIMA model - Residuals from ARIMA.

### Models
We use the following ML models:
- ARIMA
- LSTM
- LSTM-ARIMA
Models are implemented using `statsmodel`, `keras`, and `tensorflow` libraries.

### Performance metrics
Because our goal is to make the best investment strategy, instead of using ML evaluation metrics, we use individaully calculated performance metrics for investment strategies. Our main performance metric is **Information ratio\*\***.

### Validation approach
We use walk forward approach for validation and hyperparameter tuning. For details see `Data_nd_WFO.ipynb`.

## Project structure

- `ARIMA` - contains the relevant functions, executor files, and the results in `.csv` for the base model and the sensitivity analysis for ARIMA for each equity index.
- `LSTM` - contains the relevant functions, executor files, and the results in `.csv` for the base model and the sensitivity analysis for LSTM for each equity index.
- `LSTM-ARIMA` - contains the relevant functions, executor files, and the results in `.csv` for the base model and the sensitivity analysis for LSTM-ARIMA for each equity index.
- `PERFORMANCE_METRICS` - contains the files with calculated performance metrics for each equity index and each model. Furthermore, it also contains the calculation of portfolio equity lines and its performance metrics.
- `Report` - graphical representation of the equity lines and the performance metrics for both base model and the sensitivity analysis for each model for each equity index.
- `Data_nd_WFO.ipynb` - graphical representation of walk forward approach.
- `requirements.txt` - requirements file to run the code.
