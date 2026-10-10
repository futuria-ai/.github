## What and why

<!-- One or two sentences: what changes, and why. Link the ticket (FUT-NNNN). -->

## How it was tested

<!-- Tests added or changed, and where you tried it: local, or dev (your PR joins the dev bundle once its tests pass). -->

**How to tell it's working or broken after deploy:** <!-- the log line, metric or check to look at -->

**How to roll back:** <!-- revert, turn the flag off, or run the migration downgrade -->

## Review

Tick each box that applies. Each one links to its section of the [engineering guidance](https://futuria.atlassian.net/wiki/spaces/AAATM/pages/433913864).

- [ ] **Architecturally significant** ([guidance](https://futuria.atlassian.net/wiki/spaces/AAATM/pages/433913864#5.-Cross-service-contract-changes)): new endpoint, cross-service contract, new dependency, or data model change. If ticked, tag the architecture reviewer.
- [ ] **High-risk area**: touches auth or authz, database migrations, `.github/`, or charts and infra. Needs a release approver.
- [ ] **Env vars / flags** ([guidance](https://futuria.atlassian.net/wiki/spaces/AAATM/pages/433913864#1.-Environment-variables-and-feature-flags)): any new flag has an owner and a removal ticket. A bug fix is not behind a flag.
- [ ] **Supportability** ([guidance](https://futuria.atlassian.net/wiki/spaces/AAATM/pages/433913864#2.-Supportability:-logging,-errors-and-resilience)): new logs carry the context IDs, nothing sensitive is logged, and a failure can be traced by one ID.
- [ ] **Migration** ([guidance](https://futuria.atlassian.net/wiki/spaces/AAATM/pages/433913864#3.-Database-migrations)): has a working downgrade and runs safely while the old code is still live. A drop, rename or type change is done in two steps. It stays off the shared dev database unless you add the `dev-migration` label.
- [ ] **Secrets** ([guidance](https://futuria.atlassian.net/wiki/spaces/AAATM/pages/433913864#4.-Secrets)): any new secret key has its secret store mount updated first.
- [ ] **Cross-service contract change** ([guidance](https://futuria.atlassian.net/wiki/spaces/AAATM/pages/433913864#5.-Cross-service-contract-changes)): the consumers that change in the same release are named.
- [ ] **Affects staging or prod** beyond the code itself (config, data, a manual step): announce it in the dev chat before merging.

Reply to or resolve every Copilot `[BLOCKER]` and `[RISK]` before merging.

## Notes

<!-- Rollout steps, follow-ups, anything a reviewer should know. -->
