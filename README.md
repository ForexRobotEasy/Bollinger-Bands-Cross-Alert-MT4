# Bollinger Bands Cross Alert MT4 ReadMe File

This code is an MT4 custom indicator that detects Bollinger Bands crosses and provides buy and sell signals. It was developed by the Forex Robot Easy Team and can be found on their website [here](https://www.forexroboteasy.com).

## Indicator Parameters

The indicator has the following input parameters:

- `BollingerPeriod`: Period for Bollinger Bands (default value: 20)
- `BollingerDeviation`: Standard deviation for Bollinger Bands (default value: 2.0)
- `EnableAlerts`: Enable/disable alerts (default value: true)

## Indicator Initialization

The `OnInit()` function is responsible for initializing the indicator. It sets up the indicator buffers and labels.

## Indicator Calculation

The `OnCalculate()` function is called for each bar of the chart. It calculates the Bollinger Bands and checks for crosses.

- The function iterates through the bars from the last calculated bar (`prev_calculated`) to the current bar (`rates_total`).
- It calculates the upper and lower Bollinger Bands for each bar using the `iBands()` function.
- If the close price is above the upper band, a sell signal is triggered. The `isSellSignal` flag is set to true and the `isBuySignal` flag is set to false. If alerts are enabled, an alert is triggered.
- If the close price is below the lower band, a buy signal is triggered. The `isBuySignal` flag is set to true and the `isSellSignal` flag is set to false. If alerts are enabled, an alert is triggered.
- If the close price is within the bands, both flags are set to false.

## Product Description

This code is a sample implementation of a Bollinger Bands cross alert indicator for MT4. It provides buy and sell signals based on Bollinger Bands crosses. The indicator is customizable with parameters for the Bollinger Bands period and deviation.

Please note that Forex Robot Easy is not the official developer of this product. We are only providing a sample code that can work as described in the product. To find the official developer of this product, please refer to the [MQL5](https://www.mql5.com) platform.

For detailed reviews and trading results of this product, please visit [this page](https://forexroboteasy.com/forex-robot-review/review-bollinger-bands-cross-alert-mt4-the-candle-stick-patterns-finder/).

