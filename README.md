# 🌌 Hand Gesture Controlled 3D Particle System....

<p align="center">
	<b>AI-powered interactive 3D visualization using hand gestures in real time</b><br><br>
	<img src="https://img.shields.io/badge/Three.js-3D%20Graphics-black?style=for-the-badge&logo=three.js" alt="Three.js badge">
	<img src="https://img.shields.io/badge/MediaPipe-Hand%20Tracking-blue?style=for-the-badge&logo=google" alt="MediaPipe badge">
	<img src="https://img.shields.io/badge/WebGL-High%20Performance-green?style=for-the-badge" alt="WebGL badge">
	<img src="https://img.shields.io/badge/Status-Active-success?style=for-the-badge" alt="Status badge">
</p>

-----

## ✨ Overview...

This project is an interactive 3D particle system that responds to hand gestures captured through your webcam.

It blends AI hand tracking with 3D rendering to create a futuristic, immersive, and highly responsive visual experience.

## 🎯 Features

| Feature | Description |
|---|---|
| 🎥 Real-time hand tracking | Detects hand movement live from your webcam |
| 🧠 Gesture recognition | Recognizes gestures and maps them to particle actions |
| 🌈 Dynamic colors | Uses smooth color transitions for a more vivid effect |
| 🔄 Particle morphing | Animates particles between different shapes |
| 🌌 Multiple 3D shapes | Switch between several generated particle forms |
| ⚡ Fast rendering | Powered by WebGL and Three.js for smooth performance |
| 🎮 Gesture controls | Simple gestures make the scene interactive |

## 🤏 Gesture Controls

| Gesture | Action |
|---|---|
| ✌️ Victory sign | Switch to the next shape |
| 👌 Pinch | Expand or contract particles |
| ✊ Fist | Collapse the particle core |

## 🌠 Available Shapes

- 🔵 Sphere
- ❤️ Heart
- 🪐 Saturn
- 🌸 Flower
- 🍩 Torus

## 🛠️ Tech Stack

| Technology | Purpose |
|---|---|
| Three.js | 3D rendering |
| MediaPipe Hands | Hand tracking AI |
| WebGL | Graphics performance |
| JavaScript (ES6+) | Application logic |
| HTML5 + CSS3 | User interface |

## 🚀 Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/Saurabh24500/Particles_Game.git
cd Particles_Game
```

### 2. Open the project

Open `Particles.html` in VS Code or your preferred editor.

### 3. Run locally

Use a local server because webcam access usually requires it.

```bash
# Example with VS Code Live Server
# Right-click Particles.html and choose Open with Live Server
```

## ⚙️ Requirements

- 🌐 A modern browser such as Chrome or Edge
- 🎥 Webcam permission enabled
- 📶 Internet connection for CDN-based libraries

## 🧠 How It Works....

1. MediaPipe detects 21 hand landmarks.
2. Gesture logic interprets landmark relationships.
3. Mathematical point generation creates the 3D shapes.
4. Particles move using smooth interpolation.
5. Three.js renders the final scene in real time.

## 📁 Project Structure

```text
Particles_Game/
├── Particles.html
└── README.md
```

## 🧾 Code Preview

This is a small excerpt from [Particles.html](Particles.html) that shows the main app structure and gesture-driven UI.

```html
<body>
	<div id="loading">Loading AI Models...</div>
	<div id="ui">
		<h2 id="shape-name">Shape: Sphere</h2>
		<div class="instruction">✌️ <b>Victory Sign</b>: Next Shape</div>
		<div class="instruction">👌 <b>Pinch</b>: Expand/Contract</div>
		<div class="instruction">✊ <b>Fist</b>: Collapse Core</div>
	</div>

	<video id="video-input"></video>
	<div id="canvas-container"></div>

	<script type="module">
		function onResults(results) {
			if (results.multiHandLandmarks && results.multiHandLandmarks.length > 0) {
				const landmarks = results.multiHandLandmarks[0];
				const thumbTip = landmarks[4];
				const indexTip = landmarks[8];
				const distance = Math.sqrt(
					Math.pow(thumbTip.x - indexTip.x, 2) +
					Math.pow(thumbTip.y - indexTip.y, 2)
				);
			}
		}
	</script>
</body>
```

## 📸 Visual Preview

<p align="center">
	<img src="https://placehold.co/1200x675/0f172a/f8fafc?text=Project+Screenshot+Here" alt="Project screenshot placeholder">
</p>

<p align="center">
	<img src="https://placehold.co/1200x675/111827/f59e0b?text=Add+an+animated+GIF+preview+here" alt="Animated GIF placeholder">
</p>

<p align="center"><i>Replace these placeholders with a real screenshot and GIF whenever you add them to the repository.</i></p>

## 🤖 Built With AI Assistance

This project was improved using:

- ChatGPT
- Google Gemini
- GitHub Copilot

AI tools helped speed up development, refine the logic, and improve the overall presentation.

## 🚧 Future Enhancements

- 🎵 Music-reactive particles
- 📱 Better mobile support
- 🥽 AR or VR integration
- 🎨 Custom shape generator
- 🧩 More gesture controls

## 🙌 Credits

- Three.js Community
- MediaPipe Team
- AI development tools

## 📜 License

This project is open source and free to use.

## ⭐ Show Your Support

If you like this project, consider:

- ⭐ Starring the repository
- 🍴 Forking it
- 🚀 Sharing it with others

## 👨‍💻 Author

Saurabh Patel

Computer Engineering Student

> 💡 Where AI meets creativity and real-time interaction.
