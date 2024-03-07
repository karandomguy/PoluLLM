# PoluLLM - Air Quality Forecasting with LSTM and LLMs

## Introduction

PoluLLM is a air quality forecasting project that utilizes Long Short-Term Memory (LSTM) networks and Language Model (LLM) fine-tuning approaches to predict air quality metrics in Delhi. The project is based on a dataset that includes hourly measurements of various pollutants such as CO, NO, NO2, O3, SO2, PM2.5, PM10, and NH3.

## Setup and Installation

1. Clone the repository to your local machine or Colab environment.
2. Ensure you have Python 3.6+ installed.
3. Install required dependencies:

   ```
   pip install -r requirements.txt
   ```

4. If using Colab, ensure you have the necessary extensions installed for interactive sessions:

   ```
   !pip install colab-xterm
   %load_ext colabxterm
   ```

## Data Preprocessing

1. The dataset, `delhi_aqi.csv`, contains hourly air quality measurements.
2. Data preprocessing includes handling missing values, normalizing the data using `MinMaxScaler`, and creating sequences of data for the LSTM model.
3. The processed data is then split into training and testing sets.

## Model Training

### LSTM Model

- The LSTM model with customizable parameters for input dimension, hidden dimension, number of layers, and output dimension.
- Train the model using the training set and evaluate its performance on the test set.

### LLM Fine-Tuning

- Fine-tune LLMs on air quality forecasting tasks.
- Experiment with different LLMs like Mistral, Mixtral, Phi-2, and Lag-Llama to compare their forecasting capabilities.

## Evaluation

- Computed evaluation metrics such as MSE, MAE, RMSE, and R2 score for the LSTM model.
- For LLMs, assess their zero-shot forecasting abilities and compare their performance with LSTM and other traditional time series models.

## Visualization

- Visualize the actual vs. predicted values for various pollutants to assess model performance.
- Utilize matplotlib for generating plots that showcase the forecasting accuracy of each model.

## My insights while working on this task:
1. LLMs can't do a good job at zero-shot prediction in time series forecasting unless they have been explicitly fine-tuned on doing so.
2. LSTM does a very good job here even though the dataset is very large
3. LLMs like Lag-Llama(https://huggingface.co/time-series-foundation-models/Lag-Llama) which have been trained to do time series forecasting do give exceptional results on this task(as can be seen in the graphs above) and there structure can be taken as reference for better time-series forecasting specifically for air quality forecasting.

## Contributing

Contributions to PoluLLM are welcome! Whether it's improving the models, extending the dataset, or enhancing the documentation, your input is valuable. Please submit a pull request or open an issue to discuss your ideas.

## License

This project is licensed under the MIT License. See the LICENSE file for more details.

---

For detailed instructions on how to use each component of the project, refer to the respective scripts and notebooks. If you encounter any issues or have suggestions for improvement, please open an issue or submit a pull request. Happy forecasting!
