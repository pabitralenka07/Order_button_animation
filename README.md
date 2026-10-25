# 🚚 Order Button Animation

An animated "Complete Order" button built with pure HTML, CSS and [GSAP](https://greensock.com/gsap/). When clicked, the button flips into 3D, a box is loaded onto a delivery truck, the truck drives along a progress road, and the button flips back with an "Order Placed" confirmation.

[![HTML5](https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=white)](#)
[![CSS3](https://img.shields.io/badge/CSS3-1572B6?logo=css3&logoColor=white)](#)
[![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?logo=javascript&logoColor=black)](#)
[![GSAP](https://img.shields.io/badge/GSAP-88CE02?logo=greensock&logoColor=white)](https://greensock.com/gsap/)

**[✨ Live Demo](https://pabitralenka07.github.io/Order_button_animation/)**

<!-- Tip: record a short GIF of the animation, save it as demo.gif in the repo, and uncomment the line below.
![Order button animation demo](demo.gif)
-->

---

## Features

- 🎬 Smooth multi-step animation sequence powered by GSAP
- 🧊 3D flip effect using CSS `transform-style: preserve-3d`
- 🎨 Fully themeable through CSS custom properties
- 🔁 Click again after completion to reset and replay
- 🪶 No build tools, frameworks or dependencies to install
- 🚚 Truck, wheels, box and road drawn entirely in CSS

## Demo

Click **Complete Order** to start the animation. Once the truck reaches the end of the road, the button shows **Order Placed ✓**. Click it again to reset.

## Tech Stack

| Technology | Purpose |
| --- | --- |
| HTML5 | Button markup and inline SVG checkmark |
| CSS3 | Truck artwork, 3D transforms, CSS variables |
| JavaScript (ES6) | Click handling and animation state |
| [GSAP 3.0.1](https://greensock.com/gsap/) | Animation timeline and CSS variable tweening |
| [Inter UI](https://rsms.me/inter/) | Typeface |

## Getting Started

### Prerequisites

Just a modern web browser. No Node.js or build step required.

### Run locally

```bash
# Clone the repository
git clone https://github.com/pabitralenka07/Order_button_animation.git

# Move into the project folder
cd Order_button_animation
```

Then open `index.html` in your browser. Or serve it with a local server:

```bash
# Python 3
python -m http.server 8000

# or Node.js
npx serve
```

Visit `http://localhost:8000`.

> **Note:** GSAP, the Inter font and the CSS reset load from a CDN, so an internet connection is needed the first time you open the page.

## Project Structure

```
Order_button_animation/
├── index.html   # Button markup and CDN links
├── style.css    # Layout, truck artwork and 3D transforms
├── script.js    # GSAP animation logic
└── README.md
```

## How It Works

1. **Click:** the `animation` class is added to the button, which rotates it `-90deg` on the X axis to reveal the "road".
2. **Loading:** GSAP tweens the CSS variables `--box-s`, `--box-o`, `--hx` and `--bx` so the box appears, slides in and gets packed.
3. **Driving:** a GSAP timeline moves the truck along the road while `--progress` fills the route.
4. **Done:** the `done` class flips the button back to flat and fades in the "Order Placed" message with an animated checkmark.
5. **Reset:** clicking again removes both classes and resets every variable to its starting value.

## Customization

The colors are CSS variables defined on `.truck-button` in `style.css`. Change them to match your brand:

```css
.truck-button {
  --background: #2B3044;  /* button color */
  --tick: #16BF78;        /* checkmark color */
  --back: #6D58FF;        /* truck cargo area */
  --box: #DCB97A;         /* delivery box */
}
```

To change the text, edit the labels in `index.html`:

```html
<span class="default">Complete Order</span>
<span class="success">Order Placed ...</span>
```

To adjust timing, edit the `duration` and `delay` values in `script.js`.

## Browser Support

Works in current versions of Chrome, Edge, Firefox and Safari. It relies on CSS custom properties, `clip-path` and 3D transforms.

## Contributing

Contributions, issues and feature requests are welcome.

1. Fork the project
2. Create your branch (`git checkout -b feature/my-feature`)
3. Commit your changes (`git commit -m "Add my feature"`)
4. Push to the branch (`git push origin feature/my-feature`)
5. Open a Pull Request

## License

This project is licensed under the [MIT License](LICENSE).

## Author

**Pabitra Lenka**
GitHub: [@pabitralenka07](https://github.com/pabitralenka07)

## Acknowledgements

- [GSAP](https://greensock.com/gsap/) by GreenSock
- [Inter](https://rsms.me/inter/) typeface by Rasmus Andersson
- Based on the "Order button animation" design from CodePen. Credit the original creator here if you are building on their work.

---

⭐ If you like this project, give it a star!
