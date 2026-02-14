# Open RPG Artel Studio

This workspace brings together two AgentArtel projects for review and integration:

- **[agent-artel-studio](./agent-artel-studio)** — Lovable-built app (Vite, TypeScript, React, shadcn-ui, Tailwind). [Agent-Artel-studio](https://github.com/AgentArtel/Agent-Artel-studio).
- **[Open-RPG](./Open-RPG)** — RPGJS v4 game with AI NPCs (Moonshot/Kimi). [Open-RPG](https://github.com/AgentArtel/Open-RPG).

## Setup

### Clone with submodules

```bash
git clone --recurse-submodules https://github.com/AgentArtel/open-rpg-artel-studio.git
cd open-rpg-artel-studio
```

If you already cloned without `--recurse-submodules`:

```bash
git submodule update --init --recursive
```

**If `Open-RPG` is missing** (e.g. it was added after your clone), run:

```bash
git submodule add https://github.com/AgentArtel/Open-RPG.git Open-RPG
```

### Agent Artel Studio (frontend / studio)

```bash
cd agent-artel-studio
npm i
npm run dev
```

### Open-RPG (game + AI agents)

```bash
cd Open-RPG
cp .env.example .env
# Edit .env and set MOONSHOT_API_KEY (see Open-RPG/readme.md)
npm install
npm run dev
```

Open the game at <http://localhost:3000>.

## Working together

- **agent-artel-studio**: UI/studio layer (Lovable, React).
- **Open-RPG**: RPGJS v4 game, AI agent system, Supabase.

Integration points (to be defined): shared auth, linking studio to game instances, or embedding the game in the studio.

## Repos

- [Agent-Artel-studio](https://github.com/AgentArtel/Agent-Artel-studio)
- [Open-RPG](https://github.com/AgentArtel/Open-RPG)
