# 🎉 An Interactive Birthday Surprise Web Experience

A **multi-page, animation-rich digital birthday card** built entirely with **HTML, CSS, and JavaScript**.  
This project is designed as a unique, personal, and unforgettable birthday gift — taking the user on a journey from a spectacular countdown to a nostalgic photo gallery, heartfelt messages, and an interactive finale.

https://01-akm.github.io/birthday-page/

---

## 🚀 How the System Works

The experience flows linearly, with each page leading to the next:

1. **The Grand Reveal (`index.html`)**
   * Starts with a **"Click to Begin!"** screen (to enable audio).
   * A **10-second countdown** launches, with sparkles, ribbons, and animations.
   * All animations are powered by **`setInterval`** and **`setTimeout`** in JavaScript.

2. **Continuous Music**
   * Background music **plays seamlessly across all pages**.
   * Achieved with `localStorage`:
     - On exit: current time + mute state is saved.
     - On load: playback resumes from the exact same spot.

3. **The Memory Lane (`phase2.html`)**
   * A **slideshow of personal photos** with captions.
   * Runs automatically via a **JavaScript array** + timed CSS transitions.

4. **The Heartfelt Message (`phase3.html`)**
   * A long message revealed with a **typing animation effect**.
   * Built using a custom JavaScript function iterating through the text.

5. **The Interactive Finale (`phase4.html`)**
   * Visitors can **add personal messages**, stored persistently with `localStorage`.
   * A **Share Feature**:
     - Uses the **Web Share API** (on mobile HTTPS).
     - Falls back to the **Clipboard API** (desktop/local).

---

## 🛠️ Tech Stack

* **HTML5** → Page structure & semantic content.  
* **CSS3** → Styling + particle effects + keyframe animations.  
* **JavaScript (ES6)** → Interactivity, logic, and data persistence.  
* **Tailwind CSS** → Rapid, responsive UI styling.  
* **Google Fonts** → Typography with *Lobster* & *Poppins*.  

---

## ✨ Key Features

* 🎶 **Persistent background music** across all pages.  
* 🖼️ **Photo slideshow** with captions & animations.  
* ⌨️ **Typing effect** for heartfelt text.  
* 💌 **Message board** where users can leave notes.  
* 📤 **Sharing system** (Web Share API + Clipboard fallback).  
* 🎨 Fully customizable: text, images, music, and animations.  

---

## 📝 How to Use & Edit

1. **Change Text Content**
   - `index.html` → Main "Happy Birthday" title.
   - `phase2.html` → Title, subtitle, and **memories array** (captions).
   - `phase3.html` → Long text (`fullMessage` variable).
   - `phase4.html` → Header text and instructions.

2. **Update Images**
   Edit the `memories` array in `phase2.html`:
   ```js
   const memories = [
       { image: 'your_image_url_1.jpg', caption: 'Your first caption here!' },
       { image: 'your_image_url_2.jpg', caption: 'Your second caption here!' }
   ];

### 🎵 Change Music

1. Add your **`.mp3`** file.  
2. Rename it to **`background-music.mp3`**.  
3. Place it in the **project root folder**.  

---

## ⚡ Challenges We Faced

### 🔇 Browser Auto-Play Restrictions
* **Problem**: Browsers block audio from auto-playing.  
* **Solution**: Added a **Start Screen** that requires user interaction before playback.  

### 🎶 Continuous Music Across Pages
* **Problem**: Music restarted every time a new page loaded.  
* **Solution**: Used **localStorage** to save and resume playback state seamlessly.  

### 📤 Sharing Across Devices
* **Problem**: `navigator.share` only works on **HTTPS + mobile browsers**.  
* **Solution**: Built a **Clipboard fallback** + a visual preview card.  

---

## 🤝 Contributing

Want to make this birthday card even better?  

1. **Fork** this repo  
2. **Make your changes** (add animations, improve design, fix bugs, etc.)  
3. **Submit a pull request** 🎉  

---

## 📜 License

This project is open-source under the **MIT License**.  
✅ You’re free to **use, modify, and share** it.  
💖 Just spread the love and give credit where due!  
---




![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)  

