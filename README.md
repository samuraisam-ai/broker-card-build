# Broker Card Build

A single-page tool for updating the **Broker** lesson cards on the Space Online Academy (LearnWorlds) site, without hand-editing code.

**Live:** deployed on Vercel from this repo. Every push to `main` redeploys.

## How it's used
1. Copy the current code from the Broker page's **Embeddable script** box in LearnWorlds.
2. Paste it into the builder and click **Load**.
3. Make changes in the **📝 Simple form** or the **👁 Visual editor**.
4. Click **Copy new code**, paste it back into LearnWorlds, then **Update → Save**.

There's also a **Check code** tab, which validates code from anywhere before it's pasted.

## How it stays safe
- Everything runs in the browser. Nothing is sent or stored anywhere.
- Pasted code is checked strictly against the card and section templates. Damaged or cut-off code is refused. The two fixed wrapper lines are repaired automatically.
- The output is rebuilt from the exact templates and read back, and **Copy** is only offered if nothing was lost.

## Editing
It's one self-contained file: `index.html`. The read/write logic lives between `/* CORE START */` and `/* CORE END */`. If the card or section markup ever changes, update the templates there.
