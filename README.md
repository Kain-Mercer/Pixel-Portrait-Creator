# Pixel Portrait Creator

Make 64×64 pixel-art character portraits in your browser.

**Open it: https://kain-mercer.github.io/Pixel-Portrait-Creator/**

Every part (face shape, eyes, brows, nose, mouth, hair, facial hair, outfit, eyewear and extras) sits on a fixed layout, so any combination fits together cleanly. Build a character part by part, or roll a whole crew at random.

## Features

- **Three worlds**
  - **Across Country**: early 2000s, natural looks only
  - **Underpass**: still human, but cyberpunk: neon hair, visors, implants
  - **Across Cosmos**: everything, including alien skin tones, pointed ears and antennae
- **Gender: male, female or either**: randomizing only uses parts that match the chosen gender.
- **Randomize with locks**: keep the parts you like and re-roll the rest.
- **Crew roster**: twelve random characters at a time; click one to edit it.
- **Save PNG**: 64×64 for use as a game sprite, or 512×512 for previews.
- **Copy recipe**: a short JSON description that rebuilds the exact same character.
- **Templates**: import recipes, lists or whole crew packs from JSON, and save the current character or crew as a file.
- **Works on phones**: the portrait stays pinned at the top while you pick parts.
- **Anchor guides** and a **reference overlay** for checking proportions. Overlay images stay in your browser and are never uploaded.

## Templates

You can import characters as JSON with **Import file** or **Paste JSON**:

- **One recipe**, as produced by **Copy recipe** or **Save recipe file**
- **A list** of recipes: `[ {...}, {...} ]`
- **A pack**: `{ "name": "My crew", "characters": [ {...}, {...} ] }`. **Save crew file** writes this format.

A list or pack fills the crew roster (up to 48 characters), and the first character opens in the editor.

**Partial recipes work as templates.** Set only the parts you care about and the rest is filled in from the seed (a random one if you leave `seed` out):

```json
{ "world": "underpass", "sex": "fem", "hairStyle": "undercut", "hairColor": 7 }
```

Values a world or gender doesn't allow are swapped for an allowed one. For example, alien skin in Across Country becomes a human tone, and a beard on a female character is removed. In recipes, gender is written `"sex": "masc"` or `"sex": "fem"`.

## Use it offline

Download `index.html` and open it in any modern browser. It's a single self-contained file with nothing to install.
