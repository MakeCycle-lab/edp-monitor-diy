# iPad Series Adapters: Device-Specific Resources

This directory contains specialized adapters, enclosures, and accessory files for various iPad models. 

### 🧩 Modular Hardware Design

This project uses a decoupled architecture between the **Mainboard**, **Touch Controller**, and **Device Adapters**. To complete your project, follow this specific workflow:

1.  **Check the Device Documentation**: Find your iPad model in the folders below and open its `README.md`. It will specify which **Mainboard** and **Touch Controller** are required for that specific device.
2.  **Locate the Mainboard**: Navigate to the **[`dptoipad-lite`](../dptoipad-lite/)** directory in the repository root to find the designated driver board.
3.  **Locate the Touch Controller**: The touch boards live in a separate repository: **[touch-controllers](https://github.com/MakeCycle-lab/touch-controllers)** (I2C-to-USB bridge).

## 📱 Will it work for my iPad?

Most iPads come in two versions: **Wi-Fi** and **Cellular**. They almost always use the exact same **Screen** and **Touch** hardware.

* **Example**: If you have an **iPad 3 (A1403 or A1430)**, it uses the same hardware as the Wi-Fi model (**A1416**). You can simply use the files in the **ipad-a1416** folder.
* **How to find your files**: Look up your model number (AXXXX) in the tables below to find the correct folder.

---

## ✅ Verified Models
These folders contain ready-to-use files for both the screen and touch functionality:

| Model | Lcd Adapter | Touch Adapter | 
| :--- | :--- | :--- | 
| **a1416 (iPad 3)** | Works | Works | 
| **a1474 (iPad Air 1)** | Works | In Development |  
| **a1566 (iPad Air 2)** | Works | In Development |  
| **a2197 (iPad 7)** | Same as a1474 | In Development | 
| **a1673 (Pro 9.7)** | Works | In Development | 
| **a1489 (mini 2)** | Works | In Development | 
| **a1538 (mini 4)** | Works | In Development | 
| **a2133 (mini 5)** | Same as a1538 | In Development | 

---

## 🔄 Compatibility Table
If your specific model isn't listed above, find its match here:

| Your Model | Lcd Adapter | Touch Adapter |
| :--- | :--- | :--- |
| **a1458 (iPad 4)** | ipad-a1416 | ipad-a1416 |
| **a1822 (iPad 5)** | ipad-a1474 | ipad-a1474 |
| **a1893 (iPad 6)** | ipad-a1474 | In Development |
| **a2270 (iPad 8)** | ipad-a1474 | ipad-a2197 |
| **a2602 (iPad 9)** | ipad-a1474 | ipad-a2197 |
| **a1599 (mini 3)** | ipad-a1489 | ipad-a1489 |

---

## 🛠️ How to Use
1. **Find your Model**: Check the **AXXXX** number on the back of your iPad.
2. **Find the Match**: Use the tables above to see which folder you need.
3. **Go to Folder**: Open that folder to download the files and watch the setup video.
