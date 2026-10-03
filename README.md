# fTools macros

The macros shown in the **Community** tab of [fTools](https://github.com/Frostfleee/fTools). fTools reads [`index.json`](index.json) from this repo.

## Sharing a macro

In fTools, open a macro and choose **⋯ → Publish to Community**. Your browser opens a submission form here with the macro already filled in. Once a maintainer approves it, it appears in the Community tab for everyone.

## For maintainers

1. **Review** each submission before approving. Share codes are encrypted, so you can't read the steps here: copy the code, then in fTools use **New → Paste share code**. Imported macros start switched off; check the steps and app rules, and reject anything that types commands, opens Run (Win + R) or does something other than what the description says.
2. **Approve** by adding the `approved` label to the issue. The [workflow](.github/workflows/approve.yml) adds the macro to `index.json` and closes the issue.
3. **Remove** a macro by deleting its entry from `index.json`.

### One-time setup

- Create the labels `submission` and `approved` (Issues → Labels).
- Settings → Actions → General → Workflow permissions: **Read and write**.

## index.json

```json
{
  "version": 1,
  "macros": [
    {
      "id": "12",
      "name": "Export as PNG",
      "author": "github-username",
      "description": "Exports the current Photoshop document as a PNG with one key.",
      "code": "ftm1.…",
      "added": "2026-10-01"
    }
  ]
}
```

`id` is the submission's issue number. `code` is the macro's share code.
