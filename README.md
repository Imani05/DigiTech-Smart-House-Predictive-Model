# DigiTech Smart House Predictive Model

Welcome to the **DigiTech Smart House Predictive Model** repository! This project leverages **LSTM Neural Networks** to enhance the **energy efficiency**, **indoor air quality (IAQ)**, and **occupant comfort** in smart buildings by predicting environmental conditions such as CO2 levels, humidity, and temperature.

## Table of Contents
1. [Project Overview](#project-overview)
2. [Features](#features)
3. [Data](#data)
4. [Model Architecture](#model-architecture)
5. [Installation](#installation)
6. [Usage](#usage)
7. [Results](#results)
8. [Contributing](#contributing)
9. [License](#license)

---

## Project Overview
The **DigiTech Smart House** project is designed to improve building management systems through predictive analytics. By forecasting key indoor environmental parameters, the model allows for preemptive adjustments to HVAC and ventilation systems, leading to:
- **Optimized energy consumption**: Reducing HVAC energy usage by making more informed adjustments.
- **Improved air quality**: Predicting CO2 and VOC levels, which helps in maintaining healthy indoor environments.
- **Enhanced occupant comfort**: Stabilizing temperature and humidity to create more pleasant living and working spaces.

## Features
- **Time-series forecasting** using **LSTM Neural Networks**.
- Predicts **CO2 levels**, **humidity**, **temperature**, and other environmental metrics.
- Optimizes **energy efficiency** by forecasting environmental conditions.
- Handles **missing data** through interpolation and robust preprocessing.
- Provides **visualizations** for model performance and residuals analysis.

## Data
The model uses historical sensor data collected from the **DigiTech Smart House**, which includes:
- **CO2 levels**
- **Temperature**
- **Humidity**
- **VOC levels**
- **Light intensity**
- **Air Quality Index (IAQ)**

External data, such as weather information or occupancy data, can also be integrated for improved prediction accuracy.

## Model Architecture
The predictive model is built using a **Long Short-Term Memory (LSTM)** neural network, which is well-suited for time-series data due to its ability to capture long-term dependencies. The architecture includes:
- Two LSTM layers (64 and 32 units, respectively)
- **Dropout layers** to reduce overfitting
- **Early stopping** to prevent unnecessary training epochs
- **MinMaxScaler** for data normalization

The model predicts future environmental conditions based on the last 24 hours of historical data, allowing for proactive HVAC adjustments.

## Installation
To run the project locally, you’ll need to have **Python 3.x** installed along with several libraries.

1. Clone the repository:
   ```bash
   git clone https://github.com/imani05/digitech-smart-house.git
   cd digitech-smart-house
   ```

2. Install the required dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Run the preprocessing and model training scripts:
   ```bash
   python preprocess_data.py
   python train_model.py
   ```

## Usage
1. **Data Preprocessing**:
   - The `preprocess_data.py` script handles data cleaning, interpolation for missing values, and scaling the data using **MinMaxScaler**.
   ```bash
   python preprocess_data.py
   ```

2. **Training the LSTM Model**:
   - Train the LSTM model on historical sensor data using the `train_model.py` script.
   ```bash
   python train_model.py
   ```

3. **Making Predictions**:
   - The trained model can be used to predict future CO2 levels and other environmental parameters by using the `predict_future.py` script.
   ```bash
   python predict_future.py
   ```

4. **Visualizing Results**:
   - You can visualize the residuals, distribution of errors, and other key metrics using the `visualize_results.py` script.
   ```bash
   python visualize_results.py
   ```

## Results
- The LSTM model has demonstrated strong performance in predicting future CO2 levels, temperature, and humidity, leading to improved energy efficiency and air quality in the DigiTech Smart House.
- **Validation RMSE**: [Insert RMSE value]
- **Validation MAE**: [Insert MAE value]

## Contributing
We welcome contributions! If you'd like to contribute to this project, please follow these steps:
1. Fork the repository.
2. Create a feature branch (`git checkout -b feature-branch`).
3. Commit your changes (`git commit -m 'Add some feature'`).
4. Push to the branch (`git push origin feature-branch`).
5. Open a Pull Request.

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.


