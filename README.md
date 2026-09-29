# pi-tiny-replay

A Pi extension that rewrites compatible assistant messages for configured model families, so the active model receives a family member's messages as its own. Configure families with `replayCompatibleModels` in `~/.pi/agent/settings.json`:

```json
{
  "replayCompatibleModels": [
    [
      "github-copilot/gpt-5.6-sol",
      "github-copilot/gpt-5.6-luna"
    ]
  ]
}
```

Families use `provider/model` IDs. Messages from another API are left to Pi's normal conversion.

## Install

```bash
pi install git:github.com/spoj/pi-tiny-replay
```

Or try it locally:

```bash
pi -e ./extensions/replay.ts
```

## Development

```bash
npm install
npm run check
```
