---
title: "Tools"
layout: default
excerpt: "Tools"
sitemap: false
permalink: /tools/
---

<style>
.tools-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
    gap: 20px;
    margin-top: 20px;
}
.tool-card {
    border: 1px solid #ddd;
    border-radius: 8px;
    padding: 20px;
    text-align: center;
    transition: box-shadow 0.3s ease;
    text-decoration: none;
    color: inherit;
    display: block;
}
.tool-card:hover {
    box-shadow: 0 4px 8px rgba(0,0,0,0.1);
    text-decoration: none;
    color: inherit;
}
.tool-icon {
    font-size: 40px;
    margin-bottom: 10px;
    color: #007bff;
}
.tool-title {
    font-size: 18px;
    font-weight: bold;
    margin: 0;
}
</style>

# Tools

<div class="tools-grid">
    <a href="{{ site.url }}{{ site.baseurl }}/tools/qr/" class="tool-card">
        <div class="tool-icon">📱</div>
        <div class="tool-title">Link to QR Code</div>
    </a>
    <a href="{{ site.url }}{{ site.baseurl }}/tools/ris2bib/" class="tool-card">
        <div class="tool-icon">🔄</div>
        <div class="tool-title">RIS to BibTeX</div>
    </a>
</div>
