# Sun USDJPY Trading Robot

This is a sample code for the Sun USDJPY trading robot developed by the Forex Robot Easy Team. Please note that ForexRobotEasy is not the official developer of this product. This code is provided as a sample and is not intended for live trading.

For detailed reviews and trading results of the official product, please visit the [Forex Robot Easy website](https://forexroboteasy.com/forex-robot-review/sun-usdjpy-review-aggressive-scalper-for-forex-trading/).

## Description

The Sun USDJPY trading robot is an aggressive scalper designed for forex trading. It uses a martingale system to adjust the lot size and aims to take profit at a specified level while limiting losses with a stop loss level.

## Usage

To use this trading robot, you need to include the necessary libraries: Trade and Math. These libraries provide trading functions and math functions, respectively.

The robot has several constants defined:
- TP_LEVEL: Take profit level
- SL_LEVEL: Stop loss level
- INITIAL_LOT: Initial lot size
- MARTINGALE_FACTOR: Martingale factor

The global variables used in the code are:
- trade: Trading object
- currentLotSize: Current lot size
- currentProfit: Current profit
- previousProfit: Previous profit

The OnInit() function is called when the robot is initialized. It sets the initial lot size and resets the profit values.

The OnTick() function is called on each tick. It checks if there are open positions. If there are, it gets the current profit and compares it with the previous profit. If the current profit is greater, all open positions are closed and the lot size and profit values are reset. If the current profit is not greater, the lot size is adjusted using the martingale system, and a new buy order is placed with the adjusted lot size. If there are no open positions, a new buy order is placed with the initial lot size. The previous profit is updated.

The OnTradeError() function is called when there is an error during trading operations. It prints the error message.

The OnDeinit() function is called when the robot is deinitialized. It closes all open positions and prints the reason for deinitialization.

## Disclaimer

Please note that ForexRobotEasy is not the official developer of the Sun USDJPY trading robot. This code is provided as a sample and is not intended for live trading. To find the official developer of this product, please use MQL5.
