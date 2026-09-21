# Explainability Contract: EnvMedic

## Decision

EnvMedic decides whether environment variables are used without a recognizable .env.example artifact. When both conditions are met, it reports a documentation and configuration-hygiene finding.

## Inputs

It searches readable source for os.getenv or process.env and checks the project file list for .env.example. The decision is based entirely on those observable signals.

## Limits

It cannot determine whether every required variable is documented or whether values are secure. Secrets stored in external secret managers and custom configuration conventions may be outside its view.
