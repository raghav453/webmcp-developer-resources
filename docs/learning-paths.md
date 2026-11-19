# Task-based learning paths

## Path A: understand the model

Outcome: explain a website action without confusing it with a server-side MCP server.

1. Read the draft introduction and [architecture comparison](webmcp-vs-mcp.md).
2. Choose a website task you can already complete manually.
3. Write its inputs, expected result, access boundary and effects in plain language.
4. Identify which facts are public observations and which need browser execution evidence.

Exercise: a catalogue search returns public products; an account update uses protected data and changes state. Explain why the same discovery surface does not justify the same permission policy. Completion artifact: two short action contracts, no API code required.

## Path B: implement one read-only action

Outcome: discover and execute a bounded lookup in a recorded environment.

1. Read Chrome's implementation/setup guide and the current draft IDL. Record the actual API surface in the [compatibility worksheet](compatibility-and-debugging.md).
2. Start with the companion [action examples](https://github.com/raghav453/webmcp-action-examples). Read the handler before running it.
3. Test a valid query, an empty result, wrong type, unknown property and abort.
4. Verify tool registration and execution independently from manual form submission.
5. Abort registration, check discovery, then register once again.

Completion artifact: one sanitized evidence record with caller path, expected/actual results and limitations. A passing handler test alone does not close this path.

## Path C: review a consequential workflow

Outcome: show that a proposal cannot silently become a committed change.

1. Use the companion [security checklist](https://github.com/raghav453/webmcp-security-checklist) to map trust boundaries.
2. Separate preparation from final mutation. Identify the exact payload, principal and freshness to bind to review.
3. Test cancellation, timeout, changed payload, expired session, cross-account resource IDs and replay.
4. Record which controls exist in the browser demo and which require a real server.

Completion artifact: threat table, confirmation evidence and unresolved server requirements. Do not classify a local confirmation dialog as production authorization.

## Framework notes

In component frameworks, own registration in the effect/lifecycle that owns its data and UI. Await setup, cancel on teardown, and handle development double-mounts without duplicate registrations. Server rendering does not have the browser document API. Delay browser-only registration to client initialization. On route or session changes discard stale closures and in-flight actions. Test transitions, not just initial render.
