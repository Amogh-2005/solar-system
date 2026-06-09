# 🌌 Solar System Exploration

An interactive, 3D WebGL orrery and astronomical game hub built for **NASA Space Apps Challenge 2024** by team **JAAS'zzz code**.

Explore the wonders of our solar system, learn about the planetary bodies using real NASA resource links, and challenge yourself with space-themed games!

---

## 🚀 Key Features

### 1. Interactive 3D Orrery (`star.html` & `app.js`)
* **Realistic Physics & Motion:** Planets orbit the Sun using custom Keplerian orbital calculation algorithms (`calculate_position`), accounting for semi-major axes, orbital eccentricity, inclination, orbital period, and axial rotation speed.
* **Stunning Visuals:** Built with **Three.js**, featuring high-resolution planetary textures, custom shader-based solar glow, dynamic lighting intensity that scales with distance from the Sun, Saturn's rings, and simulated solar flare particles.
* **Smooth Navigation:** Utilizes **OrbitControls** for panning, rotating, and zooming.
* **Tweened Focus:** Interactive raycasting lets you click any planet to smoothly zoom in on it via **Tween.js** and open an information card with key facts and direct NASA science resource links.

### 2. Space Games
* **Space Shooter (`game1.html` & `game1.js`):** A fast-paced retro arcade shooter. Control your spaceship with your mouse, shoot dual lasers (equipped with rate-limiting cooldowns), avoid alien ships, and beat your high score within a 60-second timer. High scores are saved persistently in `localStorage`.
* **Space Shuffler / Starry Night Puzzle (`game2.html` & `game2.js`):** A classic 15-sliding tile puzzle. Rearrange the scrambled slices of a starry space nebula image back to its original order.

### 3. Resource Center (`resource.html`)
* Links to the core documentation, 3D rendering engines, and astronomical databases utilized to build this project (NASA APIs, NASA Space Science Data Coordinated Archive, Blender, Three.js, etc.).

---

## 🛠️ Tech Stack

* **Structure:** HTML5 (Semantic elements)
* **Styling:** CSS3 (Custom animations for starfields and twinkling backdrops)
* **3D Graphics & Math Engine:** [Three.js](https://threejs.org/) (WebGL)
* **Orbit Manipulation:** [OrbitControls](https://threejs.org/docs/#examples/en/controls/OrbitControls)
* **Animation Tweening:** [Tween.js](https://github.com/tweenjs/tween.js)
* **Icons:** [Font Awesome 6](https://fontawesome.com/)

---

## 💻 How to Run Locally

> [!IMPORTANT]
> Because the application loads high-resolution planetary textures and images dynamically, opening the `.html` files directly via the browser (`file://` protocol) will trigger **CORS (Cross-Origin Resource Sharing) security blockages**. You **must** serve the project directory through a local web server.

Choose one of the quick methods below to run the project locally:

### Option A: Using Node.js (Recommended)
If you have Node.js installed, open your terminal in the `solar-system` directory and run:
```bash
# Install dependencies (Three.js and Tween.js)
npm install

# Run a lightweight local server instantly
npx http-server
```
Then open `http://localhost:8080` in your web browser.

### Option B: Using Python
If you have Python installed, open your terminal in the `solar-system` directory and run:
```bash
# Python 3
python -m http.server 8000
```
Then open `http://localhost:8000` in your web browser.

### Option C: VS Code Live Server Extension
1. Open the project folder in VS Code.
2. Click **Go Live** on the bottom status bar, or right-click `index.html` and choose **Open with Live Server**.

---

## 📂 Project Structure

```text
solar-system/
├── images/               # Image assets for games and icons
│   └── images_g2_1/      # Sliced tile pieces for the sliding puzzle
├── textures/             # High-res planetary & starfield textures (Earth, Moon, Sun, etc.)
├── index.html            # Main home portal / landing page
├── style2.css            # Stylesheet for home, resources, and starfields
├── star.html             # The 3D Orrery page
├── app.js                # Core WebGL rendering, orbital physics, and interaction logic
├── game1.html            # Space Shooter game layout
├── game1.js              # Space Shooter logic (collisions, score, spaceship)
├── game1.css             # Space Shooter styles
├── game2.html            # Starry Night Puzzle layout
├── game2.js              # Space Shuffler puzzle logic (shuffling, slide checks)
├── game2.css             # Space Shuffler puzzle styles
├── resource.html         # Project credits & learning resources
├── package.json          # Node package definition
└── README.md             # This documentation file
```

---

## 👥 The Team: JAAS'zzz code

* **R L Jayesh** — 3D Animator (designed and modeled solar system entities)
* **Ayesha** — Web page maintenance & interactive model features
* **Sanjana B Kulkarni** — Integration Developer (stitched animations and interactive modules together)
* **Amogh A Kashyap** — Orbit & Scale Engineer (implemented spatial calculations and orbital motions)
* **Shravya** — Lead Researcher & Scientific Content Writer
