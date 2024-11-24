Crypto Real-Time Trading System
Overview
This project implements a real-time cryptocurrency trading system leveraging a Transformer AI Model for enhanced decision-making and optimized trade execution. The system utilizes the Alpaca API to execute trades and processes live market data to enable prompt, accurate decision-making.

Features
Integration of a Transformer model with BERT + Time embeddings for price prediction.
Real-time trade and quote data streaming and visualization.
Automatic order submission based on predictions.
Modular architecture for streamlined data collection, analysis, and trade execution.
Tools and Technologies
Programming Language: Python
Libraries and Frameworks: TensorFlow, Alpaca API, asyncio
Dependencies: Listed in requirements.txt
System Architecture


Project Structure
main.py: Core script to trigger streaming, plotting, and data loading.
market_minute.py: Extracts minute-level market data and stores it in the price_bar_minute folder.
streaming_trade.py: Collects real-time trade and quote data, saving logs to the logging folder.
live_plot.py: Visualizes live trade data.
transformer_model.py: Implements layers for the BERT + Time embeddings model.
btc_order.py: Submits Bitcoin orders based on Transformer model predictions (referenced from AlpacaHQ plug-and-play strategies).
model/: Contains the final trained Transformer model.
config.ini: Contains configuration details for the project.


Steps to Run
1. Install Dependencies
Run the following command to install all required packages:

bash
Copy code
pip install -r requirements.txt  
2. Clone the Repository
Clone the project repository using:

bash
Copy code
git clone https://github.com/ChenFengTsai/Speech_Emotion_Summary_API.git  
3. Execute Desired Functions
You can run specific functions based on your needs:

a. Get Bar Data (Minute Timeframe)
Collect minute-level market data:

bash
Copy code
python3 main.py --symbols BTC/USD ETH/USD --func collector  
b. Stream Real-Time Trade and Quote Data
Stream real-time data for analysis:

bash
Copy code
python3 main.py --symbols BTC/USD ETH/USD --func stream  
c. Live Plot Trade Data
Visualize live trading data:

bash
Copy code
python3 main.py --symbols BTC/USD ETH/USD --func plot  
d. Submit Bitcoin Order Based on Transformer Model
Submit Bitcoin trades based on predictions:

bash
Copy code
python3 main.py --func run_order --script btc_order.py  
Note: The Transformer model is currently trained only on BTC data, so predictions and order submissions are limited to Bitcoin.

Author
This project was developed by Atharv Santoshkumar More.
For queries or further information, feel free to contact me.
https://www.linkedin.com/in/atharv-more-0498b524b/