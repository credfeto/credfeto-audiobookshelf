# Changelog
All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

<!--
Please ADD ALL Changes to the UNRELEASED SECTION and not a specific release
-->

## [Unreleased]
### Security
### Added
### Fixed
### Changed
- Watchtower now updates on a configurable cron schedule (WATCHTOWER_SCHEDULE, default hourly) instead of a poll interval, and removes superseded images (WATCHTOWER_CLEANUP)
### Deprecated
### Removed
### Deployment Changes
- WATCHTOWER_POLL_INTERVAL replaced by WATCHTOWER_SCHEDULE (6-field cron); override via .env

<!--
Releases that have at least been deployed to staging, BUT NOT necessarily released to live.  Changes should be moved from [Unreleased] into here as they are merged into the appropriate release branch
-->

## [0.0.0] - Project created