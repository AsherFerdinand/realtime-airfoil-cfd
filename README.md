# ✈️ Realtime Airfoil CFD (Computational Fluid Dynamics)

Welcome back! Let's explore how air flows over airplane wings in real-time! 🚀

---

## 🏎️ ELI5: What is this? (Explain Like I'm 5)

Imagine you are in a moving car and stick your hand out the window 🚗💨:
- If you hold your hand **flat**, the air glides over it smoothly.
- If you **tilt** your hand up, the air pushes your hand upward! 🖐️⬆️
- If you tilt it **too much**, your hand gets slapped backward! 💥

This project uses a computer brain 🧠 (AI) to show you **how the air moves around a wing instantly**, without waiting hours for heavy science calculations! ⚡

---

## 🛠️ Project Repository & Quick Setup

### 📦 Key Components
- **Dataset / Mesh Generator:** 📐 Creates different wing shapes (airfoils) and wind angles.
- **Neural Network / ML Model:** 🤖 Learns how air flows so it can predict it in milliseconds.
- **Interactive UI (Streamlit / WebGL):** 🎮 Let's you slide controls and watch the air change color and speed in real-time!

---

## 💻 Get Started in 3 Steps

1. **Clone the Repo:**
   ```bash
   git clone https://github.com/your-username/realtime-airfoil-cfd.git
   cd realtime-airfoil-cfd
   ```

2. **Install Dependencies:**
   ```bash
   pip install -r requirements.txt
   ```

3. **Run the Interactive App:**
   ```bash
   streamlit run app.py
   ```

---

## 🎮 Interactive Experiments: Try It Yourself!

| 🎛️ Control | 🧪 What to Change | 📊 What Happens? |
| :--- | :--- | :--- |
| **Angle of Attack (Tilt)** | Increase to $15^\circ$ | Watch lift go UP 📈 until it suddenly stalls 📉! |
| **Wind Speed** | Boost velocity $v$ | Colors turn red 🔥 (high speed / low pressure)! |
| **Wing Shape** | Pick a curved airfoil | Notice how top air moves faster than bottom air 🌬️! |

---

## ❓ Mini Quick Quiz!

> **Why does an airplane lift up into the sky?**
>
> - **A)** The air under the wing pushes harder than the fast air on top! 🎈
> - **B)** Magic Invisible Strings ✨
> - **C)** The engines push directly down 🛞

*(Hint: It's **A**! Bernoulli's principle at work!  Bernoulli says: Fast air = lower pressure!)*
