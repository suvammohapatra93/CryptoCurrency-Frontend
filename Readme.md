# SUVAM'S Crypto Currency Web

# Overview
This project is a simple cryptocurrency website that allows users to view the current prices of Bitcoin, Ethereum, and Dogecoin. The website features a clean design with responsive styling and integrates with the CoinGecko API to fetch real-time cryptocurrency prices.

# Features
Real-time Cryptocurrency Prices: Displays the current prices of Bitcoin, Ethereum, and Dogecoin.
Responsive Design: Optimized for various screen sizes and devices.
Modern UI: Includes a stylish navigation bar, content section, and coin listing.

### 🎨 Technologies Used

HTML5: Structure and layout of the form.

CSS3: Styling of the form, including responsiveness and design.

JavaScript: Form validation and real-time feedback on user input.

# License

This project is licensed under the MIT License.

### SUVAM MOHAPATRA ###


# API Integration

The project fetches cryptocurrency prices from the CoinGecko API. The API endpoint used is:

```script.js
https://api.coingecko.com/api/v3/simple/price?ids=bitcoin%2Cethereum%2Cdogecoin&vs_currencies=usd
```

```script.js
let settings = {
  async: true,
  crossDomain: true,
  url: "https://api.coingecko.com/api/v3/simple/price?ids=bitcoin%2Cethereum%2Cdogecoin&vs_currencies=usd",
  method: "GET",
  headers: {},
};

$.ajax(settings).done(function (response) {
  btc.innerHTML = response.bitcoin.usd;
  eth.innerHTML = response.ethereum.usd;
  doge.innerHTML = response.dogecoin.usd;
});
```

```index.html(Before complete of head tag)
<script
      src="https://code.jquery.com/jquery-3.7.1.js"
      integrity="sha256-eKhayi8LEQwp4NKxN+CfCh+3qOVUtJn3QNZ0TciWLP4="
      crossorigin="anonymous"></script>
```