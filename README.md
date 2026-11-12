# 📝 KEYLOOM

### Weaving better typing habits, one keystroke at a time.

Keyloom is a local-first, intelligent touch-typing learning platform designed to help users transition from hunt-and-peck typing to proper touch typing.

Combining structured guided lessons with adaptive practice, Keyloom analyzes typing patterns, identifies weaknesses, generates personalized exercises, and helps users develop accuracy, consistency, and muscle memory.

**Learn deliberately. Practise intelligently. Type effortlessly.**

# 🪜 Architecture Structure

```
KEYLOOM/
│
├── .github/
│   ├── workflows/
│   │   ├── ci.yml
│   │   └── release.yml
│   │
│   ├── ISSUE_TEMPLATE/
│   │   ├── bug_report.md
│   │   └── feature_request.md
│   │
│   └── PULL_REQUEST_TEMPLATE.md
│
├── docs/
│   ├── PROJECT_VISION.md
│   ├── SYSTEM_ARCHITECTURE.md
│   ├── CURRICULUM_DESIGN.md
│   ├── LEARNING_ENGINE.md
│   ├── ADAPTIVE_ENGINE.md
│   ├── TYPING_METRICS.md
│   ├── DATABASE_SCHEMA.md
│   ├── PRIVACY_POLICY.md
│   │
│   └── decisions/
│       ├── ADR-001-local-first-architecture.md
│       ├── ADR-002-indexeddb-storage.md
│       └── ADR-003-modular-learning-engine.md
│
├── public/
│   ├── favicon.svg
│   ├── logo.svg
│   └── images/
│
├── src/
│   │
│   ├── app/
│   │   ├── App.tsx
│   │   ├── main.tsx
│   │   ├── routes.tsx
│   │   └── providers/
│   │
│   │
│   ├── features/
│   │   │
│   │   ├── onboarding/
│   │   │   ├── components/
│   │   │   ├── hooks/
│   │   │   └── pages/
│   │   │
│   │   ├── dashboard/
│   │   │   ├── components/
│   │   │   ├── hooks/
│   │   │   └── pages/
│   │   │
│   │   ├── guided-learning/
│   │   │   ├── components/
│   │   │   ├── lessons/
│   │   │   ├── hooks/
│   │   │   └── pages/
│   │   │
│   │   ├── typing-practice/
│   │   │   ├── components/
│   │   │   ├── virtual-keyboard/
│   │   │   ├── finger-guide/
│   │   │   ├── hooks/
│   │   │   └── pages/
│   │   │
│   │   ├── session-results/
│   │   │   ├── components/
│   │   │   └── pages/
│   │   │
│   │   ├── analytics/
│   │   │   ├── components/
│   │   │   ├── charts/
│   │   │   └── pages/
│   │   │
│   │   ├── coding-lab/
│   │   │   ├── components/
│   │   │   └── pages/
│   │   │
│   │   ├── revision/
│   │   │   ├── components/
│   │   │   └── pages/
│   │   │
│   │   └── settings/
│   │       ├── components/
│   │       └── pages/
│   │
│   │
│   ├── core/
│   │   │
│   │   ├── domain/
│   │   │   │
│   │   │   ├── typing-engine/
│   │   │   │   ├── keystroke-tracker.ts
│   │   │   │   ├── typing-timer.ts
│   │   │   │   ├── wpm-calculator.ts
│   │   │   │   ├── accuracy-calculator.ts
│   │   │   │   ├── transition-analyzer.ts
│   │   │   │   └── typing-session.ts
│   │   │   │
│   │   │   ├── learning-engine/
│   │   │   │   ├── lesson-manager.ts
│   │   │   │   ├── progression-manager.ts
│   │   │   │   ├── mastery-evaluator.ts
│   │   │   │   └── prerequisites.ts
│   │   │   │
│   │   │   ├── exercise-engine/
│   │   │   │   ├── generators/
│   │   │   │   │   ├── movement-generator.ts
│   │   │   │   │   ├── combination-generator.ts
│   │   │   │   │   ├── vocabulary-generator.ts
│   │   │   │   │   ├── sentence-generator.ts
│   │   │   │   │   └── paragraph-generator.ts
│   │   │   │   │
│   │   │   │   ├── difficulty-controller.ts
│   │   │   │   ├── exercise-validator.ts
│   │   │   │   └── exercise-selector.ts
│   │   │   │
│   │   │   ├── adaptive-engine/
│   │   │   │   ├── weakness-detector.ts
│   │   │   │   ├── key-analyzer.ts
│   │   │   │   ├── transition-analyzer.ts
│   │   │   │   ├── recommendation-engine.ts
│   │   │   │   ├── difficulty-adapter.ts
│   │   │   │   └── spaced-repetition.ts
│   │   │   │
│   │   │   ├── analytics-engine/
│   │   │   │   ├── performance-analyzer.ts
│   │   │   │   ├── consistency-analyzer.ts
│   │   │   │   ├── session-analyzer.ts
│   │   │   │   ├── trend-analyzer.ts
│   │   │   │   └── heatmap-generator.ts
│   │   │   │
│   │   │   └── progress-engine/
│   │   │       ├── achievement-manager.ts
│   │   │       ├── streak-manager.ts
│   │   │       └── goal-manager.ts
│   │   │
│   │   │
│   │   └── application/
│   │       ├── use-cases/
│   │       │   ├── start-typing-session.ts
│   │       │   ├── record-keystroke.ts
│   │       │   ├── complete-session.ts
│   │       │   ├── evaluate-lesson.ts
│   │       │   ├── generate-exercise.ts
│   │       │   ├── analyze-performance.ts
│   │       │   └── get-recommendations.ts
│   │       │
│   │       └── ports/
│   │           ├── session-repository.ts
│   │           ├── progress-repository.ts
│   │           ├── profile-repository.ts
│   │           └── settings-repository.ts
│   │
│   │
│   ├── infrastructure/
│   │   │
│   │   ├── persistence/
│   │   │   ├── database.ts
│   │   │   ├── schema.ts
│   │   │   ├── migrations/
│   │   │   └── repositories/
│   │   │       ├── indexeddb-session-repository.ts
│   │   │       ├── indexeddb-progress-repository.ts
│   │   │       ├── indexeddb-profile-repository.ts
│   │   │       └── indexeddb-settings-repository.ts
│   │   │
│   │   ├── input/
│   │   │   └── browser-keyboard.ts
│   │   │
│   │   ├── workers/
│   │   │   ├── analytics.worker.ts
│   │   │   └── exercise.worker.ts
│   │   │
│   │   └── import-export/
│   │       ├── export-data.ts
│   │       └── import-data.ts
│   │
│   │
│   ├── data/
│   │   │
│   │   ├── curriculum/
│   │   │   ├── stage-00-foundations/
│   │   │   ├── stage-01-home-row/
│   │   │   ├── stage-02-top-row/
│   │   │   ├── stage-03-bottom-row/
│   │   │   ├── stage-04-capitalization/
│   │   │   ├── stage-05-numbers-punctuation/
│   │   │   ├── stage-06-letter-combinations/
│   │   │   ├── stage-07-vocabulary/
│   │   │   ├── stage-08-sentences/
│   │   │   └── stage-09-fluency/
│   │   │
│   │   ├── vocabulary/
│   │   │   ├── common-words.json
│   │   │   ├── difficult-words.json
│   │   │   └── technical-words.json
│   │   │
│   │   ├── sentences/
│   │   ├── paragraphs/
│   │   └── coding-exercises/
│   │
│   │
│   └── shared/
│       ├── components/
│       ├── hooks/
│       ├── keyboard/
│       ├── constants/
│       ├── types/
│       ├── utils/
│       └── styles/
│
│
├── tests/
│   ├── unit/
│   │   ├── typing-engine/
│   │   ├── learning-engine/
│   │   ├── exercise-engine/
│   │   ├── adaptive-engine/
│   │   └── analytics-engine/
│   │
│   ├── integration/
│   │   ├── learning-flow/
│   │   ├── session-flow/
│   │   └── persistence/
│   │
│   └── e2e/
│       ├── onboarding.spec.ts
│       ├── guided-learning.spec.ts
│       └── typing-practice.spec.ts
│
│
├── package.json
├── package-lock.json
├── tsconfig.json
├── vite.config.ts
├── tailwind.config.ts
├── eslint.config.js
├── .prettierrc
├── .gitignore
└── README.md
```
