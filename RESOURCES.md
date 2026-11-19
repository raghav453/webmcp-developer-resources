# Annotated WebMCP resources

Verified 19 November 2026. “Official” identifies source ownership; it does not mean every proposal is standardized or every API is available.

## Specifications and browser documentation

| Resource | Use it for | Check before copying |
| --- | --- | --- |
| [WebMCP draft](https://webmachinelearning.github.io/webmcp/) | Current IDL, registration/discovery/execution and lifecycle definitions | Community draft dated 13 November; implementation may lag |
| [Chrome WebMCP guide](https://developer.chrome.com/docs/ai/webmcp) | Origin trial/local testing and browser-specific implementation, including declarative forms | Guide revision and actual browser/API surface |
| [Chrome best practices](https://developer.chrome.com/docs/ai/webmcp/best-practices) | Designing coherent tasks and contracts | Advice is not a server authorization guarantee |
| [Chrome comparison with MCP](https://developer.chrome.com/docs/ai/webmcp/compare-mcp) | Explaining browser context versus server integration | Distinguish API availability from architecture |
| [Agent security guidance](https://developer.chrome.com/docs/agents/security) | Prompt injection, permissions and consequential action boundaries | Apply application controls and negative tests |
| [MCP architecture](https://modelcontextprotocol.io/docs/2026-07-28/learn/architecture) | Hosts, clients, servers and transports in server-side MCP | Versioned MCP documentation, not the WebMCP API |

## Open-source tools and experiments

| Resource | Useful job | Limitations |
| --- | --- | --- |
| [GoogleChromeLabs/webmcp-tools](https://github.com/GoogleChromeLabs/webmcp-tools) | Browser utilities, demo source, inspection and evaluation workflows | Each subproject has its own setup and supported API revision; not a guarantee for all agents |
| [W3C OSS WebMCP polyfill](https://github.com/w3c-oss/webmcp-polyfill) | Reproducible experimentation with draft discovery/execution | Apache-2.0; pin version, distinguish polyfill behavior from native interoperability |
| [Web Machine Learning community list](https://github.com/webmachinelearning/awesome-webmcp) | Discover publicly shared experiments, websites and articles | Editorial discovery; individual entries still need independent verification |
| [Webfuse community list](https://github.com/webfuse-com/awesome-webmcp) | Find community tutorials, examples and integration approaches | Community commentary and API versions vary |

## How to use declarative learning resources

Begin with Chrome's guide, not a random HTML snippet. Identify the recognized form attributes, input constraints, submission behavior and result mechanism for that browser. Check discovery with a supported inspector. Leave consequential submission under human control. Ordinary HTML submission is useful fallback evidence but not proof of WebMCP execution.

## How to use imperative learning resources

Compare the example's entry point, registerTool return type, discovery surface and teardown mechanism with the current draft and runtime. An older navigator.modelContext snippet may teach a concept, but it is not interchangeable with today's document.modelContext IDL. Pin the runtime or migrate; do not silently patch the global API to claim native support.

## Framework, testing and security follow-up

Use the [learning paths](docs/learning-paths.md) to apply these sources to a task. Check lifecycle during router teardown and login changes. Prefer handler tests with bad input and cancellation plus independent discovery/execution evidence. A tool list without these details is not an implementation guide.

The companion [security review](https://github.com/raghav453/webmcp-security-checklist) turns source guidance into threat cases and test evidence. Its checklist does not certify security.
