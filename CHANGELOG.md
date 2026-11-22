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
- `./update` runs `docker compose up -d --remove-orphans`, so containers removed from docker-compose.yml (such as dozzle) are removed from the host too
- Watchtower now updates on a configurable cron schedule (WATCHTOWER_SCHEDULE, default hourly) instead of a poll interval, and removes superseded images (WATCHTOWER_CLEANUP)
### Deprecated
### Removed
- Dozzle log viewer (port 8080, no authentication, Docker socket mounted): container logs now go to the journal and on to VictoriaLogs (credfeto-setup-arch-vm journald log driver), so it duplicated that
### Deployment Changes
- WATCHTOWER_POLL_INTERVAL replaced by WATCHTOWER_SCHEDULE (6-field cron); override via .env

<!--
Releases that have at least been deployed to staging, BUT NOT necessarily released to live.  Changes should be moved from [Unreleased] into here as they are merged into the appropriate release branch
-->

## [0.0.0] - Project created