# 🌟 Interactive Solar System Simulator

An engaging, purely front-end visualization project built with HTML, CSS, and vanilla JavaScript that simulates the orbits of the eight major planets around the Sun. This project is a great demonstration of complex CSS animations and simple JavaScript DOM manipulation.



### ✨ Features

* **Heliocentric Model:** Accurate (stylized) representation of the eight major planets (Mercury through Neptune) orbiting the Sun.
* **Physics-Inspired Animations:** Orbital speeds (`--speed` CSS variable) are set relative to their actual positions, creating a continuous, fast-forwarded orbital effect.
* **Interactive Info Cards:** Click any celestial body (the Sun or a planet) to display a dedicated information card detailing its basic characteristics.
* **Dynamic Visual Effects:**
    * **Twinkling Stars:** A randomly generated, animated background of stars is created using JavaScript for a dynamic space atmosphere.
    * **Comet Streak:** A periodically animated CSS-based comet streaks across the screen.
    * **Saturn's Rings:** A distinct visual ring structure is included for Saturn.
* **User Controls:** A **Pause/Resume Orbits** button to instantly halt and restart the entire system's animation state.

### 🛠️ Technologies Used

| Technology | Purpose |
| :--- | :--- |
| **HTML5** | Structure for the solar system elements and information cards. |
| **CSS3** | Layout, styling, and all primary orbital and background animations (`@keyframes`). |
| **Vanilla JavaScript** | Logic for star generation, comet animation control, interactive info cards (`showInfo`, `closeInfo`), and the pause/play functionality (`togglePause`). |

### ⚙️ Installation and Usage

This project is a single-file application (`index.html`). No complex dependencies or build steps are required.

1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/YOUR_USERNAME/interactive-solar-system-css-js.git](https://github.com/YOUR_USERNAME/interactive-solar-system-css-js.git)
    ```
2.  **Open the file:**
    Navigate to the project directory and double-click the `index.html` file. It will open directly in your web browser.
3.  **Deployment:** This project is ideal for hosting on **GitHub Pages** due to its pure front-end nature.

### 💡 Core Implementation Details

The smooth, continuous animation is achieved entirely through CSS using the `animation` property and the `rotate` keyframe.

```css
/* Core orbital animation */
@keyframes rotate { 
    from { transform: rotate(0deg); } 
    to { transform: rotate(360deg); } 
}

.orbit {
    /* Uses a custom property defined per planet (e.g., 5s for Mercury, 80s for Neptune) */
    animation: rotate var(--speed) linear infinite;
}
.paused { 
    /* The key to pausing */
    animation-play-state: paused !important; 
}
```



**📄 License** 
```txt
This project is licensed under the MIT License - see the LICENSE file for details.
```
