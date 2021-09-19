**Disclaimer**

Use at your own risk! Do not actually use this for anything significant. There are a lot of fundamental assumptions made and this should not be used as the basis of your financial reporting. I am not liable for any errors that occur due to the usage of this tool.

**Summary**

This file serves to merge Binance Future trades that have the same date, pair and side into one trade and export it as a CSV file. If prices are different, ie. due to a market order, then the average price is calculated. The USDT prices are then converted to AUD using RBA daily exchange rates for 2018-current given by:
https://www.rba.gov.au/statistics/historical-data.html#exchange-rates

If the exchange rate does not exist (weekend or public holiday), the adjacent date is used instead.

This script assumes that 1 USDT = 1 USD hence, RBA rates are used.


**Requirements**
*   Must be in a CSV Format
*   Trades ordered by date
*   Columns should have the following labels: 
    
    `Date(UTC) || Pair || Side || Price || Quantity || Amount || Fee || Realized Profit`
