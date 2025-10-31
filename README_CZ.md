# 🪙 Home Assistant Crypto Ticker

Stylový **krypto ticker** pro zobrazení aktuálních cen kryptoměn přímo z **Home Assistantu**.  
Ticker běží v prohlížeči a načítá hodnoty z entit typu `sensor.crypto_*` přes **Home Assistant REST API**.

---

## ✨ Funkce
- 🔁 Automatické načítání dat z Home Assistantu (každých 10 sekund)  
- 📉 Zobrazení ceny a 24h změny (%)  
- 📈 Barevné zvýraznění růstu/poklesu  
- ⏸️ Možnost zastavit animaci najetím myši  
- 🌙 Moderní vzhled s přechody a plynulou animací  

---

## ⚙️ Jak to funguje
Ticker čte entity ze senzoru typu:  
```
sensor.crypto_bitcoin
sensor.crypto_ethereum
sensor.crypto_kava
...
```
Každá entita musí mít atribut `change_24h` a `symbol`.  
Hodnoty se získávají pomocí **Home Assistant REST API** (`/api/states/...`).

---

## 🧩 Instalace
1. Otevři soubor a uprav konfiguraci v `<script>` části:
   ```js
   const HA_URL = "http://192.168.1.1:8123"; // IP adresa tvého Home Assistantu
   const HA_TOKEN = "Tvoje dlouhodobé API token";
   const UPDATE_INTERVAL = 10000; // Aktualizace každých 10 sekund
   ```

2. Ulož soubor jako `crypto-ticker.html`.

3. Spusť ho v prohlížeči nebo vlož jako **iframe** do Home Assistant dashboardu (např. pomocí `panel_custom` nebo `browser_mod`).

---

## 🪙 Podporované kryptoměny
Seznam přednastavených coinů (lze rozšířit v poli `COINS`):
- Bitcoin ₿  
- Ethereum Ξ  
- Cardano ₳  
- Dogecoin Ð  
- Solana ◎  
- Ripple ✕  
- The Graph 🔺  
- Balancer 🅱️  
- …a další  

---

## 🧠 Tipy
- Animaci můžeš pozastavit najetím kurzoru na ticker.  
- Pokud chceš přidat vlastní kryptoměnu, stačí přidat nový objekt do pole `COINS`:  
  ```js
  { ha_name: 'mycoin', icon: '💰', name: 'MyCoin' }
  ```

---

## 📷 Ukázka
*(Sem můžeš později vložit GIF nebo screenshot hotového tickeru.)*

---

## 🧑‍💻 Autor
**Joshua**  
Projekt vytvořen pro Home Assistant komunitu ❤️  

🔗 [https://github.com/joshuaaaaa](https://github.com/joshuaaaaa)
