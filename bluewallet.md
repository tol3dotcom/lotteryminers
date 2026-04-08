# Step-by-Step Guide: Setting up BlueWallet for NerdMiner V2

This guide will walk you through creating a new Bitcoin wallet using **BlueWallet** (a popular open-source mobile wallet) and then generating a permanent Bitcoin address to configure your **NerdMiner V2**.

## Prerequisites
- An iPhone or Android smartphone.
- Your **NerdMiner V2** device.
- Internet connection for the initial setup.

---

## Part 1: Installing and Creating a New BlueWallet

**Important:** Always download apps from the official app stores to avoid fake or malicious wallets.

### Step 1: Download and Install
1.  **iPhone users:** Open the Apple App Store and search for "BlueWallet".
2.  **Android users:** Open the Google Play Store and search for "BlueWallet".
3.  Look for the app developed by **BlueWallet LLC** (blue icon with a white "B").
4.  Tap **Install** or **Get**.

### Step 2: Create a New Wallet
1.  Open the BlueWallet app.
2.  On the welcome screen, tap **Create a new wallet** (not "Import wallet").
3.  You will see a list of wallet types. Select **Bitcoin** (not Bitcoin Testnet or Lightning).
4.  Choose a name for your wallet, e.g., `NerdMinerWallet` or `Mining Wallet`. Tap **Create**.

### Step 3: Back Up Your Seed Phrase (Critical!)
1.  BlueWallet will display a list of **12 words**. This is your **seed phrase**.
    - **⚠️ WARNING:** This phrase is the master key to your Bitcoin. Anyone with these words can steal your funds instantly.
    - **Do NOT** take a screenshot, save it in a notes app, or email it to yourself.
    - Write it down on **paper** with a pen. Store it in a safe place.
2.  Tap **Next**.
3.  Verify the seed phrase by tapping the words in the correct order as prompted.
4.  Tap **Confirm** or **Finish**.

### Step 4: Secure Your Wallet with a PIN or Biometrics
1.  You will be prompted to set a PIN code (6 digits) to unlock the app.
2.  Enter your PIN and confirm it.
3.  (Optional) Enable Face ID or Touch ID for faster access.
4.  You will now see your main wallet screen with a balance of zero and a receive button.

---

## Part 2: Creating a "No Expiration" Address for NerdMiner

Unlike exchange accounts that rotate deposit addresses, BlueWallet can generate static, permanent addresses. Since your NerdMiner will continuously mine to this address, you need one that **never expires**.

### Step 1: Navigate to the Receive Screen
1.  In the BlueWallet main screen, tap on your wallet (e.g., `NerdMinerWallet`).
2.  Tap the **Receive** button at the bottom of the screen.

### Step 2: Create a Permanent Address
1.  You will see a QR code and a Bitcoin address below it.
2.  **Important:** By default, BlueWallet generates a new address each time you tap Receive for privacy. However, previously generated addresses **remain valid forever**.
3.  To get an address that will not disappear or expire:
    - If this is the **first time** you tap Receive, the address shown is your wallet's first address. It will **never expire**.
    - Tap the **copy icon** (two overlapping squares) next to the address.
    - **Optional but recommended:** Tap the **three dots** (⋮) or label icon to add a note like "NerdMiner V2" so you remember which address is for mining.

### Step 3: Verify the Address Does Not Expire
- **In BlueWallet, addresses do not expire.** Unlike Electrum's request system, BlueWallet has no "expiry" feature for receive addresses.
- All addresses ever generated for a wallet remain valid and associated with your wallet forever.
- You can safely use the first address indefinitely.

### Step 4: Copy the Address
1.  After tapping the copy icon, the address (a long string starting with `bc1`) is now on your clipboard.
2.  **Paste it somewhere temporarily** (like a note or text message to yourself) so you can easily copy it during the NerdMiner setup, OR have BlueWallet ready to switch between apps.

---

## Part 3: Configuring the NerdMiner V2

Now that you have a permanent Bitcoin address from BlueWallet, you will insert it into the NerdMiner configuration.

### Step 1: Connect to the NerdMiner AP
1.  Plug your NerdMiner V2 into a USB power source.
2.  Wait for the screen to display **"NerdMinerAP"** .
3.  On your phone or PC, open the Wi-Fi settings.
4.  Connect to the network named **NerdMinerAP** .
5.  Use the password displayed on the NerdMiner screen, which is **`MineYourCoins`** (case-sensitive).

### Step 2: Configure the Wi-Fi and Address
1.  After connecting, a captive portal or browser window should open automatically. If it does not, open a browser and navigate to `192.168.4.1`.
2.  Click the **Configure WiFi** button.
3.  **Select your Wi-Fi:** Choose your home Wi-Fi network from the list.
4.  **Enter Wi-Fi Password:** Input the password for your home network.
5.  **Enter BTC Address:**
    - Find the field labeled **"Your BTC address"** .
    - **Important:** Delete any placeholder text (e.g., `yourBtcAddress`) entirely before pasting.
    - **On your phone:** Switch back to BlueWallet, copy the address again, then return to the browser and long-press the address field to paste.
    - **On PC:** Type or paste the address you saved earlier.
6.  **Time Zone (Optional):** Adjust the time zone offset if desired (e.g., `-5` for US Eastern Time, `0` for UTC).
7.  Click **Save**.

### Step 3: Verify the Connection
1.  The device will reboot and attempt to connect to your Wi-Fi.
2.  Check the NerdMiner screen. It should now show the Bitcoin address you entered (or a shortened version like `bc1...xxxx`) and the hashrate.
3.  To verify the miner is submitting shares, enter your BlueWallet Bitcoin address into a public pool explorer like `https://web.public-pool.io/` to see if shares are being submitted.

---

## Part 4: How to Find Your Address Again Later

If you ever need to copy the same permanent address again:

### Method 1: Use the Same Receive Screen (Easiest)
1.  Open BlueWallet and tap your wallet.
2.  Tap **Receive**.
3.  If a **new address** appears, scroll down or look for an **"Addresses"** or **"UTXOs"** section.
4.  Tap **"Show previous addresses"** or swipe left on the address list to see older addresses.
5.  Find the one you labeled "NerdMiner" and copy it.

### Method 2: Export Addresses (Advanced)
1.  Tap the **three dots** (⋮) in the top right of your wallet view.
2.  Select **Export wallet** or **View addresses**.
3.  You will see a list of all addresses ever generated for this wallet. The first address is often the most stable choice for long-term mining.

---

## Important Notes on Security and Privacy

- **BlueWallet is a Hot Wallet:** Your private keys are on your phone. Treat your phone like a cash wallet – do not store large amounts of Bitcoin long-term in a phone wallet. For significant earnings, periodically sweep funds to a hardware wallet or cold storage.
- **Seed Phrase is Everything:** BlueWallet cannot recover your funds if you lose your seed phrase. Store that paper backup securely. Never enter it into any website or app other than BlueWallet itself.
- **Address Reuse:** In Bitcoin, reusing an address is generally not recommended for privacy, but for a mining device like NerdMiner, it is **necessary and acceptable**. Your earnings will be visible on the blockchain, but the funds remain secure.
- **Deleting the Wallet:** If you delete the wallet from BlueWallet, you can restore it later using the 12-word seed phrase, and all your addresses (including the one used for mining) will be regenerated automatically.
