# Compatibility worksheet and debugging order

Reviewed 19 November 2026 against the [13 November WebMCP draft](https://webmachinelearning.github.io/webmcp/). This community-group draft is experimental and is not a W3C Standard. Its JavaScript surface is `document.modelContext`, asynchronous `registerTool`, and registration cleanup through an AbortSignal. Chrome implementations and older examples may use another API revision. Record the actual browser, flags or trial, and observed API before assessing compatibility. A polyfill test does not prove browser-agent interoperability.

Copy this record into your test notes:

```text
Date / commit:
Browser / version / OS:
Origin / secure context:
Feature flag or origin-trial setup:
Caller / version:
API revision and observed methods:
Mode: native / polyfill / manual only
Registered names / origins / schemas:
Invocation interface and fixture:
Expected result / actual result:
Cancellation / cleanup result:
Untested combinations:
```

## If an example does not work

1. **No API:** verify secure context, browser setup and guide revision. Show an unsupported/manual state. Do not silently inject a mock and call it native support.
2. **Different entry point:** determine whether the code targets an earlier navigator.modelContext implementation. Choose an explicit adapter/runtime or migrate to the draft; preserve revision notes.
3. **Registration rejects:** inspect the sanitized error, duplicate names, schema and readiness of dependencies. Await the promise before declaring success.
4. **Discovery empty:** verify the correct origin/window, registration scope and teardown state. A local in-memory list proves only local storage.
5. **Execution fails:** use a known small fixture, validate types, inspect the supported caller signature and output serialization. Draft executeTool accepts a discovered tool object.
6. **UI differs from tool result:** identify separate handlers or stale state. Use one domain function and render returned results safely.
7. **Only the first visit works:** test route teardown, login changes and repeat mounting. Abort old registration and pending work before replacement.

## What qualifies as evidence?

Handler tests: useful for business logic and validation. Mock contract tests: useful for intended registration shape. Polyfill integration: useful for draft experimentation. Native discovery/execution: evidence only for the named browser/caller. External agent task: evidence for that particular integration and task. Keep these separate in test reports.

Official setup: [Chrome guide](https://developer.chrome.com/docs/ai/webmcp). Draft interfaces: [WebMCP](https://webmachinelearning.github.io/webmcp/).
