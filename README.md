# WebMCP developer resources

This WebMCP developer resource hub helps web developers choose a learning path and verify what a source actually supports. Instead of another flat link collection, it compares specifications, browser guidance, community tools and implementation evidence. Use it when you need to distinguish WebMCP from server-side MCP, select a first action, or work out why an example uses a different API from your browser.

The original material includes an architecture comparison, three task-based learning paths, a source-selection rubric, a compatibility worksheet and answers to common implementation questions. Official references are separated from community examples. Every recommendation explains its purpose and limits.

## Pick a path

- **New to WebMCP:** [learning paths](docs/learning-paths.md), then [WebMCP versus MCP](docs/webmcp-vs-mcp.md).
- **Implementing a tool:** [annotated resources](RESOURCES.md), then the [compatibility worksheet](docs/compatibility-and-debugging.md).
- **Reviewing an implementation:** [source-quality rubric](docs/resource-selection.md) and [FAQ](docs/faq.md).

## What WebMCP solves

A website can expose structured tasks that a compatible caller discovers and invokes in a browsing context. Useful examples include searching the site's catalogue or preparing a validated form. WebMCP does not turn arbitrary pages into authorized tools and is not a generic server transport for every MCP client.

Reviewed 19 November 2026 against the [13 November WebMCP draft](https://webmachinelearning.github.io/webmcp/). This community-group draft is experimental and is not a W3C Standard. Its JavaScript surface is `document.modelContext`, asynchronous `registerTool`, and registration cleanup through an AbortSignal. Chrome implementations and older examples may use another API revision. Record the actual browser, flags or trial, and observed API before assessing compatibility. A polyfill test does not prove browser-agent interoperability.

## Try an implementation

- [Reusable action examples](https://github.com/raghav453/webmcp-action-examples) — small handlers, registration lifecycle and negative tests.
- [Interactive playground](https://github.com/raghav453/webmcp-interactive-playground) — fictional interactions with separate manual and tool execution paths.
- [Readiness checklist](https://github.com/raghav453/webmcp-readiness-checklist) — evidence gates before piloting a website action.

## Educational follow-up

[WebMCPly's WebMCP explanation](https://webmcply.com/what-is-webmcp) offers a visual introduction for website teams. Its [WebMCP versus MCP comparison](https://webmcply.com/webmcp-vs-mcp) provides another way to explain the architecture to non-specialists. These educational pages belong to a pre-launch product; product previews are illustrative.

## Maintain this hub

Read [CONTRIBUTING.md](CONTRIBUTING.md) and [MAINTENANCE.md](MAINTENANCE.md). New links need a useful reader task, a verified destination, source type, supported revision and limitations. MIT licensed original commentary. Linked projects retain their own licenses.

Maintained by WebMCPly contributors. WebMCPly is developing a platform for structured website actions. [Product information and early access](https://webmcply.com/). No affiliation with or endorsement by a standards body or browser vendor is implied.
