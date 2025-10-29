🔗 Dynamic QR Code Generator
A simple, single-file HTML, CSS, and JavaScript application that allows users to dynamically generate QR codes for various data types, including URLs, email addresses, phone numbers, and plain text.

The generator utilizes the open-source qrcode.js library to render the codes directly in the browser, offering options for customizing the protocol, data content, and colors.

✨ Features
Dynamic Data Input: Easily generate QR codes for different protocols (https://, mailto:, tel:, sms:) or plain text.

Real-time Color Customization: Instantly change the dot color and background color of the QR code using color pickers.

High Error Correction: Uses CorrectLevel.H (High) for robust scanning.

Simple, Responsive UI: A clean, easy-to-use interface built with minimal CSS.

Single File Deployment: Everything is contained within a single Qr Generator.html file, making it easy to host or run locally.

🚀 How to Use
Running Locally
Clone the repository:

Bash

git clone https://github.com/LegedsDaD/HTML-QR-Code-Generator.git
cd HTML-QR-Code-Generator
Open the file: Simply double-click on the Qr Generator.html file in your file explorer. It will open in your default web browser.

Generating a Code
Select a Protocol: Choose the appropriate prefix from the dropdown (e.g., https:// for a website, mailto: for an email). Select "Text/Plain" for any unformatted text.

Enter Data: Type the destination (URL, email, number, etc.) into the Address/Data input field.

Customize Colors (Optional): Click the color swatches next to Dot Color and BG Color to select new colors. The QR code will update immediately.

Generate: Click the "✨ Generate QR Code" button. The code is also regenerated automatically when the protocol or colors are changed, or the Enter key is pressed in the data field.

🛠️ Technology Stack
HTML5: Structure and content.

CSS3: Styling and layout.

JavaScript (ES6): Logic for handling user input and generating the QR code.

qrcode.js Library: Used for the actual QR code generation.

The library is included via a CDN:

HTML

<script src="https://cdn.jsdelivr.net/npm/qrcodejs@1.0.0/qrcode.min.js"></script>
📖 Code Structure Overview
The entire application resides in Qr Generator.html and is split into three main sections:

1. <head>
Includes the <title>, the external qrcode.js library, and the <style> block containing all the custom CSS for a modern, clean look.

2. <body> (HTML Structure)
The main UI is defined here:

#controls: Contains the <select> for protocols, the text <input> for data, and the color <input type="color"> elements.

#generateBtn: The trigger button.

#qrcode: An empty <div> that serves as the container where the qrcode.js library renders the final QR code (as a <canvas> or <table>).

3. <script> (JavaScript Logic)
Element References: All necessary DOM elements are referenced (e.g., protocolSelect, addressInput, qrContainer).

generateQR() Function: The core function that:

Collects the current values for protocol, address, and colors.

Constructs the full data string (protocol + address).

Initializes or re-initializes the QRCode object with the new settings, clearing any old code first (qrContainer.innerHTML = '';).

Event Listeners: Listeners are set up on the button click, color inputs, protocol select change, and the Enter key on the address input to trigger the generateQR function.

Initial Load: window.onload = generateQR; ensures a default QR code is visible when the page first loads.

🤝 Contribution
Feel free to fork the repository, open issues, or submit pull requests with improvements!

📝 License
This project is open-source and available under the MIT License.
