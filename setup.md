
# NerdMiner V2 Setup Guide: Your Bitcoin Lottery Ticket

## 1. Introduction
The NerdMiner V2 is a small device that allows you to try **Solo Bitcoin Mining**. Unlike large mining farms, this device has a very low hash rate (approximately 55-78 KH/s) and consumes about 1W of power . Think of it as a "perpetual lottery ticket"—if you are extremely lucky and find a block, the block reward (currently 3.125 BTC) is sent directly to your Bitcoin wallet .

**Important:** This guide assumes you already have a personal Bitcoin wallet. **You will need your wallet's Receive Address (Public Key) to proceed.** It is recommended to use a SegWit address (starting with `bc1q`) for maximum compatibility .

---

## 2. What's in the Box
- NerdMiner V2 Device
- USB Cable 

---

## 3. Step 1: Power On & Connect
1.  **Power the Device:** Connect the USB cable to the NerdMiner and plug it into a power source (computer, USB wall plug, etc.). The screen should light up.
> NanoMiner devices will light up a red LED to indicate power, and a blue LED when Wifi is ready.
3.  **Check the Screen:** If the device is new or has been reset, the screen will display a QR code and the credentials for its own internal WiFi network .

---

## 4. Step 2: Configure WiFi & Wallet
The NerdMiner creates its own WiFi hotspot so you can tell it how to connect to your home internet and where to send the Bitcoin.

1.  **Connect to the NerdMiner:**
    - Using your smartphone or laptop, scan the QR code on the device screen, or manually connect to the WiFi network:
        - **SSID (Network Name):** `NerdMinerAP`
        - **Password:** `MineYourCoins` 
2.  **Open the Config Page:**
    - Once connected, a setup window should open automatically. If it doesn't, open a web browser and go to `http://192.168.4.1` .
3.  **Enter Your Details:**
    - Click **"Configure WiFi"** .
    - Select your **home WiFi network** (SSID) from the list.
    - Enter your home WiFi **Password**.
    - **Crucial Step:** In the field labeled **"Your BTC Address"** , paste the public address of your personal Bitcoin wallet (e.g., `bc1q....`). **If this field is empty, the miner will not start** .
    - (Optional) You can leave the Pool settings as default (`public-pool.io`) unless you are running your own local pool .
4.  **Save & Restart:**
    - Click **"Save"** .
    - The device will restart. It will now attempt to connect to your home WiFi and start mining .
> Nano devices a blue LED will blink indicating mining activity.
---

## 5. Step 3: Reading the Display
Once the device restarts and connects to the internet, the screen will display live mining statistics :

- **KH/s:** Your current hashing speed (how fast you are guessing).
- **Valid Blocks:** **This is the number you care about.** If this changes from 0 to 1, congratulations! You mined a block, and the reward is on its way to your wallet.
- **Block Templates:** The number of different blocks your device has attempted to validate.
- **Difficulty:** The current global mining difficulty.
- **Pool:** The status of your connection to the mining pool.

---

## 6. Step 4: Device Controls & Navigation
The device has two or three buttons on the side (usually near the USB port) .

- **Top Button:**
    - *Short Press:* Changes the screen view (cycles through different data displays).
    - *Hold (5 seconds):* Resets the configuration to factory settings (erases WiFi and wallet). Use this if you change wallets or move houses .
- **Bottom Button:**
    - *Short Press:* Turns the screen on/off (the miner continues running in the background).
    - *Double Click:* Flips the screen orientation (useful if you want the USB cable on the left or right side).
- **Middle Button (if present):** Hard reset / force configuration mode .

---

## 7. Monitoring Your Progress
You do not need to look at the screen to see if you won. You can monitor your miner remotely .

1.  Open a web browser and go to: [https://web.public-pool.io](https://web.public-pool.io)
2.  Paste your **Bitcoin Wallet Address** into the search bar.
3.  You will see the hashrate and statistics for your NerdMiner(s) associated with that address.

---

## 8. Troubleshooting

| Issue | Solution |
| :--- | :--- |
| **Hashrate shows 0 KH/s** | Your Bitcoin wallet address is missing or incorrect. Hold the top button for 5 seconds to reset and re-enter the address . |
| **Cannot connect to NerdMinerAP** | Ensure you are using the password `MineYourCoins`. If the screen is frozen, unplug the USB and plug it back in . |
| **Won't connect to my home WiFi** | The NerdMiner only supports **2.4GHz** networks. Ensure your router isn't forcing 5GHz. Double-check the WiFi password . |
| **Screen is frozen/glitchy** | The device may need a hard reset. Unplug the power, hold down the top button, plug power back in while holding, then release. This forces configuration mode . |

---

## 9. Final Notes
- **Reality Check:** Your odds of finding a block with this device are extremely low. It is a learning tool and a novelty item, not an investment vehicle .
- **Fan Connection:** Some cases allow for a fan. If you have one, the instructions usually involve connecting the red wire to the "3.3V" pin and black to ground (GND) for silent operation, or to "5V" for stronger cooling .

Happy Mining, and good luck!
