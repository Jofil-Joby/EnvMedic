# EnvMedic

> Portable agent for identifying environment-variable usage that lacks a safe documentation surface.

## What it does

EnvMedic detects common environment-variable access patterns and checks whether the project exposes an `.env.example`-style reference. It helps make runtime configuration discoverable without exposing private values.

### Diagnostic fingerprint

**Environment usage → documentation gap → evidence → remediation**

## Why this agent is distinct

EnvMedic sits between application code and deployment configuration. Its focus is not secret detection itself, but whether environment-dependent behavior is documented in a safe, reproducible way.

## Workflow

```text
Source/config
    ↓
Environment-variable detector
    ↓
Documentation rule
    ↓
Evidence-backed finding
    ↓
Safe example configuration plan
```

## Verification

Includes:
- OpenGAP-compatible passport metadata
- environment-focused fixture
- explainability contract
- four framework adapters
- automated verification tests

OpenGAP validation passed and all four generated exports have been exercised successfully.

## Design principle

**Document names, not values.** EnvMedic encourages safe configuration examples while keeping sensitive runtime values outside the repository.

## Medic family

EnvMedic is the configuration-documentation specialist in the broader Medic family.