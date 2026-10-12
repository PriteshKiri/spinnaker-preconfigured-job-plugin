# Contributing to spinnaker-preconfigured-job-plugin

Thanks for your interest in contributing! This repository is the Spinnaker plugin that exposes LitmusChaos experiments as preconfigured job stages.

## Getting Started

### Ask Questions or Discuss Ideas

Join the community on [Slack](https://slack.litmuschaos.io) and post in **#litmus** for general questions or **#litmus-dev** for technical discussions.

### Report Issues or Propose Changes

Open a new [GitHub issue](https://github.com/litmuschaos/spinnaker-preconfigured-job-plugin/issues/new) describing your request, bug, or feature idea. For larger changes, please open an issue and reach agreement with the maintainers before writing code.

## What Lives Here

A Gradle/Kotlin project. `build.gradle` and `settings.gradle` drive the build, and `gradle.properties` pins the Spinnaker service versions the plugin compiles against.

## Developer Certificate of Origin (DCO)

All contributions must be signed off with the **Developer Certificate of Origin**, confirming you have the legal right to submit your work. Add a line to every commit message:

```
Signed-off-by: Joe Smith <joe.smith@email.com>
```

To sign off automatically, set your git identity and use `git commit -s`:

```bash
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"
git commit -s
```

Use your real name — no pseudonyms or anonymous commits. For full details, see the [DCO documentation](https://developercertificate.org/).

## Submitting a Pull Request

1. **Fork the repository** and create a feature branch from the default branch.
2. **Make your change.** Keep pull requests focused on a single concern.
3. **Validate locally** before pushing — see below.
4. **Open the pull request**, describing what changed and why. Link the issue it addresses.
5. **Respond to review.** Maintainers will review and may request changes.

## Validating Your Changes

```bash
./gradlew build
./gradlew test
```

The `latestKork.yml` and `latestOrca.yml` workflows build against current Spinnaker upstream, so a change that compiles locally may still break there if it depends on a newer API.

Never commit secrets, credentials, or kubeconfigs. Check `git diff --staged` before committing.

## Code of Conduct

This project follows the [LitmusChaos Code of Conduct](https://github.com/litmuschaos/litmus/blob/master/CODE_OF_CONDUCT.md).

## Security

To report a vulnerability, see [SECURITY.md](SECURITY.md). Please do not open a public issue for security problems.
