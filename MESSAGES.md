---
layout: default
title: Messages
---

<h2 style="font-size: 42px; color: #00B03B; margin-bottom: 10px;">Choose a Number, Hubby 💚</h2>
<p style="font-style: italic; color: #32874E;">“This is for you, my love so sweet! 41 simple messages! Click on any number then scroll down. Do this every 2 months starting this September.”</p>

<div class="grid" id="button-grid"></div>
<div id="message-box"></div>

<style>
  .grid {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    gap: 12px;
    max-width: 900px;
    margin: auto;
  }

  .number-button {
    font-size: 28px;
    margin: 10px;
    padding: 20px 0;
    width: 100px;
    border: none;
    border-radius: 12px;
    cursor: pointer;
    color: white;
    transition: transform 0.2s;
    text-align: center;
  }

  .number-button:hover {
    transform: scale(1.08);
    box-shadow: 0 0 10px #00B03B;
  }

  #message-box {
    margin-top: 30px;
    font-size: 28px;
    font-style: italic;
    font-weight: 500;
    color: #98D7A5;
    min-height: 60px;
    padding: 20px;
    line-height: 1.6;
    opacity: 1;
    transition: opacity 0.3s ease;
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
    button.style.backgroundColor = `hsl(140, 50%, ${30 + i}%`;
    button.onclick = () => {
      const box = document.getElementById("message-box");
      box.style.opacity = 0;
      setTimeout(() => {
        box.innerText = messages[i] || "No message yet.";
        box.style.opacity = 1;
      }, 150);
    };
    grid.appendChild(button);
  }
</script>
