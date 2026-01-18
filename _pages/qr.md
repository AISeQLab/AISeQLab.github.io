---
title: "QR Code Generator"
layout: default
excerpt: "Generate QR codes from URLs"
sitemap: false
permalink: /tools/qr/
---
<script src="https://cdnjs.cloudflare.com/ajax/libs/qrcodejs/1.0.0/qrcode.min.js"></script>

<style>
.tool-section {
margin-bottom: 50px;
padding: 20px;
border: 1px solid #eee;
border-radius: 5px;
}
.tool-section h2 {
margin-top: 0;
}
.form-group {
margin-bottom: 15px;
}
label {
display: block;
margin-bottom: 5px;
font-weight: bold;
}
input[type="text"] {
width: 100%;
padding: 8px;
border: 1px solid #ccc;
border-radius: 4px;
box-sizing: border-box; 
}
button {
background-color: #007bff;
color: white;
padding: 10px 15px;
border: none;
border-radius: 4px;
cursor: pointer;
}
button:hover {
background-color: #0056b3;
}
#qrcode {
margin-top: 20px;
}
</style>

# Link to QR Code

<div class="tool-section">
<div class="form-group">
<label for="url-input">Enter URL:</label>
<input type="text" id="url-input" placeholder="https://example.com">
</div>
<button onclick="generateQRCode()">Generate QR Code</button>
<div id="qrcode"></div>
</div>

<script>
// QR Code Generator
function generateQRCode() {
var url = document.getElementById("url-input").value;
var qrcodeContainer = document.getElementById("qrcode");
qrcodeContainer.innerHTML = ""; // Clear previous
if (url) {
new QRCode(qrcodeContainer, url);
}
}
</script>
