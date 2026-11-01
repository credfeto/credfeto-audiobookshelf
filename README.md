# credfeto-audiobookshelf

Docker configuration for audio booksheld

## Configuration

Settings can be overridden per host in a `.env` file next to `docker-compose.yml`.
Copy [.env.example](.env.example) to `.env` and uncomment the values to change.
The `.env` file is git-ignored and must never be committed.

### Watchtower

Watchtower checks for updated images on a schedule and removes superseded images after updating (`WATCHTOWER_CLEANUP` is enabled).

| Variable              | Type   | Default       | Description                                              |
| --------------------- | ------ | ------------- | -------------------------------------------------------- |
| `WATCHTOWER_SCHEDULE` | string | `0 0 * * * *` | When to check for updates (6-field cron, seconds first). |

The schedule uses Watchtower's 6-field cron format: `second minute hour day month weekday`.
The default runs hourly, on the hour. To update at a different time on a host, for example daily at 03:30, set it in `.env`:

```sh
WATCHTOWER_SCHEDULE="0 30 3 * * *"
```
