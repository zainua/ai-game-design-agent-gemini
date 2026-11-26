# AI Game Design Agent Team (Gemini version)

A Streamlit app where a team of AI agents (story, gameplay, visuals, tech) collaborates to write a game design document from your inputs. It produces a **design document**, not a playable game.

Adapted from [`ai_game_design_agent_team`](https://github.com/Shubhamsaboo/awesome-llm-apps/tree/main/advanced_ai_agents/multi_agent_apps/agent_teams/ai_game_design_agent_team) in [awesome-llm-apps](https://github.com/Shubhamsaboo/awesome-llm-apps) by Shubham Saboo, licensed under Apache 2.0 (see `LICENSE`).

## Changes from the original

- Uses the **Gemini API** (via its OpenAI-compatible endpoint) instead of OpenAI.
- The sidebar asks for a Gemini API key and lists the models that key can use.
- Shows the provider's error message in the app if a request fails.
- `requirements.txt` pins `ag2[openai]==0.7.3`: the script uses `SwarmAgent` and the `register_hand_off` method, which newer AG2 releases removed or changed.

## Run locally

Requires Python 3.9+ and a Gemini API key (https://aistudio.google.com/apikey).

```powershell
python -m venv venv
.\venv\Scripts\python.exe -m pip install -r requirements.txt
.\venv\Scripts\python.exe -m streamlit run game_design_agent_team.py
```

Paste your Gemini API key in the sidebar (it is not stored anywhere), pick a model, fill in the game details and click **Generate Game Concept**. Check Google's pricing page to confirm the model you pick is on the free tier.
