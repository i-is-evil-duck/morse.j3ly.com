# Morse Trainer  <br />  <img alt="Stargazers" src="https://img.shields.io/github/stars/i-is-evil-duck/morse.j3ly.com?style=for-the-badge&logo=starship&color=C9CBFF&logoColor=D9E0EE&labelColor=302D41">


## Morse Trainer
Google Gboard-style Morse code trainer. Type words letter-by-letter with mnemonic hints, weighted rare-letter practice (Q, X, Z, J, V), and a persistent solved counter.

Live at [morse.j3ly.com](https://morse.j3ly.com).

## Downloads

Single static file — no build step. Download from the [releases](https://github.com/i-is-evil-duck/morse.j3ly.com/releases) page.

| Platform | File |
|----------|------|
| Static | `index.html` |
| Docker | serve with any static server |

## Build from Source

```bash
# Clone the repo
git clone https://github.com/i-is-evil-duck/morse.j3ly.com.git
cd morse.j3ly.com

# Serve statically (no dependencies)
python -m http.server 8080
# or
npx serve .
```

Then open http://localhost:8080 in your browser.

## Setup

No config files. Tweak in `index.html`:

- `MORSE_MAP`: letter → morse + mnemonic + rarity weight
- `WORD_LIST`: practice vocabulary (rare-letter, complex, standard sets)
- `HINT_DELAY_MS` (default 2500): delay before showing the mnemonic hint

Progress persists in `localStorage` key `morse_words_solved`.

## Usage

Click the card to focus the keyboard, then type the shown word:

- Correct letters turn green and advance; wrong keys flash red
- Stuck for 2.5s? A hint box shows the morse pattern + mnemonic (e.g. `Q = Quarter`)
- Solved count increments per completed word

## Views

<img src="https://count.getloli.com/get/@MorseTrainer?theme=rule34" />
