# Signer

This guide describes how to use the validation UI from the [task-signing-tool](https://github.com/base/task-signing-tool) to sign tasks in this repository. Your task’s `README.md` may add steps (which task to pick, rollback flows, multiple parts, etc.)-always follow those instructions first.

## Prerequisites

- A clone of this repo at the commit your facilitator specified.
- Node.js (the tool runs via npm). Install dependencies are handled when you start the UI.

## Start the signing UI

From the **repository root** (not inside a task directory):

```bash
make sign-task
```

Wait until the dev server is ready, then open [http://localhost:3000](http://localhost:3000) in your browser.

## Sign

1. Select the correct task (and role or part, if your task README distinguishes them).
2. Complete signing in the UI as prompted.
3. Copy the signature output and send it to the facilitator over the agreed channel.

When you are done, stop the dev server with `Ctrl+C` in the terminal where `make sign-task` is running.

## Ledger

If your task uses a hardware wallet, connect and unlock your Ledger and open the Ethereum app before signing. Task-specific READMEs may reference `LEDGER_ACCOUNT` or other env vars from the network `.env`.

## Further reading

- Task-specific validation text: `VALIDATION.md` or `validations/*.md` in the task folder.
- Facilitator steps: `FACILITATOR.md` or `FACILITATORS.md` when present.
