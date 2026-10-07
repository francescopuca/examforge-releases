# ExamForge Free Beta privacy

ExamForge has no ExamForge account, backend, analytics service, telemetry, or ExamForge server.

## Stored locally in Obsidian plugin data

- OpenAI and Gemini API keys and provider settings
- generated questions
- study and exam sessions
- answers from which statistics are calculated locally
- structured AI evaluations of open exam answers, including provider/model metadata and unavailable/disabled states
- JSON exports created explicitly by the user inside the vault

A clean Free Beta installation contains no API key, license key, user data, or preconfigured account. This release does not request, create, validate, or update an ExamForge license. If it replaces an earlier licensed test build, dormant legacy licensing fields may remain untouched in that local installation solely for storage compatibility; the Free Beta does not read them to grant access or send them to Lemon Squeezy.

## Sent to the selected AI provider

When you start generation, ExamForge sends directly to the provider selected in Settings (OpenAI or Google Gemini):

- the text of the selected Markdown note(s)
- their vault-relative paths
- generation parameters such as language, question type, count, and difficulty

After exam submission, when **AI evaluation for open questions** is enabled, ExamForge sends:

- the open question
- the user's answer
- the reference answer
- the saved source excerpt and source path
- a bounded relevant window of the source note, when that note is still available

Empty open answers are not sent. Evaluation requests run sequentially, consume the user's provider quota, and may incur charges under the user's provider plan. If the provider is unavailable, rate-limited, over quota, or returns malformed data, ExamForge saves an unavailable state while retaining the exam and answer locally. AI feedback is optional and advisory, not a definitive grade.

When you select **Test connection**, ExamForge sends the configured model name and a fixed minimal prompt asking the model to reply `OK`.

Only the active provider receives a request; switching providers does not send data to the inactive provider. API keys are used only to authenticate requests with their corresponding provider. Both OpenAI Responses requests and Gemini Interactions requests set `store: false`; Gemini authenticates with the key in the `x-goog-api-key` header. The direct data path is **ExamForge → selected AI provider**. ExamForge does not send unrelated notes, study history, statistics, or any data to an ExamForge proxy. Entire-vault generation is disabled by default.

Provider retention and training policies are outside ExamForge. In particular, Google's current [Gemini API pricing documentation](https://ai.google.dev/gemini-api/docs/pricing) states that Free-tier content may be used to improve Google products and Paid-tier content is not. Check the terms and plan attached to your Google project before sending sensitive notes. OpenAI processing remains governed by the terms and controls of the user's OpenAI API project.

## Lemon Squeezy and licensing

The Free Beta makes no activate, validate, or deactivate requests to Lemon Squeezy. It does not ask for or save a license key or purchase email. The dormant licensing implementation remains in the source architecture for a possible future paid release, but it is disabled by the centralized Free Beta release mode.

## Local secret storage

Obsidian does not expose a cross-platform secure secret store to community plugins. AI API keys are therefore stored in the plugin's local `data.json` and masked in the settings interface, but they are not encrypted by ExamForge. ExamForge JSON data exports exclude API keys, provider settings, and all licensing metadata. Protect access to your vault and device, use provider keys with appropriate project limits, and revoke an exposed key in the relevant OpenAI or Google account.
