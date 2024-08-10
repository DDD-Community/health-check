
# health-check

> health check with github action

<br>

### Health Check Bot

> Four bots are operating through a cron-based scheduler.

- health-check
- health-check-bot-1
- health-check-bot-2
- health-check-bot-3
- health-check-bot-4

<br>

### Usage

If you want to add a health-check, add it according to the following spec.

```
      - name: alignlab health check
        run: |
          curl -X 'GET' \
          'https://api.alignlab.site/api/v1/health' \
          -H 'accept: application/json'
```

<br>

### Heads up

- If the health check fails prematurely, the entire specific bot may be terminated.
- API requests may take timeouts.
- Depending on the queue status of git-action, the task may be delayed.
- Scheduling does not guarantee time.
