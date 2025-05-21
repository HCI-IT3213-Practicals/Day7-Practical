# Day 07 (20_05_2025) Practical Sessions – Quick Action Buttons 🎯

Welcome to Day 07 of the IT3213 Human-Computer Interaction (HCI) practical sessions!  
In today’s hands-on Axure RP 9 session, we focused on designing interactive **Quick Action Buttons** integrated with **Dynamic Panels**, gesture-based interactions, and advanced conditional logic. This exercise enhances UX by simulating real app-like behavior such as **like**, **share**, **info**, and **delete** actions.

---

## 🚀 Practical Overview

In this session, we:

- Designed a **top bar with dynamic content areas**.
- Added **Quick Action Buttons** (Share, Heart, Info, Delete).
- Created separate **panels** for each action with animations and interactions.
- Implemented **toggle states**, **slide animations**, and **gesture-based events** like swipe.
- Enhanced realism using **lightbox effects** and **responsive pinning**.

---

### 📦 01: UI Setup

**Steps:**

1. Create the **top bar**.
2. Add a **Dynamic Panel** to contain the image.
3. Inside the panel, add an **image container** and insert an image.
4. At the bottom, add a **rectangle** for the quick action buttons.
5. Place icons: **Share**, **Heart**, **Info**, and **Delete** inside the rectangle.

---

### 🎨 02: Panels and Layout

**Share Panel:**
- Create using a **rectangle**.
- Add **ellipses** as share menu icons.
- Select all elements and convert to a **Dynamic Panel (name: share)**.
- Add **title: Share** as Heading 3.
- Pin it: Horizontal center, Vertical bottom.
- Set **Hidden** by default.

**Info Panel:**
- Add a rectangle with **Info Heading** and border styles.
- Add **text content** as inner rectangle.
- Convert to a **Dynamic Panel (name: info)**.
- Pin it: Horizontal center, Vertical bottom.
- Set **Hidden**.

**Delete Panel:**
- Create rectangle with **two buttons**: `Delete (Red)` and `Cancel`.
- Set background to **transparent black**.
- Convert to **Dynamic Panel (name: delete)**.
- Pin it: Horizontal center, Vertical bottom.
- Set **Hidden**.
- Position it horizontally off-screen to prepare for animation.

---

### 🧠 03: Interaction Logic

**Heart Icon:**
- Interaction: **On Click**
- Action: Set **Selected/Checked**
- Effect: **Change fill color to Red**
- Toggle selected state.

**Share Icon:**
- Interaction: **On Click**
- Action: **Show/Hide** `share` panel
- Animation: **Slide Up (200ms)**
- Treat as **Lightbox**, set semi-transparent black background.

**Info Icon:**
- Interaction: **On Click**
    - **Show/Hide** `info` panel – Slide Up (200ms)
    - **Move** image dynamic panel Y-axis **−100px** (Linear, 200ms)
    - Set image panel’s **selected state = true**
- Add conditional logic:
    - If **selected = false** → Determine Y position.
- Add gesture:
    - **Swipe Down** on image panel:
        - If **selected = true**:
            - Move image panel Y-axis **+100px** (Linear, 200ms)
            - **Hide** info panel (Slide Down, 200ms)
            - Set selected state to **false**
- Add **Swipe Down** on `info` panel to **trigger** image panel swipe down.

**Delete Icon:**
- Interaction: **On Click**
    - Show `delete` panel
    - Animation: **Slide Up (200ms)**
    - Treat as **Lightbox**

- Inside delete panel:
    - On `Delete Photo` button click: **Hide** delete panel.

**Share Panel Buttons:**
- On Click: **Hide** the share panel.

---

### 📸 Output Snapshots (Expected)

1. **Default View** – Top bar, image, and quick actions visible.

![Screenshot 1](https://github.com/user-attachments/assets/89ce4ca7-669b-4537-ae43-c4349045258e)

2. **Heart Clicked** – Icon changes to red.

![Screenshot 3 Heart](https://github.com/user-attachments/assets/38663a61-7ec9-4d82-9dc6-373c97424f74)

3. **Share Clicked** – Share menu slides up with ellipses.

![Screenshot 2 Share](https://github.com/user-attachments/assets/f60927ce-f9d1-4f68-b852-3dd9d8f0bb36)

4. **Info Clicked** – Info panel slides in, image moves up.

![Screenshot 4 Info](https://github.com/user-attachments/assets/e4ea0cde-6fb4-4307-9b52-1fed60fd1693)

5. **Delete Clicked** – Delete confirmation panel appears.

![Screenshot 5 Delete](https://github.com/user-attachments/assets/2ead1f62-f8b2-4b20-93ad-928f6876036e)


---

### 🛠️ How to Use the Axure RP 9 File

1. **Install Axure RP 9** (if not installed).
2. Download the `.rp` file provided by the instructor.
3. Open the file and go to preview mode.
4. Try clicking icons and swiping panels as described above.

---

## 📜 License

This project is licensed under the **MIT License**. Please refer to the LICENSE file for more information.
