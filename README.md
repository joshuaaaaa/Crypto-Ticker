# 🪙 Home Assistant Crypto Ticker

[🇬🇧 English](README.md) | [🇨🇿 Čeština](README_CZ.md)

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


https://github.com/heyajohnny/cryptoinfo

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

3. Copy it to `/config/www/` folder

## Configuration

### Basic Configuration

```yaml
type: iframe
url: /local/crypto_ticker.html
grid_options:
  rows: 2
  columns: full
aspect_ratio: "10" 
```


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
![Animace](https://github.com/user-attachments/assets/6946fd2f-0dbd-4b24-bde1-49bce5ad1bd5)


---

## 🧑‍💻 Author
**Joshua**  
Created for the Home Assistant community ❤️  

🔗 [https://github.com/joshuaaaaa](https://github.com/joshuaaaaa)

## http://buymeacoffee.com/jakubhruby


<img width="150" height="150" alt="qr-code" src="https://github.com/user-attachments/assets/2581bf36-7f7d-4745-b792-d1abaca6e57d" />

