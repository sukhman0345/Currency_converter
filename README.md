# Currency_converter


Overview

# This is a simple web-based Currency Converter application that allows users to convert one currency to another using real-time exchange rates. The application is built with HTML, CSS, and JavaScript and fetches exchange rate data from an external API.

# Features

User-friendly interface with dropdown selections for currency conversion.

Automatic country flag updates based on selected currencies.

Real-time exchange rate fetching using the fetch() method.

Default selection of USD to INR for convenience.

Responsive and minimalistic design.

# Technologies Used

HTML, CSS, JavaScript for frontend development.

Flags API for displaying country flags dynamically.

Currency API (via CDN) for fetching real-time exchange rates.

# Fetch Method Usage

The project uses the JavaScript fetch() method to retrieve currency exchange rates from the external API. The following snippet demonstrates how data is fetched dynamically:

const URL = `${BASE_URL}/${fromCurr.value.toLowerCase()}/${toCurr.value.toLowerCase()}.json`;
let response = await fetch(URL);
let data = await response.json();
let rate = data[toCurr.value.toLowerCase()];
let finalAmount = amtValue * rate;
msg.innerText = `${amtValue} ${fromCurr.value} = ${finalAmount}
