---
layout: default
title: Messages
---

<h2>Choose a Number</h2>
<p style="font-style: italic; color: #32874E;">“Some memories don’t speak—they wait to be touched.”</p>

<div class="grid" id="button-grid"></div>
<div id="message-box"></div>

<style>
  .grid {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    gap: 12px; /* Adds spacing between buttons */
    max-width: 900px;
    margin: auto;
  }

  .number-button {
    font-size: 28px;              /* Bigger numbers */
    margin: 10px;
    padding: 20px 30px;           /* Larger clickable area */
    border: none;
    border-radius: 12px;          /* Softer, rounder corners */
    cursor: pointer;
    color: white;
    transition: transform 0.2s;
  }

  .number-button:hover {
    transform: scale(1.08);
    box-shadow: 0 0 10px #00B03B;
  }

  #message-box {
    margin-top: 30px;
    font-style: italic;
    color: #98D7A5;
    min-height: 40px;
  }
</style>

<script>
  const messages = {
    1: "Message for 1",
    2: "Message for 2",
    3: "Message for 3",
    // ... up to 41
    41: "Message for 41"
  };

  const grid = document.getElementById("button-grid");

  for (let i = 1; i <= 41; i++) {
    const button = document.createElement("button");
    button.innerText = i;
    button.className = "number-button";
    button.style.backgroundColor = `hsl(140, 50%, ${30 + i}%`; // Different green shades
    button.onclick = () => {
      document.getElementById("message-box").innerText = messages[i] || "No message yet.";
    };
    grid.appendChild(button);
  }
</script>
