
# ExamForge Free Beta

ExamForge turns your Obsidian notes into source-linked study material and exam practice. Questions, answers, sessions, history, and statistics remain in your local Obsidian vault.

## Proprietary license and private source

© 2026 Francesco Puca. All rights reserved.

ExamForge is a proprietary, closed-source plugin. The public distribution
repository contains release metadata and documentation. The TypeScript source,
tests, and build configuration are maintained in a separate private repository.
The compiled JavaScript needed to run the plugin is distributed publicly as
the `main.js` release asset and can be read; source maps are not supplied.

The [ExamForge Proprietary Free Beta License](LICENSE) permits end users to
download, install, and use official copies free of charge during the Beta.
It does not grant an open-source license or a general permission to redistribute,
resell, publish forks, reuse code in other products, or remove notices.
Independent rights required by law or arising under applicable GitHub Terms
for public content remain unaffected. The Beta can end prospectively with
reasonable prior notice; no automatic charge or subscription is created.

The planned Obsidian Community submission uses the official
[Obsidian Community Directory GitHub App](https://github.com/apps/obsidian-community-directory)
for read-only access to the private source repository, source review, and build
verification. No directory acceptance or installation availability is claimed
until review is complete. Private source access is not granted to end users.

## Free during the Beta

ExamForge is currently available as a free Beta. This release:

- requires no ExamForge account, purchase, license key, or activation;
- opens directly to the Dashboard with every current feature available;
- does not contact Lemon Squeezy;
- includes no ExamForge credits, subscription, payment flow, telemetry, analytics, or artificial usage limits.

The Free Beta is not a promise that ExamForge will remain free permanently.

## Main features

- Generate flashcards from selected Markdown notes.
- Create multiple-choice and true/false quizzes.
- Generate open-ended questions with optional AI evaluation of answers.
- Run focused study sessions with immediate feedback.
- Use Smart Review to prioritize mistakes, weak topics, and unseen questions.
- Review Weak and Strong Topics and start targeted practice.
- Run timed exam simulations with objective scoring kept separate from advisory AI review.
- View a local dashboard, statistics, history, and completed exam results.
- Keep every generated question linked to its source note and excerpt.

## Your AI provider and API key

ExamForge is BYOK: “bring your own key.” No API key or AI credits are included with the plugin.

- Google Gemini and OpenAI are supported.
- You choose the provider, enter your own API key, and select the model in **Settings → ExamForge Free Beta**.
- Only the selected provider is contacted.
- Any provider charges, quotas, rate limits, model availability, and account terms belong to the user and the selected provider.

Non-AI features and existing local study data remain available without an API key. An API key is required only when you request AI generation, connection testing, or optional AI evaluation of an open answer.

Never share your API key. ExamForge stores it locally using Obsidian's plugin storage so it can make requests directly from your device.

## Install

Follow the step-by-step instructions in [INSTALL.md](INSTALL.md).

## First use

1. Open ExamForge from the graduation-cap icon. The Dashboard opens immediately; there is no activation screen.
2. Open **Settings → ExamForge Free Beta**.
3. Choose Google Gemini or OpenAI.
4. Enter your own API key and a compatible model.
5. Select **Test connection**.
6. Open a Markdown note containing your study material.
7. Generate questions, begin a study session, or create an exam simulation.

AI evaluation for open exam answers is enabled by default. You can disable it in ExamForge settings; open answers will then remain ungraded. AI feedback is advisory and is not a definitive grade.

## Privacy

- Study data, questions, answers, statistics, and history are stored locally in Obsidian plugin data.
- Selected note content is sent directly to the AI provider you choose only when you request an AI operation.
- Open-answer evaluation sends the question, your answer, the reference answer, and relevant source context directly to that provider.
- ExamForge has no ExamForge account, backend, analytics service, telemetry, or ExamForge server.
- API keys and provider settings are excluded from ExamForge data exports.
- This Free Beta neither requests a license key nor makes license API calls.

Read [PRIVACY.md](PRIVACY.md) for the complete data boundary.

## Known limitations

- AI-generated questions and open-answer evaluations should be reviewed. AI grading is optional, advisory, and may not match an instructor's grading.
- Provider rate limits, quota, model availability, network errors, and pricing are controlled by Google or OpenAI.
- If open-answer evaluation fails, the exam and answer remain saved and the open question stays ungraded.
- API keys are stored locally in Obsidian plugin storage. Obsidian does not provide community plugins with a cross-platform encrypted secret vault.
- ExamForge does not include an account, custom backend, cloud sync, OCR, speech, advanced spaced repetition, local models, telemetry, or analytics.

## Release

Version: **0.1.3 Free Beta**

Minimum Obsidian version: **1.7.2**
