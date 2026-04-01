
# Step-by-Step Guide: Setting up Electrum for NerdMiner V2

This guide will walk you through creating a new Bitcoin wallet using **Electrum** (the official software from `electrum.org`) and then generating a permanent Bitcoin address to configure your **NerdMiner V2**.

## Prerequisites
- A computer running Windows, macOS, or Linux.
- Your **NerdMiner V2** device.
- Internet connection for the initial setup.

---

## Part 1: Installing and Creating a New Electrum Wallet

**Important:** Always download software from the official source to avoid malware. Only use [https://electrum.org](https://electrum.org).

### Step 1: Download and Install
1.  Navigate to [https://electrum.org](https://electrum.org).
2.  Click the **Download** tab.
3.  Select the installer suitable for your operating system (Windows, macOS, or Linux).
4.  Run the installer and follow the installation instructions.

### Step 2: Create a New Wallet
1.  Launch the Electrum application.
2.  You will be prompted to choose a wallet name. Enter a name (e.g., `NerdMinerWallet`) and click **Next**.
3.  Select **Standard wallet** and click **Next**.
4.  Select **Create a new seed** and click **Next**.

### Step 3: Secure Your Seed Phrase
1.  Electrum will display a list of 12 (or more) words. This is your **seed phrase**.
    - **Crucial:** This phrase is the master key to your Bitcoin. Anyone with this phrase can steal your funds.
    - Write it down on paper. **Do not** take a screenshot or save it on your computer.
2.  Click **Next**.
3.  Verify the seed phrase by clicking the words in the correct order to confirm you have written it down correctly. Click **Next**.

### Step 4: Set a Password
1.  Enter a strong password to encrypt your wallet file on your computer. This password protects your wallet if your computer is lost or stolen.
2.  Confirm the password and click **Next**.
3.  Wait for the wallet to synchronize with the network (this may take a few minutes). You should now see your main wallet screen with a balance of zero.

---

## Part 2: Creating a "No Expiration" Address for NerdMiner

Unlike exchange accounts that rotate deposit addresses, Electrum can generate static, permanent addresses. To ensure your NerdMiner always has a valid address to mine to, you need to create a **static** request or use an address that does not expire.

*Note: Standard Electrum requests usually expire after 24 hours. To prevent the address from expiring, we will set the expiration to "Never" and optionally make it static.*

### Step 1: Navigate to the Receive Tab
1.  In the Electrum main window, locate the **Receive** tab (usually next to the "Send" tab).

### Step 2: Configure the Request
1.  **Description:** Enter a label to help you identify this address. Since this is for the NerdMiner, type something like "NerdMiner Mining" or "Permanent Miner". This helps you track incoming mining rewards.
2.  **Requested Amount:** Leave this **blank**. If you enter an amount here, the address will still work, but it will mark the request as "paid" after receiving that specific amount, which might cause confusion later. Leaving it blank makes it a permanent donation/receiving address.
3.  **Expiry:** This is the critical step for "no expiration".
    - Click the expiry dropdown menu.
    - Select **Never** .
    - *(Alternatively, you can uncheck "Expires after" if the checkbox is present, depending on your Electrum version).*

### Step 3: Create and Copy the Address
1.  Click the **Create Request** button.
2.  The request will appear in the list on the right side of the window.
3.  **Locate the Address:** Click on the QR code icon or the address text itself. The address (a long string starting with `bc1`, `1`, or `3`) will be displayed.
4.  **Copy:** Click the **Copy** button (usually a small clipboard icon next to the address) .

---

## Part 3: Configuring the NerdMiner V2

Now that you have a permanent Bitcoin address, you will insert it into the NerdMiner configuration.

### Step 1: Connect to the NerdMiner AP
1.  Plug your NerdMiner V2 into a USB power source.
2.  Wait for the screen to display "NerdMinerAP".
3.  On your phone or PC, open the Wi-Fi settings.
4.  Connect to the network named **NerdMinerAP**.
5.  Use the password displayed on the screen, which is **`MineYourCoins`** .

### Step 2: Configure the Wi-Fi and Address
1.  After connecting, a captive portal or browser window should open automatically. If it does not, open a browser and navigate to a page like `192.168.4.1` or follow the redirect.
2.  Click the **Configure WiFi** button .
3.  **Select your Wi-Fi:** Choose your home Wi-Fi network from the list.
4.  **Enter Wi-Fi Password:** Input the password for your home network.
5.  **Enter BTC Address:**
    - Find the field labeled **"Your BTC address"** .
    - **Important:** Delete the placeholder text (e.g., `yourBtcAddress`) entirely before pasting .
    - Paste the Bitcoin address you copied from Electrum.
6.  **Time Zone (Optional):** Adjust the time zone offset (e.g., `2` for Central European Summer Time) if desired .
7.  Click **Save**.

### Step 3: Verify the Connection
1.  The device will reboot and attempt to connect to your Wi-Fi.
2.  Check the NerdMiner screen. It should now show the Bitcoin address you entered (or a shortened version) and the hashrate.
3.  To verify the miner is submitting shares, you can enter your Bitcoin address into a public pool explorer like `https://web.public-pool.io/` to see if the worker is active .

---

## Important Notes on Addresses and Privacy

- **Address Changes:** By default, Electrum uses a new address for every transaction for privacy reasons. However, by creating a request with **Expiry set to Never**, that specific address remains valid forever. Do not delete the request from the "Receive" tab, or the NerdMiner will stop being able to deposit to it .
- **Static Address Method:** If you want to be absolutely sure the address never changes (even if you accidentally delete the request), you can go to the **Addresses** tab, right-click an unused address, and select "Freeze" or simply label it. However, using the **Receive** tab with **No Expiry** is the safest method for beginners .
- **Watching Only:** If you plan to use this wallet on a computer connected to the internet, ensure your seed phrase is stored offline. Electrum is a "hot wallet" on your PC; treat it with the same security as cash.
