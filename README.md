# Road to 270

**Road to 270** is a single-player, browser-based **U.S. presidential campaign strategy game**. Create your candidate, define a policy platform, compete for your party's nomination, and campaign across the country to win the White House.

**Your objective:** win at least **270 of the 538 electoral votes** in the general election.

> **Note:** This is a fictional strategy game, not an election forecast. Candidates, rivals, polls, campaign events, delegate rules, and campaign effects are simulated.

## Play locally

There is no build step or package installation required.

1. Clone the repository:
   ```bash
   git clone https://github.com/iamshauryashah/Road-to-270.git
   cd Road-to-270
   ```
2. Open **`road-to-270/dist/index.html`** in a modern browser.

The current game is a static website with no server-side application or required API keys. For a local web server instead, run this from the repository root:

```bash
python3 -m http.server 8000
```

Then visit **http://localhost:8000/road-to-270/dist/**.

## Gameplay

### 1. Build your candidate

- Choose a candidate name, **Democratic or Republican** party, and home state.
- Select a political outlook, professional background, and personal backstory.
- Different backgrounds and stories affect starting campaign funds, trust, and organizing strength.

### 2. Shape your platform

Choose positions on six issues:

- Health care
- Taxes and the economy
- Climate and energy
- Immigration
- Guns
- Education

Your positions affect how well you connect with voters across different states. The game also considers how closely your platform matches your candidate's ideology.

### 3. Win the primaries

Compete against fictional rivals in a sequence of state primary contests. Manage your budget, organize locally, and collect delegates to pursue your party's nomination.

### 4. Fight the general election

Once nominated, compete against a fictional opposing-party candidate. Plan campaign actions, target states, and watch the electoral map shift as you pursue **270 electoral votes**.

### 5. Respond on the campaign trail

Campaign actions include interactive scenarios where you write responses to voters or interviewers. The current **practice judge is rule-based, not live AI**: it looks for wording and topic signals and returns feedback that can affect in-game support and credibility.

## Game systems

- **50 states and Washington, D.C.**, with 538 total electoral votes.
- State-by-state electoral map and campaign targeting.
- Campaign funding, organizing, credibility, and voter alignment.
- Simulated primary delegates and fictional opponents.
- Campaign choices and random variation that influence outcomes.
- Automatic game progress storage using your browser's **localStorage**.

**Important limitations:** Progress is saved in the current browser, not synced across devices. For gameplay simplicity, Maine and Nebraska use statewide winner-take-all electoral votes. The fictional election model should not be interpreted as live polling or a real election prediction.

## Project structure

```text
Road-to-270/
├── README.md
└── road-to-270/
    └── dist/
        ├── index.html   # Page markup, styling, and game entry point
        └── game.js      # Candidate setup, campaign rules, maps, and gameplay
```

## Deployment

Because this is a static HTML/JavaScript project, you can deploy the contents of **`road-to-270/dist/`** to any static web host.

- **Build command:** none
- **Publish directory:** `road-to-270/dist`
- **Entry point:** `index.html`
- **Environment variables:** none required

Keep `index.html` and `game.js` together so the browser can load the game script.

## Development

The game is implemented in plain HTML, CSS, and JavaScript. Edit `road-to-270/dist/index.html` for the page shell and styles, and `road-to-270/dist/game.js` for game data and mechanics. Reload the browser to see changes.

---

*Road to 270 — build a coalition, earn every vote.*
