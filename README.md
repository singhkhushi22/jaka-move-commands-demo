# 🤖 JAKA Cobot Motion Commands – MoveJ vs MoveL vs MoveC

This repository demonstrates the **difference between JAKA cobot movement commands**:

* **`MoveJ`** – Joint movement
* **`MoveL`** – Linear movement
* **`MoveC`** – Circular movement

Each section explains the motion type, its advantages/disadvantages, and includes a **video demonstration** using a **JAKA collaborative robot**.

---

## 🔹 1. MoveJ – Joint Movement

**Definition:**
`MoveJ` moves each robot joint to the target position following the **shortest joint path**. The tool (TCP) path is **not guaranteed straight**, but the move is usually **faster**.

**Best used for:**

* Approaching/retracting
* Non-critical path moves
* Safe moves around workspace

**Video Demo:**  
👉 [![Watch MoveJ Demo](https://drive.google.com/file/d/1vsO3cmxGxyEdyfHisvhAHMG34MEnLgcH/view?usp=sharing)


## 🔹 2. MoveL – Linear Movement

**Definition:**
`MoveL` moves the TCP along a **straight line in Cartesian space**. This ensures precise linear paths but may be **slower** compared to `MoveJ`.

**Best used for:**

* Pick and place
* Assembly tasks
* Welding, gluing, or inspection along a straight path

**Video Demo:**
👉 [![Watch MoveL Demo](https://drive.google.com/file/d/1LKv0oqTbGd1cUirSIOzAP2ixPQIm_Wuy/view?usp=sharing)

---

## 🔹 3. MoveC – Circular Movement

**Definition:**
`MoveC` moves the TCP along a **circular arc** defined by two target points (intermediate + final).

**Best used for:**

* Machining tasks (arc welding, polishing)
* When a circular/arc path is required

**Video Demo:**
👉 [![Watch MoveC Demo](images/movec-thumb.png)](your_movec_video_link_here)

---

## 🔹 Comparison Table

| Command   | Path Type              | Speed   | Accuracy         | Use Cases                     |
| --------- | ---------------------- | ------- | ---------------- | ----------------------------- |
| **MoveJ** | Joint interpolation    | Fastest | Not linear       | Approach, retract, reposition |
| **MoveL** | Linear interpolation   | Medium  | Linear & precise | Pick & place, assembly        |
| **MoveC** | Circular interpolation | Medium  | Arc-precise      | Arc welding, polishing        |

---

## 🔹 Safety Notes

* Always test with reduced speed first.
* Define **pre-approach and retract waypoints**.
* Ensure safe zones are respected for each movement type.


