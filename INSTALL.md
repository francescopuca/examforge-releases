# Install ExamForge Free Beta

ExamForge is installed inside your Obsidian vault. It is currently free during the Beta and requires no ExamForge license. AI features use your own Google Gemini or OpenAI API key; any provider cost is your responsibility.

## Step-by-step installation

1. Download `ExamForge-0.1.2-free-beta.zip`.
2. Extract the ZIP. You will see a folder named `examforge`.
3. Find your Obsidian vault folder. This is the folder that contains your notes.
4. Inside the vault, open the hidden folder `.obsidian`, then open `plugins`.
5. If the `plugins` folder does not exist, create it.
6. Copy the entire extracted `examforge` folder into `.obsidian/plugins/`.
7. Confirm that these files exist directly inside `.obsidian/plugins/examforge/`:
   - `main.js`
   - `manifest.json`
   - `styles.css`
8. Open or restart Obsidian.
9. Open **Settings → Community plugins**.
10. If necessary, enable community plugins, then enable **ExamForge Free Beta**.
11. Open ExamForge from the graduation-cap icon. It should open directly to the Dashboard; no license or activation screen is used.
12. Open **Settings → ExamForge Free Beta** and choose Google Gemini or OpenAI.
13. Create your own provider API key, enter it in the matching password field, and select a compatible model.
14. Select **Test connection**.
15. Open a study note and start using ExamForge from the graduation-cap icon.

Non-AI features work without an API key. Generation and optional open-answer evaluation require the user's selected provider and may consume that provider's paid quota.

## Free Beta and licensing

- No ExamForge account, payment, purchase email, or license key is required during the Free Beta.
- ExamForge makes no Lemon Squeezy activation, validation, or deactivation requests in this release.
- The Free Beta is not a promise that ExamForge will remain free permanently.

## API key safety

- ExamForge does not include or share an API key belonging to its author.
- Every user must provide their own key for AI features.
- Never send your API key to another person or include it in screenshots, shared vaults, backups, or support messages.
- Gemini and OpenAI availability, free-tier eligibility, usage limits, and pricing are controlled by the provider and can change.
- The key is stored locally by Obsidian in the plugin's `data.json`. Protect access to your device and vault, and revoke the key in the relevant provider account if it is exposed.

## If ExamForge does not appear

- Confirm the final path is `.obsidian/plugins/examforge/manifest.json`.
- Make sure there is not an extra nested folder such as `.obsidian/plugins/examforge/examforge/`.
- Restart Obsidian and check **Settings → Community plugins** again.
