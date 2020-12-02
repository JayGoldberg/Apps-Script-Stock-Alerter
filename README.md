# Apps-Script-Stock-Alerter
Apps Script Stock Alerter is a Google Sheets-based stock watcher that triggers several alert types from a watchlist

## Planned features
- Set bulk alerts
- Set "range" alerts when stocks break out of expected volatility
- Predictive alerts that notify just before market close that indicate likely candle close
- Microcharts in the sheet

## Install
1. Copy the Google Sheet @ 
1. Create an Apps Script project using *Tools > Script Editor* in the Sheet
1. Paste the code from this project into the same-named files in the script editor
1. Get your apps script ID for later (oauth callback), it is in the format https://script.google.com/macros/d/<script_id>/usercallback
1. Sign up for TD Ameritrade and turn on real-time quotes for your account if not already
1. Create an API account at TD Ameritrade (separate from account creation above) at https://developer.tdameritrade.com/
1. generate a client ID and enter the callback URL for your Apps Script using *Add App* at https://developer.tdameritrade.com/user/me/apps
1. Select *StockWatcher > Settings* in the Google sheet and enter your client ID and your TD account number, click Save

## Authentication
The app requests scope *AccountAccess* which is the lowest permission in the TD API, it **cannot** make trades or transfer funds.
