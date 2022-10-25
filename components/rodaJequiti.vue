<template>
    
   <!-- TradingView Widget BEGIN -->
<div class="tradingview-widget-container">
  <div class="tradingview-widget-container__widget"></div>
  <script type="text/javascript" src="https://s3.tradingview.com/external-embedding/embed-widget-ticker-tape.js" async>
  {
  "symbols": [
    {
      "description": "BTC/USDT",
      "proName": "BINANCE:BTCUSDT"
    },
    {
      "description": "ETH/USDT",
      "proName": "BINANCE:ETHUSDT"
    },
    {
      "description": "ADA/USDT",
      "proName": "BINANCE:ADAUSDT"
    },
    {
      "description": "SOL/USDT",
      "proName": "BINANCE:SOLUSDT"
    },
    {
      "description": "BNB/USDT",
      "proName": "BINANCE:BNBUSDT"
    },
    {
      "description": "LUNA/USDT",
      "proName": "BINANCE:LUNAUSDT"
    }
  ],
  "showSymbolLogo": true,
  "colorTheme": "dark",
  "isTransparent": true,
  "displayMode": "adaptive",
  "locale": "en"
}
  </script>
</div>
<!-- TradingView Widget END -->
</template>