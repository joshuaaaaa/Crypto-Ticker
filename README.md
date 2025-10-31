# 🪙 Home Assistant Crypto Ticker

A stylish **crypto ticker** for displaying live cryptocurrency prices directly from **Home Assistant**.  
It runs in your browser and fetches values from entities like `sensor.crypto_*` via the **Home Assistant REST API**.

---

## ✨ Features
- 🔁 Automatic updates from Home Assistant (every 10 seconds)  
- 📉 Shows price and 24h change (%)  
- 📈 Color-coded for up/down trends  
- ⏸️ Pause scrolling on hover  
- 🌙 Modern gradient design with smooth animations  

---

## ⚙️ How It Works
The ticker reads entities of this type:  
```
sensor.crypto_bitcoin
sensor.crypto_ethereum
sensor.crypto_kava
...
```
Each entity must include attributes `change_24h` and `symbol`.  
Values are fetched via the **Home Assistant REST API** (`/api/states/...`).

---

## 🧩 Installation
1. Open the file and edit configuration inside the `<script>` section:
   ```js
   const HA_URL = "http://192.168.1.1:8123"; // Your Home Assistant IP address
   const HA_TOKEN = "Your Long-Lived Access Token";
   const UPDATE_INTERVAL = 10000; // Update every 10 seconds
   ```

2. Save the file as `crypto-ticker.html`.

3. Open it in a browser or embed it in your Home Assistant dashboard  
   (for example using `panel_custom` or `browser_mod`).

---

## 🪙 Supported Coins
Default list of supported coins (you can expand it in the `COINS` array):
- Bitcoin ₿  
- Ethereum Ξ  
- Cardano ₳  
- Dogecoin Ð  
- Solana ◎  
- Ripple ✕  
- The Graph 🔺  
- Balancer 🅱️  
- …and more!  

---

## 🧠 Tips
- Hover over the ticker to pause animation.  
- To add your own coin, just extend the `COINS` array:  
  ```js
  { ha_name: 'mycoin', icon: '💰', name: 'MyCoin' }
  ```

---

## 📷 Preview
*(You can later add a GIF or screenshot of your running ticker here.)*

---

## 🧑‍💻 Author
**Joshua**  
Created for the Home Assistant community ❤️  

🔗 [https://github.com/joshuaaaaa](https://github.com/joshuaaaaa)
