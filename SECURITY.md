# Security status

This repository is an educational copy of Cosmic Themes' Blogsmith Free, not a hardened production distribution.

## Initial dependency review

The upstream source is commit `3d0849221b0a6f098b59b169a738745d2a6447a5`. Its dependency versions were retained rather than performing a framework migration while preparing the workshop.

The initial npm dependency audit reported 26 vulnerable packages: 1 critical, 21 high, 2 moderate, and 2 low. The audit includes the Astro framework, image processing dependencies, build integrations, and development tooling. Severity in the dependency report does not establish exploitability in every deployment, but the findings must not be treated as resolved merely because the static build succeeds.

The local production build succeeded. That verifies build compatibility in the tested environment, not security or hosted deployment behavior.

## Workshop precautions

- Use only fictional or cleared public content.
- Keep development servers local. Do not bind them to a public interface.
- Do not add credentials, authentication, databases, payments, or API integrations for the exercise.
- Keep dependency install and build operations in a project environment, not a production server.
- Do not assume example articles, author profiles, or the sample privacy policy are appropriate for your own published site.

## Before production use

Run a fresh `npm audit`, remediate applicable advisories, and test the resulting dependency changes. Framework upgrades may require compatible integration updates and source migrations. Do not run `npm audit fix --force` blindly.

Review asset rights, site metadata, deployment permissions, links, and any policy text before a real public launch. A passing build and an empty environment file are not a complete security review.
