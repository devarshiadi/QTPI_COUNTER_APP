# 🏀 Basketball Counter App 🏀

## Overview 📌
This **Basketball Counter App** is built using **Code2Play and QTPI**, following a drag-and-drop approach similar to **MIT App Inventor**. It helps track basketball shots using an **IR sensor** and visually indicates successful shots with **RGB lights**. The app also integrates **Bluetooth connectivity** to communicate with external hardware.

> *"Don’t be afraid of failure. This is the way to succeed."* – LeBron James 🚀

---

## 📌 Components Used
### **🎨 Visible Components**
1️⃣ **ListPicker** (`CONNECT`) – Used to connect with the Bluetooth module 🔗
2️⃣ **Label** (`IR_SIGNAL`) – Displays **TRUE** or **FALSE** based on the IR sensor input 🏀
3️⃣ **Label** (`TEXT`) – Placeholder text to show the **Total Count** heading 📢
4️⃣ **Label** (`TotalCount`) – Displays the count of basketball shots (initially set to `0`) 📊
5️⃣ **Button** (`RESET`) – Resets the shot count to `0` 🔄

### **⚙️ Non-Visible Components**
🔹 **BluetoothClient** – Connects the app to external hardware 📡
🔹 **IR_Sensor** – Detects basketball shots via infrared technology (Connected to **port 2**) 📶
🔹 **RGB** – Changes colors based on shot detection (Connected to **port 1**) 🌈
🔹 **Notifier** – Displays connection status messages 📢

---

## 🏀 Logic and Functionality 🛠️

### **1️⃣ Bluetooth Connection Setup** 🔗
✅ When the user clicks **CONNECT**, the app retrieves the list of available Bluetooth devices.
✅ After selecting a device, the app attempts to connect using `BluetoothClient1.Connect`.
✅ If **successful**, a **Notifier** displays **"CONNECTED"**.
✅ If **unsuccessful**, a **Notifier** displays **"FAILED TO CONNECT"**.

---

### **2️⃣ IR Sensor Detection and Counter** 📟
📡 The **IR sensor** continuously monitors for basketball shots.

**✅ If a shot is detected (`IR_Sensor1.Get IR Value = true`):**
   - The **global count** increases by `1`. ➕
   - The **TotalCount** label updates to show the new count. 📈
   - The **RGB light turns GREEN** (`255` for Green, `0` for Red & Blue). ✅
   - A successful shot is registered!

**❌ If no shot is detected (`IR_Sensor1.Get IR Value = false`):**
   - The **RGB light remains OFF** (`0` for Red, Green, and Blue). ⚫
   - The **TotalCount** label remains unchanged. 🔄

🔹 This system ensures that every basket is accurately counted!

---

### **3️⃣ Reset Button** 🔄
🔘 Clicking the **RESET** button:
   - Sets **global count** back to `0`.
   - Updates the `TotalCount` label to display **`0`**.
   - Clears any previous count.

---

## 📊 Variables Used
📌 **global count** – Stores the total number of successful shots (initialized to `0`).
📌 **TOTALCOUNT.Text** – Displays the global count value on the UI.

---

## 🎯 Expected Behavior
1️⃣ The user selects a Bluetooth device and connects successfully. ✅
2️⃣ When a basketball shot is detected, the counter **increases**, and the RGB light **turns green**. 🟢
3️⃣ If no shot is detected, the **RGB light remains off**. ⚫
4️⃣ Clicking **RESET** resets the counter to **zero**. 🔄

---

## 📂 Provided Files
We have included the following files in the repository:
✅ **App.apk** – Installable Android application 📱
✅ **Counter.aia** – Source code file for Code2Play 🛠️

🚀 **Keep practicing, keep improving, and keep winning!** 🚀

