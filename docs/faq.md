# Developer questions and misconceptions

## Is WebMCP a finished W3C Standard?

The reviewed 13 November 2026 document is a community-group draft, not a W3C Standard. Recheck its publication status when using this guide later.

## Does WebMCP work in every browser or AI agent?

No universal compatibility is established. Check the browser implementation, enabled feature/trial and caller. A polyfill enables an experimental path; it does not make all agents native WebMCP clients.

## Should I use document.modelContext or navigator.modelContext?

The current draft uses document.modelContext. Earlier implementations and examples can use navigator.modelContext. Pick a stated revision and test it; do not merge incompatible snippets without an explicit compatibility strategy.

## Can I just add toolname to a form?

Only supporting browser implementations interpret declarative tool attributes. Verify recognized attributes, discovery, submission, validation and return behavior using the browser guide. Plain HTML fallback still works without proving a tool invocation.

## Can the tool reuse an authenticated website session?

Application handlers may run in the site's browsing context, but each protected operation still needs authentication and resource-level authorization. Session presence is not permission to disclose every field or mutate every resource.

## Is readOnlyHint a guarantee?

No. Annotations communicate intended behavior. Application controls and tests must enforce the actual effect.

## Can a public scan prove a registered tool exists?

A crawl or source hint is not enough. Collect discovery and execution evidence in the named runtime, including expected outputs and failure cases.

## Does publishing WebMCP tools improve search rankings?

There is no verified ranking guarantee. Useful documentation and examples can attract readers; measure search impressions, engagement and referrals independently.

## Is WebMCPly available as a complete SaaS?

WebMCPly is in pre-launch at this review. Its public educational resources and fictional interactive previews do not establish operational product integrations.

## What should I implement first?

A narrow read-only lookup with bounded inputs, known fixture results, explicit errors and cancellation. Add consequential workflows only after access, confirmation and recovery have been reviewed.

See [RESOURCES.md](../RESOURCES.md) for primary-source annotations and [MAINTENANCE.md](../MAINTENANCE.md) for review criteria.
