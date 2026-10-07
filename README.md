[README.md](https://github.com/user-attachments/files/33142741/README.md)
# Bird on a Wire: Tension vs Weight

An interactive physics simulation that shows why the tension in a nearly horizontal rope can be far larger than the weight hanging from it.

A bird of weight **W** sits at the midpoint of a light rope. Drag the angle **θ** (the angle each half of the rope makes with the horizontal) and watch the tension, its components, and Newton's second law update live.

This app accompanies a classic IB Physics multiple-choice question: *"A bird of weight W sits on a thin rope at its midpoint. The rope is almost horizontal. The tension in the rope is…"* The answer is **greater than W**, and the app shows why.

## The physics

The bird is in equilibrium, so the net force on the midpoint is zero. Taking up as positive, the vertical forces give:

```
ΣF_y = ma_y = 0
T sin θ + T sin θ + (−W) = 0
2T sin θ = W
T = W / (2 sin θ)
```

| Angle θ     | Tension           | Relation to W   |
|-------------|-------------------|-----------------|
| θ < 30°     | T > W             | Exceeds W       |
| θ = 30°     | T = W             | Equals W        |
| 30° < θ < 90° | W/2 < T < W     | Between W/2 and W |
| θ = 90°     | T = W/2           | Rope vertical   |

As the rope flattens, sin θ → 0, so T grows without limit. Each vertical component of tension is always exactly W/2. Only the horizontal components grow, and that is what drives T up.

## Features

- **θ slider (1° to 90°):** a coloured strip shows where T > W and where W/2 < T < W.
- **Weight input:** enter W in newtons to see numerical values throughout.
- **Snap buttons:** jump straight to T = 5W, 2W, W, W/√2 and W/2.
- **Setup diagram:** rope, posts, bird, both tensions with their x and y components, and the weight, all drawn to the same scale.
- **Tension vs weight box:** shows only the current relation (T > W, T = W, W/2 < T < W, or T = W/2).
- **Key thresholds:** each condition lights up when it is true.
- **Newton's second law panel:** a live force-component table with ΣF = 0, plus step-by-step working (equation, rearrangement, substitution, evaluation).
- **Vector triangle:** the closed tip-to-tail triangle of W and the two tensions, drawn to scale.
- **Graph:** T/W against θ with reference lines at W and W/2.
- **Light and dark mode:** follows your device setting.

**Sign convention:** right and up are positive; left and down are negative.

## Running it

The app is a single self-contained HTML file with no external libraries or dependencies.

- **Locally:** download `bird-on-a-wire.html` and open it in any modern browser. It works offline.
- **GitHub Pages:**
  1. Add the file to your repository. Rename it to `index.html` if you want it to load at the repository's root URL.
  2. Go to **Settings → Pages**.
  3. Under **Build and deployment**, choose **Deploy from a branch**, select your branch (e.g. `main`) and the `/ (root)` folder, then click **Save**.
  4. After a minute or two, the site will be live at `https://<your-username>.github.io/<repository-name>/`.

## Classroom ideas

- Ask students to predict the tension before revealing it, then use the slider to test their predictions.
- Use the snap buttons to show that T = W exactly at 30°, where the vector triangle becomes equilateral.
- Compare 30° and 60° to show that option C (between W/2 and W) only applies to a steeply sagging rope.
- Discuss why a perfectly horizontal rope (θ = 0) is impossible when it carries any weight.

## Author

Christopher B. Slough
